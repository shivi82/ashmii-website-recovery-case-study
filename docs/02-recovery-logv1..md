# Ashmii Website Recovery Log

## Recovery Timeline

> **Project Goal:** Recover and reconstruct Ashmii.com after the loss of the original hosting environment, incomplete backups, and missing website assets.

---

## Milestone 1 – Infrastructure Recovery

### Objectives

Recover access to critical infrastructure required for the restoration process.

### Actions Completed

* Recovered Cloudflare account access.
* Reviewed DNS configuration.
* Documented existing Cloudflare settings.
* Recovered ThemeForest account access to obtain the original licensed theme and bundled plugins.

### Outcome

Infrastructure access was successfully restored, enabling the recovery process to proceed.

---

## Milestone 2 – Recovery Environment

### Objectives

Create a safe environment for reconstruction.

### Actions Completed

* Created a staging subdomain.
* Installed a fresh WordPress instance.
* Configured the recovery environment.
* Connected the staging site to the recovered database.

### Outcome

An isolated recovery environment was established to prevent any impact on the production website.

---

## Milestone 3 – Database Recovery

### Objectives

Restore the website database.

### Challenges

* Initial database import failed due to compatibility issues.
* Full restoration prevented WordPress from loading.

### Actions Completed

* Investigated database compatibility.
* Performed selective table migration.
* Corrected database configuration issues.
* Successfully restored WordPress functionality.

### Outcome

The website database was reconstructed successfully.

---

## Milestone 4 – Theme & Plugin Recovery

### Objectives

Restore the original website appearance and functionality.

### Actions Completed

* Restored the Archi theme.
* Recovered required plugins.
* Reinstalled WPBakery Page Builder.
* Restored bundled premium plugins from ThemeForest resources.
* Corrected page builder rendering issues.

### Outcome

Website layouts rendered correctly and page content became accessible.

---

## Milestone 5 – Media Recovery

### Challenges

* Uploads archive was incomplete.
* Multiple media assets were missing.
* Several broken images appeared throughout the website.

### Actions Completed

* Investigated uploads directory.
* Restored available media assets.
* Repaired image references.
* Recovered additional assets where available.

### Outcome

Most media content was successfully restored.

---

## Milestone 6 – Content Recovery

### Actions Completed

* Reviewed recovered pages.
* Corrected internal links.
* Fixed broken navigation.
* Reconstructed missing content using archived sources where appropriate.

### Outcome

Website navigation and content structure were restored.

---

## Milestone 7 – Security Review

### Findings

A malicious JavaScript payload was discovered during the recovery process.

The injected script attempted to capture user input and transmit data to external domains.

### Actions Completed

* Identified the injection source.
* Removed malicious code.
* Reviewed plugins and configuration.
* Performed additional security verification.

### Outcome

The recovered environment was cleaned and validated before deployment.

---

## Milestone 8 – Validation

### Testing Performed

* Homepage validation
* Internal navigation
* Media verification
* Responsive layout testing
* Plugin functionality
* Broken link verification
* Broken image verification

### Outcome

The staging website was considered ready for production deployment.

---

## Milestone 9 – Production Deployment

### Actions Completed

* Migrated validated changes from staging.
* Verified production environment.
* Confirmed successful deployment.
* Performed post-launch testing.

### Outcome

Ashmii.com was successfully returned to production.

---

# Lessons Learned

* Always maintain multiple verified backups.
* Keep staging synchronized with production.
* Preserve infrastructure access whenever possible.
* Validate database compatibility before restoration.
* Review recovered websites for malware before deployment.
* Maintain recovery documentation throughout the project.

---

# Technical Skills Demonstrated

* WordPress Disaster Recovery
* Cloudflare Administration
* ThemeForest Asset Recovery
* Database Reconstruction
* Plugin Compatibility Resolution
* WPBakery Recovery
* Malware Investigation
* Media Restoration
* DNS Management
* Staging-to-Production Deployment
* Technical Documentation
* WordPress Troubleshooting
