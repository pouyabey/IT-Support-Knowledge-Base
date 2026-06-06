# BSOD Troubleshooting

## How Do I Write Knowledge Base Articles?

When writing a knowledge base article, I use a clear and step-by-step structure so both end users and IT technicians can follow it easily.

1. Define the purpose of the article
Explain what issue the article covers and who should use it.

2. List common symptoms
Include the signs users or technicians may see, such as blue screen errors, automatic restarts, stop codes, freezing, or boot failures.

3. Add quick checks first
Start with the easiest troubleshooting steps, such as asking for the stop code, checking recent changes, restarting the computer, and confirming whether the issue happened once or repeatedly.

4. Provide step-by-step troubleshooting instructions
Write the troubleshooting process in a clear order, starting with basic checks and moving toward more technical steps.

5. Include commands, screenshots, and expected results
Add useful commands, screenshots, stop code examples, Event Viewer notes, and explain what normal or abnormal results look like.

6. Add resolution steps
Explain what usually fixes the issue and how to apply the fix safely.

7. Include verification steps
Explain how to confirm the issue is resolved, such as confirming the computer boots normally, checking stability, and confirming with the user.

8. Add escalation criteria
Explain when the issue should be escalated to Tier 2, desktop support, system administrator, hardware support, vendor support, or security team.

9. Add documentation notes
Include what the technician should write in the ticket, such as the issue, stop code, troubleshooting steps, recent changes, resolution, and user confirmation.

10. Keep the article clear and easy to update
Use simple language, headings, bullet points, and update the article when procedures, tools, or systems change.

---

## Purpose

This article provides basic troubleshooting steps for Blue Screen of Death issues on Windows devices.

A Blue Screen of Death, also called a BSOD or stop error, happens when Windows encounters a serious system error and must restart to prevent further damage.

## Common Symptoms

- Blue screen error appears
- Computer restarts automatically
- Stop code appears on screen
- Device freezes before restarting
- Computer restarts during startup
- Computer enters automatic repair
- User reports repeated crashes
- Device crashes after update, driver change, or hardware change
- Error message says “Your device ran into a problem and needs to restart”

## Quick Checks

1. Ask the user if the BSOD happened once or repeatedly.
2. Ask the user to write down or take a picture of the stop code.
3. Ask what the user was doing when the BSOD occurred.
4. Check if there were recent changes, such as Windows updates, driver updates, new software, or new hardware.
5. Confirm whether the computer can boot into Windows.
6. Check if the issue affects one device or multiple devices.
7. If the computer boots normally, save important work and continue troubleshooting.
8. If the computer cannot boot, escalate or follow company recovery procedures.

## Troubleshooting Steps

### 1. Collect Basic Information

Ask the user:

- When did the blue screen happen?
- Did it happen once or multiple times?
- What stop code appeared?
- What application or task was running?
- Did the device recently install updates?
- Was new hardware connected?
- Was new software or a driver installed?
- Can the user log back into Windows?

Common stop codes may include:

- CRITICAL_PROCESS_DIED
- MEMORY_MANAGEMENT
- IRQL_NOT_LESS_OR_EQUAL
- SYSTEM_SERVICE_EXCEPTION
- PAGE_FAULT_IN_NONPAGED_AREA
- DRIVER_POWER_STATE_FAILURE
- INACCESSIBLE_BOOT_DEVICE

Do not guess the cause based only on the stop code. Document it and continue troubleshooting.

### 2. Restart and Confirm the Current Status

If the computer restarted and now works normally, ask the user to log in and test normal use.

Check:

- Can the user log in?
- Are applications opening normally?
- Is the device slow or unstable?
- Does the blue screen happen again?

If the BSOD happened only once and the device is stable, document the event and monitor.

If the BSOD repeats, continue troubleshooting.

### 3. Check Recent Changes

Review recent changes before the BSOD started.

Examples:

- Windows update
- Driver update
- New software installation
- New antivirus or security tool
- New printer or peripheral
- New docking station
- New RAM, storage, or hardware change
- BIOS or firmware update

If the issue started after a recent change, document the change and follow company policy before rolling back, uninstalling, or updating anything.

### 4. Check Windows Update

Open Settings and check Windows Update.

Steps:

1. Open Settings.
2. Go to Windows Update.
3. Check for pending updates.
4. Check if a restart is required.
5. Install updates only if approved by company policy.
6. Restart the computer if needed.

Some BSOD issues may be caused by outdated drivers or incomplete updates.

### 5. Check Device Manager

Open Device Manager and check for hardware or driver issues.

Look for:

- Yellow warning icons
- Disabled devices
- Unknown devices
- Recently changed drivers
- Display adapter issues
- Network adapter issues
- Storage controller issues

If a device has a warning icon, document it and update, roll back, or escalate according to company policy.

### 6. Run System File Checker

