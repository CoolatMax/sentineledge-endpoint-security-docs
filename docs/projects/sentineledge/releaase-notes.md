# SentinelEdge Endpoint Security – Release Notes & Security Advisories

## Objective

# 

This document provides a centralized record of new features, security enhancements, and known issues for SentinelEdge Endpoint Security. It ensures that security teams and administrators are informed of changes that impact their security posture and system stability.

## Intended Audience

# 

*   **All Users:** To stay informed about new features and UI changes.
    
*   **Security Teams:** To track vulnerability fixes and evaluate user impact.
    

* * *

## Release v2.4.0 (Current)

# 

**Release Date:** October 24, 2023

### New Features

# 

*   **Enhanced Memory Scanning:** Improved detection for "fileless" malware residing in system memory.
    
*   **macOS Sonoma Support:** Official support for the latest macOS release, including updated system extensions.
    
*   **Custom Alert Webhooks:** Administrators can now send real-time alerts to third-party tools like Slack, Microsoft Teams, or Jira.
    

### Security Fixes

# | Reference | Severity | Description | User Impact |
| --- | --- | --- | --- |
| CVE-2023-4412 | High | Fixed a local privilege escalation (LPE) vulnerability in the Windows agent service. | Prevents a limited user from gaining SYSTEM-level access via a symbolic link. |
| CVE-2023-4413 | Medium | Fixed a potential denial-of-service (DoS) in the network filter driver. | Resolves rare system crashes (BSOD) when processing malformed network packets. |

### Known Issues

# 

*   **Performance:** Slight CPU spike observed on Linux servers during initial deep-scan indexing. _Workaround:_ Schedule deep scans during maintenance windows.
    
*   **UI Bug:** The "Last Seen" timestamp in the management console may lag by up to 5 minutes for agents using proxy servers.
    

* * *

## Release v2.3.5

# 

**Release Date:** August 12, 2023

### Security Enhancements

# 

*   **Tamper Protection:** Hardened the agent's core processes to prevent unauthorized termination by advanced ransomware.
    
*   **Encrypted Log Transport:** All telemetry sent from the endpoint to the console now utilizes TLS 1.3 by default.
    

### Improvements

# 

*   **Reduced Agent Footprint:** Optimized background memory usage by 15% on Windows 10/11 devices.
    
*   **Bulk Exclusions:** Added the ability to import exclusion lists via CSV in the management console.
    

* * *

## Upgrade Notes

# 

1.  **Backup Policies:** Always export your current security policies before performing a major version upgrade.
    
2.  **Staged Rollout:** We recommend deploying the update to a "Canary" group of 5-10% of your endpoints before a full-scale rollout.
    
3.  **Reboot Requirements:** Version 2.4.0 requires a system restart on Windows endpoints to update the core protection driver.
    

* * *

## Vulnerability Reporting

# 

If you discover a security vulnerability in SentinelEdge, please do not report it via public GitHub issues. Instead, email our security team at `security@sentineledge-fictional.com`. We follow coordinated vulnerability disclosure (CVD) practices.

* * *

## Summary

# 

SentinelEdge is committed to transparency and continuous improvement. By reviewing these release notes regularly, administrators can ensure their endpoints are running the most secure and stable version of the platform.