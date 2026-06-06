# Slow Computer Performance

## How Do I Write Knowledge Base Articles?

When writing a knowledge base article, I use a clear and step-by-step structure so both end users and IT technicians can follow it easily.

1. Define the purpose of the article
Explain what issue the article covers and who should use it.

2. List common symptoms
Include the signs users or technicians may see, such as slow startup, freezing, high CPU usage, high memory usage, or delayed response.

3. Add quick checks first
Start with the easiest troubleshooting steps, such as restarting the computer, closing unused applications, checking available storage, or confirming whether the issue affects one user or multiple users.

4. Provide step-by-step troubleshooting instructions
Write the troubleshooting process in a clear order, starting with basic checks and moving toward more technical steps.

5. Include commands, screenshots, and expected results
Add useful commands, screenshots, examples of error messages, and explain what normal or abnormal results look like.

6. Add resolution steps
Explain what usually fixes the issue and how to apply the fix safely.

7. Include verification steps
Explain how to confirm the issue is resolved, such as checking performance after reboot, opening applications, or confirming with the user.

8. Add escalation criteria
Explain when the issue should be escalated to Tier 2, desktop support, system administrator, vendor, or another department.

9. Add documentation notes
Include what the technician should write in the ticket, such as the issue, troubleshooting steps, resolution, and user confirmation.

10. Keep the article clear and easy to update
Use simple language, headings, bullet points, and update the article when procedures, tools, or systems change.

---

## Purpose

This article provides basic troubleshooting steps for resolving slow computer performance issues on Windows devices.

## Common Symptoms

- Computer is slow to start
- Applications take a long time to open
- Computer freezes or becomes unresponsive
- Mouse or keyboard input is delayed
- High CPU usage
- High memory usage
- High disk usage
- Web browser is slow
- Device becomes slow after login
- System performance gets worse during normal work

## Quick Checks

1. Ask the user when the issue started.
2. Confirm whether the issue affects one device or multiple devices.
3. Ask if the issue happens all the time or only with specific applications.
4. Restart the computer.
5. Close unused applications and browser tabs.
6. Check if Windows updates or application updates are running.
7. Check available storage space.
8. Confirm whether the device is connected to VPN, external drives, or docking stations.

## Troubleshooting Steps

### 1. Confirm the Scope of the Issue

Ask the user:

- When did the computer become slow?
- Is the whole computer slow or only one application?
- Does the issue happen after login, during startup, or during specific tasks?
- Did the issue start after an update or software installation?
- Are other users or devices experiencing the same issue?

If only one application is slow, troubleshoot that application first.  
If the entire computer is slow, continue with system performance checks.

### 2. Restart the Computer

Ask the user to restart the computer.

A restart can clear temporary memory issues, stuck background processes, pending updates, or locked system resources.

After restarting, ask the user to log in and test normal work activities again.

### 3. Check Task Manager

Open Task Manager and review system usage.

Check:

- CPU usage
- Memory usage
- Disk usage
- Network usage
- Startup applications
- Applications marked as “Not Responding”

If CPU, memory, or disk usage is consistently high, identify which process is using the most resources.

Common causes include:

- Too many browser tabs
- Large applications
- Background updates
- Sync tools
- Antivirus scans
- Old or low-resource hardware

### 4. Close Unused Applications

Close applications the user is not actively using.

Examples:

- Extra browser windows or tabs
- Unused Microsoft Office files
- Streaming applications
- Background tools
- Applications showing “Not Responding”

After closing unused applications, check whether performance improves.

### 5. Check Available Storage

Open File Explorer and check available space on the C: drive.

Low disk space can cause slow performance.

Recommended checks:

- Confirm available storage
- Empty Recycle Bin if appropriate
- Remove unnecessary downloads if approved
- Move large files to approved storage location
- Run Disk Cleanup if allowed by company policy

Do not delete user files without user approval.

### 6. Check Startup Applications

Open Task Manager and go to the Startup apps tab.

Review applications that start automatically when the user logs in.

Disable unnecessary startup applications only if allowed by company policy.

Common examples may include:

- Chat applications
- Cloud sync tools
- Updaters
- Printer utilities
- Vendor tools

After changing startup apps, restart the computer and test performance again.

### 7. Check for Windows Updates

Check if Windows updates are installing, downloading, or waiting for restart.

Pending updates can slow down a device.

Steps:

1. Open Settings.
2. Go to Windows Update.
3. Check update status.
4. Install or restart only if approved by company policy.

After updates are complete, restart the computer and test performance again.

### 8. Check Browser Performance

If the user mainly reports slow web browsing, check the browser.

Possible steps:

- Close unused tabs
- Clear browser cache
- Disable unnecessary extensions
- Test another browser
- Check internet connection
- Confirm whether the issue happens on one website or all websites

If only one website is slow, the issue may be with that website or service.

### 9. Check for Malware or Security Alerts

If the computer suddenly becomes slow, check for security alerts.

Look for:

- Antivirus warnings
- Unknown applications
- Suspicious browser pop-ups
- Unusual startup programs
- Unexpected CPU or disk usage

Follow company security procedures before removing software or running scans.

Escalate to the security team if malware or compromise is suspected.

### 10. Check Device Health and Hardware Limits

If the device is older or has limited hardware resources, performance may be affected by normal workload.

Check:

- RAM amount
- Disk type, such as HDD or SSD
- Battery health for laptops
- Device age
- Number of applications required for the user’s role

If hardware is not sufficient for the user’s workload, document the issue and escalate for review.

## Escalation Criteria

Escalate the issue to Tier 2, desktop support, system administrator, or security team if:

- The device remains slow after basic troubleshooting
- CPU, memory, or disk usage stays extremely high
- The issue affects multiple users or devices
- Malware or suspicious activity is suspected
- The computer frequently freezes or crashes
- The device has hardware errors
- The hard drive may be failing
- The user cannot complete critical work
- Performance issues started after a company-wide update
- Hardware upgrade or replacement may be needed

## Documentation Example

User reported that their Windows laptop was running slowly after login and applications were taking several minutes to open. Confirmed the issue affected the whole computer, not just one application. Opened Task Manager and found high memory usage with multiple browser tabs and several startup applications running. Closed unused applications, disabled unnecessary startup apps according to company policy, and restarted the computer. After reboot, the user confirmed applications opened faster and normal work performance improved.

## Resolution

Issue resolved after closing unused applications, reviewing startup apps, and restarting the computer.

## Verification

Confirmed the computer restarted successfully. User opened browser, email, and Microsoft Office applications without delay. User confirmed system performance improved.

## Prevention / Notes

- Encourage users to restart their computers regularly.
- Keep Windows and applications updated according to company policy.
- Avoid keeping too many browser tabs and applications open at the same time.
- Monitor recurring performance issues by device, user, application, and location.
- Document high CPU, memory, or disk usage in the ticket.
- Escalate repeated slow performance issues for hardware or system review.