If the device can boot into Windows, open Command Prompt as Administrator and run:

sfc /scannow

Expected result:

- Windows Resource Protection did not find any integrity violations

Possible abnormal results:

- Windows found corrupt files and repaired them
- Windows found corrupt files but could not repair some of them

If corrupt files are found and repaired, restart the computer and test again.

### 7. Run DISM Health Check

If system corruption is suspected, run Command Prompt as Administrator and use:

DISM /Online /Cleanup-Image /CheckHealth

If needed and allowed by company policy, run:

DISM /Online /Cleanup-Image /RestoreHealth

After DISM completes, restart the computer and test again.

### 8. Check Event Viewer

Open Event Viewer to review recent system errors.

Steps:

1. Open Event Viewer.
2. Go to Windows Logs.
3. Select System.
4. Look for critical errors around the time of the BSOD.
5. Check for Kernel-Power, BugCheck, driver, disk, or hardware-related errors.

Document important event details, including:

- Date and time
- Source
- Event ID
- Error message
- Related driver or service if listed

Do not delete logs.

### 9. Check Disk Health

If the stop code or Event Viewer suggests storage issues, check disk health.

Open Command Prompt as Administrator and run:

chkdsk C: /scan

If disk errors are found, escalate or follow company policy before running repair commands.

Warning: Disk repair actions can take time and may require restart. Do not run repair commands without approval.

### 10. Check Memory Issues

If the stop code suggests memory problems, use Windows Memory Diagnostic if allowed.

Steps:

1. Search for Windows Memory Diagnostic.
2. Select Restart now and check for problems.
3. Allow the test to complete.
4. Review results after restart.

If memory errors are found, escalate to hardware support or vendor support.

### 11. Boot into Safe Mode if Needed

If Windows crashes during normal startup, Safe Mode may help with troubleshooting.

Use Safe Mode to:

- Remove recently installed software
- Disable problematic startup items
- Check Device Manager
- Roll back a driver if approved
- Collect logs

Escalate if the user cannot boot into Windows or Safe Mode.

### 12. Check for Overheating or Hardware Problems

BSOD issues can be caused by hardware problems.

Check for:

- Device overheating
- Fan not working
- Dust buildup
- Damaged laptop
- Liquid exposure
- Loose external devices
- Failing drive
- Memory issues
- Battery or power issues

Do not open the device unless authorized.

### 13. Remove External Devices

Disconnect unnecessary external devices and test again.

Examples:

- USB drives
- External hard drives
- Docking station
- Printers
- Card readers
- External monitors
- Headsets

If the BSOD stops after removing a device, reconnect devices one at a time to identify the possible cause.

### 14. Check Security Concerns

If the BSOD appears after suspicious activity, unknown software installation, or malware alerts, follow company security procedures.

Escalate to the security team if:

- Malware is suspected
- The device shows unusual behavior
- Security tools report threats
- Unknown software or scripts were installed
- The device crashes during antivirus scans

## Escalation Criteria

Escalate the issue to Tier 2, desktop support, system administrator, hardware support, vendor support, or security team if:

- BSOD happens repeatedly
- The computer cannot boot into Windows
- The computer cannot boot into Safe Mode
- Stop codes suggest driver, memory, disk, or hardware failure
- Event Viewer shows repeated critical errors
- SFC or DISM cannot repair system files
- Disk errors are detected
- Memory errors are detected
- The issue started after a company-wide update
- The issue affects multiple devices
- The device was dropped, overheated, or exposed to liquid
- Malware or compromise is suspected
- The user cannot complete critical work and needs a loaner device

## Documentation Example

User reported a blue screen error while using Microsoft Teams and Outlook. Asked the user to provide the stop code and confirmed the stop code was DRIVER_POWER_STATE_FAILURE. User reported the issue happened twice after connecting to a docking station. Confirmed the device could boot into Windows. Checked Windows Update and found a pending driver update. Reviewed Device Manager and found no warning icons. Disconnected the docking station and restarted the laptop. User worked for 30 minutes without another crash. Documented stop code, recent docking station use, troubleshooting steps, and user confirmation. Escalated to desktop support for docking station driver and firmware review.

## Resolution

Issue temporarily resolved after disconnecting the docking station and restarting the laptop. Escalated to desktop support for further driver and firmware review.

## Verification

Confirmed the device booted into Windows successfully. User opened normal work applications and used the laptop without another blue screen during the test period. User confirmed the device was stable after troubleshooting.

## Prevention / Notes

- Ask users to take a picture of the stop code when possible.
- Document the exact stop code and what the user was doing before the crash.
- Keep Windows, drivers, and firmware updated according to company policy.
- Avoid installing unapproved software or drivers.
- Monitor repeated BSOD issues by device, user, stop code, and recent changes.
- Escalate repeated crashes instead of repeatedly restarting the device without investigation.
