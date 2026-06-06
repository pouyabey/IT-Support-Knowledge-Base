# Application Not Responding

## How Do I Write Knowledge Base Articles?

When writing a knowledge base article, I use a clear and step-by-step structure so both end users and IT technicians can follow it easily.

1. Define the purpose of the article
Explain what issue the article covers and who should use it.

2. List common symptoms
Include the signs users or technicians may see, such as error messages, frozen screens, slow performance, or application crashes.

3. Add quick checks first
Start with the easiest troubleshooting steps, such as waiting a few seconds, checking if the whole computer is frozen, restarting the application, or rebooting the device.

4. Provide step-by-step troubleshooting instructions
Write the troubleshooting process in a clear order, starting with basic checks and moving toward more technical steps.

5. Include commands, screenshots, and expected results
Add useful commands, screenshots, examples of error messages, and explain what normal or abnormal results look like.

6. Add resolution steps
Explain what usually fixes the issue and how to apply the fix safely.

7. Include verification steps
Explain how to confirm the issue is resolved, such as reopening the application, testing normal functions, or confirming with the user.

8. Add escalation criteria
Explain when the issue should be escalated to Tier 2, the application owner, system administrator, vendor, or another department.

9. Add documentation notes
Include what the technician should write in the ticket, such as the issue, troubleshooting steps, resolution, and user confirmation.

10. Keep the article clear and easy to update
Use simple language, headings, bullet points, and update the article when procedures, tools, or systems change.

---

## Purpose

This article provides basic troubleshooting steps for resolving issues when an application freezes, stops responding, crashes, or becomes slow on a Windows device.

## Common Symptoms

- Application freezes
- Application shows “Not Responding”
- Application crashes or closes unexpectedly
- User cannot click inside the application
- Application is slow to open or respond
- Computer becomes slow when the application is open
- Error message appears when launching the application
- Application opens but specific features do not work

## Quick Checks

1. Ask the user what application is affected.
2. Confirm whether the issue affects one application or multiple applications.
3. Ask when the issue started.
4. Check if the user recently installed updates, changed settings, or opened a large file.
5. Confirm whether other users are experiencing the same issue.
6. Ask the user to wait a few seconds before force-closing the application.
7. Save any work if possible before restarting the application.

## Troubleshooting Steps

### 1. Confirm the Scope of the Issue

Ask the user:

- What application is not responding?
- Does the issue happen every time or only sometimes?
- Is the whole computer frozen or only one application?
- Are other users having the same issue?
- Did the issue start after an update, login change, or file download?

If only one application is affected, continue troubleshooting the application.  
If the whole computer is frozen, check system performance and consider rebooting the device.

### 2. Wait and Check for Recovery

If the application temporarily stops responding, wait 30 to 60 seconds.

Some applications may freeze while loading large files, syncing data, printing, or processing updates.

If the application starts responding again, ask the user to save their work and continue monitoring.

### 3. Close and Reopen the Application

If the application remains frozen:

1. Try closing the application normally.
2. If it does not close, open Task Manager.
3. Select the affected application.
4. Click End Task.
5. Reopen the application.

Warning: Force-closing an application may cause unsaved work to be lost.

### 4. Check Task Manager

Open Task Manager and review:

- CPU usage
- Memory usage
- Disk usage
- Application status
- Background processes

If CPU, memory, or disk usage is very high, the issue may be related to system resources.

If the application shows “Not Responding,” end the task and reopen it.

### 5. Restart the Computer

If closing and reopening the application does not fix the issue, restart the computer.

A reboot can clear temporary issues with memory, background processes, pending updates, or locked application files.

After the restart, ask the user to open the application again and test normal use.

### 6. Check for Updates

If the issue continues, check for available updates.

Check:

- Windows updates
- Microsoft Store updates if applicable
- Application updates
- Browser updates if the issue is web-based
- Plugin or add-in updates if the application uses add-ins

Install updates only if approved by company policy.

### 7. Check Internet or Network Connection

Some applications may stop responding if they depend on internet access, shared drives, cloud sync, or a company server.

Check:

- Wi-Fi or Ethernet connection
- VPN connection if required
- Access to shared drives
- Access to the application website or server
- Whether other users can access the same application

If the application requires VPN, confirm the user is connected to VPN before testing again.

### 8. Clear Temporary Files or Cache

If the application uses cached data, clearing the cache may help.

Examples:

- Clear browser cache for web applications
- Clear Microsoft Teams cache if Teams is freezing
- Clear temporary files if the device is running low on space
- Restart the application after clearing cache

Follow company procedures before deleting application-specific files.

### 9. Disable Add-ins or Extensions

If the issue happens in an application that uses add-ins or extensions, test with add-ins disabled.

Examples:

- Outlook add-ins
- Excel add-ins
- Browser extensions
- PDF plugins

If the application works after disabling add-ins, re-enable them one at a time to identify the cause.

### 10. Repair or Reinstall the Application

If the issue continues after basic troubleshooting, repair or reinstall the application if allowed.

Possible actions:

- Run application repair
- Uninstall and reinstall the application
- Remove corrupted application settings
- Reinstall from the company software portal
- Confirm the user has the correct license or access

Follow company policy before uninstalling or reinstalling software.

## Escalation Criteria

Escalate the issue to Tier 2, the application owner, system administrator, or vendor if:

- Multiple users are affected
- The application crashes repeatedly after troubleshooting
- The application shows a licensing or access error
- The application depends on a server that may be down
- The issue started after a company-wide update
- The user cannot complete critical work
- Error logs are needed for deeper troubleshooting
- Repair or reinstall does not resolve the issue
- The issue may involve permissions, profile corruption, or backend services

## Documentation Example

User reported that Microsoft Excel stopped responding when opening a large spreadsheet. Confirmed that only Excel was affected and other applications were working normally. Opened Task Manager and found Excel showing “Not Responding” with high memory usage. Ended the Excel task after confirming the user had no unsaved work. Reopened Excel and tested with a smaller file successfully. Restarted the computer and asked the user to reopen the original file. User confirmed Excel opened successfully after reboot.

## Resolution

Issue resolved after ending the unresponsive application and restarting the computer.

## Verification

Confirmed the application opened successfully after reboot. User tested normal application functions and confirmed the issue was resolved.

## Prevention / Notes

- Encourage users to save work frequently.
- Keep applications updated according to company policy.
- Restart the device regularly if performance issues occur.
- Avoid opening very large files on low-resource devices.
- Document recurring application issues by user, device, application version, and error message.
- Escalate repeated crashes for deeper review.
