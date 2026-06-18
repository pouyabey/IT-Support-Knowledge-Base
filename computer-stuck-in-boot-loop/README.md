# Computer Stuck in Boot Loop

## Purpose

This article provides basic troubleshooting steps for Windows computers that are stuck in a boot loop.

A boot loop happens when a computer repeatedly restarts and cannot successfully load Windows.

## Common Symptoms

- Computer keeps restarting
- Windows does not reach the login screen
- Device shows Automatic Repair
- Computer freezes during startup
- User sees a spinning circle for a long time
- Issue started after an update, driver change, or hardware change

Screenshot: boot-loop-loading-screen.png

## Quick Checks

1. Ask when the boot loop started.
2. Ask if the issue started after a Windows update, driver update, software installation, or hardware change.
3. Confirm whether the computer reaches the login screen.
4. Check if the computer enters Automatic Repair.
5. Ask if any error message or stop code appears.
6. Disconnect unnecessary external devices.
7. Confirm whether the issue affects one device or multiple devices.

## Troubleshooting Steps

### 1. Open Automatic Repair

Windows may open Automatic Repair automatically after several failed startup attempts.

If it does not open:

1. Turn on the computer.
2. When the Windows logo or spinning dots appear, hold the power button until the device turns off.
3. Repeat this 2 to 3 times. Alternatively, connect a Windows recovery USB or Windows installation USB,
press F11 during startup, select the USB drive, and choose Repair your computer.
4. Wait for Preparing Automatic Repair or Diagnosing your PC.
5. Select Advanced options.

Screenshot: [windows-automatic-repair-screen.png](screenshots/windows-automatic-repair-screen-01.png)
Screenshot: [windows-automatic-repair-screen.png](screenshots/windows-automatic-repair-screen-02.png)
Screenshot: [windows-automatic-repair-screen.png](screenshots/windows-automatic-repair-screen-03.png)

Expected result:
The computer opens the Windows recovery screen.

Note: To reach Windows Recover Enviornment when Windows boots normally: 

1. Open Start Menu.
2. Search for Command Prompt.
3. Right-click Command Prompt.
4. Select Run as administrator.
5. Type and press enter:

shutdown /r /o /f /t 0


### 2. Open Advanced Options

From the Automatic Repair screen:

1. Select Advanced options.
2. Select Troubleshoot.
3. Select Advanced options.

Screenshot: advanced-options-screen.png

Expected result:
The Windows Recovery Environment opens and shows troubleshooting options.

### 3. Run Startup Repair

Startup Repair can fix some startup problems automatically.

Steps:

1. Go to Advanced options.
2. Select Startup Repair.
3. Follow the prompts.
4. Restart the computer and test.

Screenshot: startup-repair-option.png

Expected result:
Windows attempts to repair startup problems automatically.

If Startup Repair works, confirm Windows boots normally.

If Startup Repair does not fix the issue, continue troubleshooting.

### 4. Boot into Safe Mode

If Startup Repair does not fix the issue, try Safe Mode.

Steps:

1. Go to Advanced options.
2. Select Startup Settings.
3. Select Restart.
4. Press 4 for Safe Mode or 5 for Safe Mode with Networking.

Screenshot: safe-mode-startup-settings.png

Expected result:
Windows starts with basic drivers and services.

Use Safe Mode to remove recent software, check Device Manager, roll back drivers if approved, or collect logs.

### 5. Remove Recent Updates or Drivers

If the computer boots into Safe Mode, remove the recent update or roll back the recent driver if allowed by company policy.

To remove a Windows update:

1. Open Settings.
2. Go to Windows Update > Update history.
3. Select Uninstall updates.
4. Choose the most recent update.
5. Click Uninstall.
6. Restart the computer normally.

To roll back a driver:

1. Right-click Start.
2. Open Device Manager.
3. Check the device category related to the recent change.

Examples:
- Display adapters
- Network adapters
- Storage controllers
- Disk drives
- Universal Serial Bus controllers
- System devices

4. Right-click the suspected device.
5. Select Properties.
6. Go to the Driver tab.
7. Check the Driver Date and Driver Version.
8. Click Roll Back Driver if the option is available.
9. Restart the computer normally.

Expected result:
The previous driver version is restored and the computer boots normally.

Note:
If Roll Back Driver is grayed out, Windows may not have a previous driver version available. Document the issue and escalate according to company policy.

### 6. Check Disk Health

If storage issues are suspected, open Command Prompt as Administrator and run:

chkdsk C:

Screenshot: command-prompt-chkdsk.png

Expected result:
Windows checks the drive and reports whether file system errors were found.

Note:
If Windows is running normally, you can also run:

chkdsk C: /scan

This performs an online scan. However, this command may not work in Safe Mode because some required services may not be running.

If disk errors are found, document the result and escalate or follow company policy before running repair commands such as:

chkdsk C: /f
chkdsk C: /r

### 7. Disconnect External Devices

Disconnect unnecessary external devices and restart the computer.

Examples:

- USB drives
- External hard drives
- Docking station
- Printers
- Card readers
- External monitors
- Headsets

Expected result:
If the computer boots normally, reconnect devices one at a time to identify the possible cause.

### 8. Check BIOS or Boot Order

If the computer is trying to boot from the wrong device, check the boot order.

Check for:

- USB drive selected as the first boot device
- Missing internal drive
- Incorrect boot mode
- Recent BIOS or firmware change

Screenshot: bios-boot-order-screen.png

Expected result:
The internal drive is detected and selected as the correct boot device.

Do not change BIOS settings unless authorized.

## Escalation Criteria

Escalate to Tier 2, desktop support, system administrator, hardware support, vendor support, or security team if:

- The computer cannot boot into Windows
- The computer cannot boot into Safe Mode
- Startup Repair fails
- Disk errors are detected
- The internal drive is not detected
- Multiple devices are affected
- Hardware damage is suspected
- Malware or compromise is suspected
- User data needs recovery
- The user needs a loaner device

## Documentation Example

User reported that the laptop kept restarting and could not reach the Windows login screen. Confirmed the issue started after a recent Windows update. The device entered Automatic Repair. Ran Startup Repair, but the issue continued. Booted into Safe Mode and removed the latest quality update according to company policy. Restarted the laptop and confirmed Windows loaded normally. Documented the symptoms, recent update, troubleshooting steps, and user confirmation.

Screenshot: ticket-documentation-example.png

## Resolution

Issue resolved after removing the latest Windows quality update and restarting the computer.

## Verification

Confirmed the device booted into Windows successfully. User logged in and opened normal work applications without another restart during the test period.

## Notes

- Ask users when the boot loop started.
- Document recent updates, drivers, software, and hardware changes.
- Do not repeatedly restart the device without investigation.
- Use Startup Repair and Safe Mode for basic troubleshooting.
- Check disk health if storage issues are suspected.
- Follow company policy before uninstalling updates or drivers.
- Escalate repeated boot loop issues.
