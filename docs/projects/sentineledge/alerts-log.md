# SentinelEdge Endpoint Security – Security Alerts & Logs Documentation

## Objective

This document describes how **SentinelEdge Endpoint Security** generates security alerts and logs, and provides guidance for administrators to interpret them effectively. This ensures timely response and accurate investigation of security incidents.

## Intended Audience

*   **SOC Analysts:** For real-time monitoring and incident triage.
    
*   **IT Administrators:** For system health monitoring and audit compliance.
    

* * *

## Alert Severity Levels

SentinelEdge prioritizes alerts to help security teams focus on the most critical threats first.

| Severity | Description | Action Recommended |
| --- | --- | --- |
| Critical | Immediate high-impact threat (e.g., active ransomware). | Immediate isolation and remediation. |
| High | Strong indicators of compromise or targeted attack. | Prioritized investigation within the hour. |
| Medium | Suspicious activity that deviates from established baselines. | Investigation during the current shift. |
| Low | Known malware blocked or minor policy violations. | Routine review and cleanup. |
| Informational | Successful administrative actions or system status updates. | No action required; used for auditing. |

* * *

## Common Alert Types

SentinelEdge categorizes alerts based on the protection module that triggered the detection.

*   **Ransomware Detection:** Triggered by behavioral monitoring when a process attempts to encrypt files rapidly or delete shadow copies.
    
*   **Exploit Prevention:** Triggered when the system blocks techniques like buffer overflows or heap sprays targeting software vulnerabilities (e.g., EternalBlue-style attacks).
    
*   **Behavioral Anomaly:** Triggered when a legitimate process exhibits unusual behavior, such as a word processor launching a command shell.
    
*   **Malware Blocked:** Triggered when a file matches a known malicious signature during a scan or upon execution.
    

* * *

## Log Locations

Administrators can access logs both locally on the endpoint for deep forensics and centrally for environmental oversight.

### Local Agent Logs

Used for troubleshooting connectivity or inspecting raw event data on a specific machine.

*   **Windows:** `%ProgramData%\SentinelEdge\Logs\`
    
*   **Linux:** `/var/log/sentineledge/`
    
*   **macOS:** `/Library/Logs/SentinelEdge/`
    

### Centralized Management Console

The primary location for SOC analysts to view aggregated logs.

*   **Alert Dashboard:** Summarizes active threats across the fleet.
    
*   **Audit Logs:** Records administrative changes, such as policy updates or agent uninstalls.
    
*   **Event Logs:** Detailed record of all telemetry sent from endpoint agents to the console.
    

* * *

## Example Alert Scenarios

### Scenario 1: Ransomware Mitigation

*   **Alert Title:** `Behavioral: Ransomware Encryption Blocked`
    
*   **Severity:** **Critical**
    
*   **Scenario:** A user downloaded a malicious attachment. SentinelEdge detected the file attempting to rename and encrypt files in the `Documents` folder.
    
*   **Admin Interpretation:** The threat was stopped in its tracks. The admin should verify if any files were modified before the block and check other endpoints for the same file hash.
    

### Scenario 2: Exploit Attempt

*   **Alert Title:** `Exploit: Memory Protection Triggered`
    
*   **Severity:** **High**
    
*   **Scenario:** An outdated version of a web browser was targeted by a drive-by download. SentinelEdge blocked the memory injection attempt.
    
*   **Admin Interpretation:** The endpoint is a target for exploitation. The admin should prioritize patching the browser version on this and all other machines.
    

* * *

## Summary
By monitoring these alerts and logs, administrators maintain visibility into the security posture of their organization. SentinelEdge provides the necessary context—from severity to local log paths—to move quickly from detection to resolution.