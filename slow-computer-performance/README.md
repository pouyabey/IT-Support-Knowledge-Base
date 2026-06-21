# Slow Computer Performance

## How I Write Knowledge Base Articles

1. Define the purpose and audience
2. List common symptoms
3. Start with quick basic checks
4. Provide clear step-by-step troubleshooting
5. Add screenshots, commands, and expected results
6. Include resolution and verification steps
7. Add escalation criteria
8. Include ticket documentation notes
9. Keep the article simple, organized, and easy to update

---
### It is recommended to include screenshots in Knowledge Base articles. However, since these documents are mainly for my personal reference, I prefer to keep them simple and avoid adding screenshots. Instead, I create a video for each knowledge base article and include it in my video portfolio:

### https://www.youtube.com/@pouyabeyranvand1688
---


## Purpose
This article provides basic troubleshooting steps for a Windows computer that is running slowly.

## Scenario
A user reports that their PC is very slow. The issue may happen during startup, after login, when opening applications, while using the browser, or during general computer use.

## Common Symptoms
- Computer takes a long time to start
- Applications open slowly
- Browser is slow or freezes
- Mouse or keyboard response is delayed
- Disk usage stays high
- CPU or memory usage is high
- Computer freezes or becomes unresponsive
- User reports the issue started after an update or new software installation

## Possible Causes
- Long system uptime
- Too many startup apps
- High CPU, memory, or disk usage
- Low disk space
- Pending or failed Windows updates
- Malware or unwanted software
- Browser extensions or too many browser tabs
- Corrupted system files
- Disk errors or failing hard drive
- Low RAM or older hardware
- Network slowness affecting cloud apps or websites

## Troubleshooting Steps

1. **Confirm the issue with the user.**
   - Ask when the issue started.
   - Ask if the computer is slow all the time or only when opening specific apps.
   - Ask if the issue started after an update, new software installation, or restart.
   - Ask if other users or devices are having the same issue.

2. **Check system uptime.**
   - Open Task Manager.
   - Go to Performance > CPU.
   - Check Uptime.
   - If uptime is very high, a restart may help clear stuck processes and refresh system resources.

   Command option:

   `systeminfo | find "System Boot Time"`

3. **Restart the computer.**
   - Restart the computer if the uptime is high, updates are pending, or the system has not been restarted recently.
   - A restart can clear stuck processes, refresh system resources, and complete pending updates.

   Command option:

   `shutdown /r /t 0`

4. **Check Task Manager for high usage.**
   - Press Ctrl + Shift + Esc.
   - Go to the Processes tab.
   - Sort by CPU.
   - Sort by Memory.
   - Sort by Disk.
   - Look for apps using unusually high resources.

5. **Check startup apps.**
   - Open Task Manager.
   - Go to Startup apps.
   - Disable unnecessary startup apps if approved.

6. **Check available storage.**
   - Open File Explorer.
   - Go to This PC.
   - Check the C: drive free space.
   - If the C: drive is almost full, Windows may become slow because it needs free space for temporary files, updates, and normal system operations.

   Command option:

   `wmic logicaldisk get size,freespace,caption`

7. **Clean temporary files.**
   - Open Run with Windows + R.
   - Type:

   `cleanmgr`

   - Select the C: drive.
   - Remove temporary files, recycle bin files, and other unnecessary files.

   Another option:

   `Settings > System > Storage > Temporary files`

8. **Check Windows Updates.**
   - Go to:

   `Settings > Windows Update`

   - Check if updates are pending.
   - Install important updates if needed.
   - Restart the computer after updates.

   Command option:

   `control update`

9. **Check for malware or unwanted software.**
   - Open Windows Security.
   - Go to Virus & threat protection.
   - Run a Quick scan.
   - If needed, run a Full scan.

   Command option:

   `windowsdefender:`

   PowerShell option:

   `Start-MpScan -ScanType QuickScan`

10. **Check installed apps.**
   - Go to:

   `Settings > Apps > Installed apps`

   - Look for recently installed or suspicious apps.
   - Remove unnecessary software only if approved.

   Command option:

   `appwiz.cpl`

11. **Check browser performance.**
   - Check the number of open tabs.
   - Disable unnecessary browser extensions.
   - Clear browser cache if needed.
   - Test another browser.
   - If only browser performance is slow, the issue may be browser-related instead of full system slowness.

12. **Check disk health.**
   - Open Command Prompt as Administrator.
   - Run:

   `chkdsk C:`

   - Check disk status:

   `wmic diskdrive get status`

   PowerShell option:

   `Get-PhysicalDisk`

13. **Check system files.**
   - Open Command Prompt as Administrator.
   - Run:

   `sfc /scannow`

   - If system file issues continue, run:

   `DISM /Online /Cleanup-Image /RestoreHealth`

14. **Check network-related slowness.**
   - If only websites or cloud apps are slow, test the network.
   - Run:

   `ping 8.8.8.8`

   `ping google.com`

   `ipconfig /all`

   - If the computer itself is not slow but websites or cloud apps are slow, the issue may be related to network connectivity or DNS.

15. **Check hardware specifications.**
   - Open System Information.
   - Run:

   `msinfo32`

   - Check:
     - Processor
     - Installed RAM
     - Windows version
     - System model

   - If the computer has low RAM, an older CPU, or an HDD instead of an SSD, the system may be slow because of hardware limitations.

16. **Check Event Viewer.**
   - Open Run with Windows + R.
   - Type:

   `eventvwr.msc`

   - Check:
     - Windows Logs > System
     - Windows Logs > Application

   - Look for disk errors, app crashes, driver errors, or update failures.

17. **Test performance after each fix.**
   - Restart the computer.
   - Open common apps.
   - Open the browser.
   - Check Task Manager again.
   - Ask the user if performance improved.

18. **Escalate if the issue continues.**
   - Escalate the ticket if:
     - Disk usage stays at 100%
     - Hard drive health looks bad
     - RAM is too low for normal work
     - System files cannot be repaired
     - Malware is detected but cannot be removed
     - The computer is very old or hardware upgrade is needed
     - The issue affects multiple users or devices

## Resolution
Document what fixed the issue. Examples may include disabling startup apps, freeing disk space, completing Windows updates, removing unwanted software, fixing corrupted system files, or identifying hardware limitations.

## Notes
A slow PC issue can be caused by software, storage, updates, malware, browser problems, network issues, or hardware limitations. Start with simple checks first before moving to deeper troubleshooting.
- Escalate repeated slow performance issues for hardware or system review.
