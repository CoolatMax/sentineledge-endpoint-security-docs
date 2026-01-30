# SentinelEdge Endpoint Security – Troubleshooting Guide

## Objective

# 

This guide helps administrators diagnose and resolve common issues encountered with SentinelEdge Endpoint Security. It is designed to provide quick, actionable solutions to minimize downtime and maintain a strong security posture.

## Intended Audience

# 

*   **IT Support Teams:** For resolving local installation and performance issues.
    
*   **Security Administrators:** For managing policy conflicts, false positives, and connectivity.
    

* * *

## 1\. Installation & Deployment Failures

# | Problem | Potential Cause | Solution |
| --- | --- | --- |
| Installer fails to start | Insufficient user privileges. | Right-click the installer and select "Run as Administrator." |
| Error: "Incompatible Software Detected" | Existing antivirus or EDR is conflicting with SentinelEdge. | Uninstall the existing security software and restart the endpoint before retrying the installation. |
| Agent does not appear in Console | Network ports are blocked or there is no internet access. | Ensure outbound traffic is allowed on Port 443 and the endpoint can reach the SentinelEdge Management URL. |
| "System Extension Blocked" (macOS) | macOS security policy requires manual approval. | Go to System Settings > Privacy & Security and click "Allow" for the SentinelEdge system extension. |

* * *

## 2\. System Performance Issues

# | Problem | Potential Cause | Solution |
| --- | --- | --- |
| High CPU/RAM usage during scans | Scan intensity is set too high for the hardware. | Adjust the Scan Performance Policy in the management console to "Balanced" or "Background" mode. |
| Slow application startup | Real-time behavioral monitoring is analyzing the app's initial execution. | If the application is known and safe, add the application path to the Exclusions List in the security policy. |
| Network latency | Large log uploads or signature updates. | Schedule updates during non-peak hours via the Global Settings menu. |

* * *

## 3\. Managing False Positives

# | Problem | Potential Cause | Solution |
| --- | --- | --- |
| Legitimate internal tool blocked | The tool uses "exploit-like" techniques (e.g., custom scripts, memory injection). | 1. Navigate to the Alerts tab.2. Select the detection.3. Review the behavior and select "Mark as False Positive" to globally whitelist the file hash. |
| Ransomware alert on database backup | Large-scale file renaming/encryption during backup mimics ransomware. | Add the specific backup process or destination folder to the Ransomware Protection Exclusions. |

* * *

## 4\. Common Error Messages

# 

*   **Error 1002: Connection Timed Out**
    
    *   _Meaning:_ The agent cannot reach the management console.
        
    *   _Fix:_ Check local firewall settings and verify that the SentinelEdge service is running in `services.msc`.
        
*   **Error 2050: Database Corrupted**
    
    *   _Meaning:_ The local threat definitions database is unreadable.
        
    *   _Fix:_ Trigger a "Force Update" from the console or manually delete the `\Definitions` folder and restart the agent.
        
*   **Error 403: Unauthorized Agent**
    
    *   _Meaning:_ The agent registration token has expired or was revoked.
        
    *   _Fix:_ Re-generate a deployment token from the console and re-install the agent.
        

* * *

## 5\. Log Collection for Support

# 

If an issue persists, collect the following logs before contacting SentinelEdge Technical Support:

1.  **Windows:** Run the `SE-DiagnosticTool.exe` found in `%ProgramFiles%\SentinelEdge\Tools\`.
    
2.  **Linux/macOS:** Run `sudo sentineledge-diag` in the terminal.
    
3.  **Output:** Provide the resulting `.zip` file to the support representative.
    

* * *

## Summary

# 

Most issues can be resolved by verifying network connectivity, checking for software conflicts, or adjusting policy exclusions. For further assistance, refer to the **SentinelEdge Admin Portal** for real-time system health status.