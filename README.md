# Ashmii Website Recovery Case Study

> **Note:** This repository documents the engineering process followed during the recovery of a production WordPress website. No client source code, database dumps, credentials, or proprietary assets are included.

## Table of Contents

- [Project Type](#project-type)
- [Background](#background)
- [Recovery Objectives](#recovery-objectives)
- [Key Challenges](#key-challenges)
- [Recovery Actions](#recovery-actions)
- [Outcome](#outcome)
- [Project Highlights](#project-highlights)
- [Skills Demonstrated](#skills-demonstrated)
- [Repository Contents](#repository-contents)

## Project Type

WordPress disaster recovery, website reconstruction, infrastructure recovery, security cleanup, and production relaunch.

---

## Background

Ashmii.com had been dormant for nearly a year after the original hosting environment and recent backups became unavailable. The recovery effort required reconstructing the website from fragmented assets, recovered infrastructure access, archived web content, and legacy backups while preserving the original design, functionality, and site structure.
---

## Recovery Objectives

* Restore the website to an operational state.
* Preserve as much original content and functionality as possible.
* Recover missing infrastructure and licensed assets.
* Resolve compatibility and security issues.
* Validate the website before production deployment.

---

## Key Challenges

* Lost hosting environment
* Incomplete and partially corrupted backup archives
* Database compatibility issues during restoration
* Missing uploads and media assets
* Broken images and internal links
* WPBakery rendering issues after restoration
* Malicious JavaScript injection discovered in the Head, Footer and Post Injections plugin
* Cloudflare and DNS recovery
* Recovery of licensed theme resources through the original ThemeForest account

---

## Recovery Actions

### Infrastructure Recovery

* Recovered Cloudflare account access
* Recovered ThemeForest account access
* Reviewed DNS and infrastructure configuration
* Established a dedicated staging environment for recovery

### WordPress Recovery

* Imported and reconstructed the recovered database
* Restored themes, plugins, and uploads where available
* Reinstalled and reconfigured WPBakery Page Builder
* Resolved plugin compatibility issues
* Fixed broken links and broken image references
* Recovered media assets using archived web snapshots, legacy resources, and manual reconstruction techniques.

### Security

* Investigated the recovered environment for malware
* Identified and removed malicious JavaScript injection
* Reviewed plugins and configuration for security issues
* Performed post-recovery validation

### Deployment

* Completed functional testing on staging
* Validated content, navigation, and media
* Deployed the recovered website to the live environment
* Performed post-launch verification

---

## Outcome

The website was successfully reconstructed from fragmented assets and returned to production. The recovery restored the site's navigation, functionality, media, and overall user experience while resolving infrastructure, compatibility, and security issues identified during the reconstruction process.

---

## Project Highlights

- Successfully recovered a dormant production WordPress website.
- Restored infrastructure access, including Cloudflare and ThemeForest.
- Reconstructed the website using legacy backups and archived content.
- Recovered approximately 95% of website media assets.
- Removed malicious JavaScript injected into the WordPress installation.
- Validated the recovered website in a staging environment before production deployment.


## Skills Demonstrated

* WordPress Disaster Recovery
* Website Reconstruction
* Infrastructure Recovery
* Cloudflare Administration
* ThemeForest Asset Recovery
* Database Troubleshooting
* WPBakery Recovery
* Plugin Compatibility Resolution
* Malware Investigation and Cleanup
* Media Recovery
* DNS Management
* Staging-to-Production Deployment
* Technical Documentation

## Repository Contents

- `docs/01-project-overview.md` – Project background, objectives, and recovery strategy
- `docs/02-recovery-log.md` – Chronological log of the recovery process
- `screenshots/` – Before, recovery, and after screenshots
- `assets/` – Diagrams and supporting material
- `references/` – Useful references used during the recovery

## Disclaimer

This repository documents the technical recovery process for educational and portfolio purposes. It intentionally excludes client source code, proprietary assets, database backups, credentials, and any confidential information. The focus is on the engineering methodology, troubleshooting process, and lessons learned during the recovery.
