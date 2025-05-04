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

## Key Findings
- Multiple failed login attempts were recorded.
- Failure reason: account failed to logon

## Outcome
This lab provided practival experience with:
- Identifying critical security events
- Using Powershell to filter logs
- Interpreting forensice log details from Windows environments

  ## Author
  Janessa Reed

