# Windows-Security-Log-Analysis
# Cybersecurity Lab: Windows Security Log Analysis

## Objective
Analyze Windows Security logs to identify failed login attempts and gain hands-on experience with forensic log analysis.

## Tools used 
-Powershell
-Event Viewer
-Windows 11

## Method
1. Opened Event Viewer and filtered logs under `Security` by Event ID 4625 (failed logons).
2. Used Powershell to extract and save failed login events:
   ``` powershell
   Get-WinEvent -LogName Security | Where-Object {$_.Id -eq 4625} | Select-Object TimeCreated, Message | Out-File .\FailedLogins.txt
