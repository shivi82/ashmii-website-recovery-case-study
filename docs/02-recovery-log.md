# Ashmii Website Recovery Log

**Recovery Period:** June 18, 2026 – June 27, 2026

## Project Goal

Recover and reconstruct Ashmii.com after the loss of the original hosting environment, incomplete backups, and missing website assets.

## Phase 1 – Asset Discovery & Infrastructure Recovery

### 1. Digital Asset Recovery

* Recovered access to legacy Google accounts and Google Drive repositories.
* Identified and collected all available recovery assets, including backups, theme packages, and historical project files.

### 2. Information Gathering

* Coordinated with previous team members over several days to identify forgotten credentials, historical email accounts, and any remaining access information that could assist the recovery process.

### 3. Infrastructure Preparation

* Provisioned a new hosting environment.
* Recovered Cloudflare account access.
* Reviewed and reconfigured DNS records to support the new recovery environment.

---

## Phase 2 – Recovery Environment

### 4. Staging Environment

* Enabled maintenance mode on the production website.
* Created a dedicated staging environment.
* Performed all recovery and validation work on staging before production deployment.

---

## Phase 3 – Database Recovery

### 5. Database Reconstruction

* Initial database restoration resulted in compatibility issues.
* Resolved the problem by selectively migrating core WordPress tables and validating the site after each stage of the restoration process.

---

## Phase 4 – Theme & Plugin Recovery

### 6. Initial Website Restoration

* Successfully restored the website to a functional but incomplete state.
* Identified rendering issues affecting WPBakery Page Builder and Slider Revolution.
* Discovered that several backup archives were incomplete or corrupted.

### 7. Plugin Recovery

* Identified required WordPress plugins.
* Reinstalled and configured all available free plugins.
* Verified compatibility with the restored WordPress installation.

### 8. Premium Theme Recovery

* Recovered access to the original ThemeForest account.
* Downloaded licensed theme packages and bundled premium plugins.
* Restored premium components and resolved compatibility issues.

---

## Phase 5 – Media Recovery

### 9. Image Reconstruction

* Discovered that the recovered uploads directory contained virtually no usable media assets.
* Used Wayback Machine snapshots and historical website references as the primary recovery source.
* Worked with two assistants over three days to manually recover and restore approximately 95% of the website images across 28 pages.

---

## Phase 6 – Website Validation

### 10. Content Validation

* Identified and corrected broken internal links.
* Repaired broken image references.
* Verified page layouts and navigation.

### 11. Functional Testing

* Performed end-to-end functional testing on the staging environment.
* Validated page rendering, navigation, media assets, and plugin functionality prior to launch.

---

## Phase 7 – Production Deployment

### 12. Production Launch

* Reconfigured Cloudflare for the recovered production environment.
* Migrated the validated staging environment to the live website.
* Performed post-deployment verification to ensure successful restoration.


# Recovery Metrics

* **Project Duration:** June 18, 2026 – June 27, 2026 (9 days)
* **Pages Reviewed & Validated:** 28
* **Recovery Environment:** Dedicated staging environment created and validated before production deployment
* **Images Recovered:** Approximately 95% using archived sources and available assets
* **Infrastructure Recovery:** Cloudflare and ThemeForest account access successfully recovered
* **Database Recovery:** Successfully reconstructed from a legacy backup
* **Theme Recovery:** Original Archi theme restored
* **Plugin Recovery:** Free plugins reinstalled and premium plugins restored
* **Media Recovery:** Broken images and media references repaired
* **Website Validation:** Broken links, page rendering, navigation, and responsiveness verified before launch
* **Production Deployment:** Successfully migrated from staging to the live environment
* **Security Review:** Malicious JavaScript injection identified within the Head, Footer and Post Injections plugin configuration and safely removed during the security review.


## Conclusion

The recovery successfully restored Ashmii.com from a partially recoverable state using legacy assets, recovered infrastructure access, and manual reconstruction techniques. By following a staged recovery approach, the website was safely validated before being deployed back to production.