# Printer Is Offline or Not Printing

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

### It is recommended to include screenshots in Knowledge Base articles. However, since these documents are mainly for my personal reference, I prefer to keep them simple and avoid adding screenshots. Instead, I create a video for each knowledge base article and include it in my video portfolio:

### https://www.youtube.com/@pouyabeyranvand1688
--- 


## Purpose
This article provides basic troubleshooting steps for a printer that is showing offline or not printing.

## Scenario
A user reports that the printer is showing offline, print jobs are stuck, or documents are not printing.

## Common Symptoms
- Printer shows offline
- Print jobs stay in the queue
- Printer does not respond
- User cannot print from one computer
- Multiple users cannot print
- Printer prints slowly or partially
- Printer shows an error light or warning message

## Possible Causes
- Printer is powered off or disconnected
- Printer is not connected to the network
- Wrong default printer selected
- Print queue is stuck
- Print Spooler service issue
- Printer driver issue
- Paper jam, low paper, or low toner
- IP address changed
- Network or Wi-Fi issue
- Printer is paused or set to offline mode

## Troubleshooting Steps

1. **Confirm the issue with the user.**
   - Ask when the issue started.
   - Ask if the issue affects one user or multiple users.
   - Ask if the printer shows any error message.
   - Ask if the user can print to another printer.

2. **Check printer power and physical status.**
   - Make sure the printer is powered on.
   - Check for paper, toner, ink, or error lights.
   - Check for paper jams.
   - Restart the printer if needed.

3. **Check printer connection.**
   - If using USB, make sure the cable is connected properly.
   - If using Ethernet, check that the network cable is connected.
   - If using Wi-Fi, confirm the printer is connected to the correct wireless network.

4. **Check if the issue affects one user or multiple users.**
   - If only one user is affected, focus on that computer.
   - If multiple users are affected, check the printer, network connection, print server, or printer IP address.

5. **Check the default printer.**
   - Go to:

   `Settings > Bluetooth & devices > Printers & scanners`

   - Make sure the correct printer is selected.
   - Set the correct printer as default if needed.

6. **Check printer status.**
   - Open Run with Windows + R.
   - Type:

   `control printers`

   - Right-click the printer.
   - Check if the printer is paused or set to offline.
   - Uncheck:

   `Use Printer Offline`

   - Uncheck:

   `Pause Printing`

7. **Clear the print queue.**
   - Open:

   `control printers`

   - Right-click the printer.
   - Click:

   `See what's printing`

   - Cancel stuck print jobs.
   - Try printing again.

8. **Restart the Print Spooler service.**
   - Open Command Prompt as Administrator.
   - Run:

   `net stop spooler`

   `net start spooler`

   - Try printing again.

9. **Clear stuck spooler files if needed.**
   - Open Command Prompt as Administrator.
   - Run:

   `net stop spooler`

   - Open this folder:

   `C:\Windows\System32\spool\PRINTERS`

   - Delete the stuck files inside the folder.
   - Start the spooler again:

   `net start spooler`

10. **Check printer IP address.**
   - Print a network configuration page from the printer if available.
   - Compare the printer IP address with the IP address configured on the computer.

   To check the configured printer port:
   - Open:

   `control printers`

   - Right-click the printer.
   - Click Printer properties.
   - Go to the Ports tab.
   - Check the selected TCP/IP port.

11. **Ping the printer.**
   - Open Command Prompt.
   - Run:

   `ping [printer-ip-address]`

   Example:

   `ping 192.168.1.50`

   - If ping works, the computer can reach the printer on the network.
   - If ping fails, the issue may be network, printer IP, Wi-Fi, VLAN, firewall, or printer connection related.

12. **Remove and re-add the printer.**
   - Go to:

   `Settings > Bluetooth & devices > Printers & scanners`

   - Remove the printer.
   - Add the printer again.
   - Test printing.

13. **Check or reinstall the printer driver.**
   - If the printer still does not work, reinstall or update the printer driver.
   - Use the correct driver for the printer model.
   - In a company environment, use the approved driver or print server driver.

14. **Test printing from another application.**
   - Try printing from Notepad, Word, or a browser.
   - If printing works from one app but not another, the issue may be application-specific.

15. **Check Windows Updates if needed.**
   - Go to:

   `Settings > Windows Update`

   - Check for pending updates.
   - Restart the computer after updates if required.

16. **Escalate if the issue continues.**
   - Escalate the ticket if:
     - Multiple users cannot print
     - Printer is not reachable by IP
     - Printer has hardware errors
     - Printer driver reinstall does not fix the issue
     - Print server issue is suspected
     - Printer IP address or network configuration needs admin access

## Resolution
Document what fixed the issue. Examples may include restarting the Print Spooler, clearing the print queue, reconnecting the printer, correcting the printer IP address, disabling offline mode, or reinstalling the printer driver.

## Notes
If only one user cannot print, the issue is usually related to that computer, printer queue, printer settings, or driver. If multiple users cannot print, check the printer, network connection, IP address, or print server.


## My personal summary 
### Use IT Support Useful Commands repository, [IT Support Useful Commands](https://github.com/pouyabey/IT-support-useful-commands-)
### 1: Confirm the issue with user, check printer power, status, and connection 
- When the issue started, affected one user or multiple
- Wether the printer is powered on
- Run control printers for status, check toner
- Check USB and Ethernet connection

### 2: Check printer queue and restart spooler 
- Run control printers, check what is printing
- Net stop spooler, Net start spooler, Run servisec.msc
- Check printer IP in port tab, ping printer IP
- Remove and re-add the printer, update driver (Get latest update from vendor's official website)
- Check Windows update 





