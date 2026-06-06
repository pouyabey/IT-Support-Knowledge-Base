# Printer Not Printing – Troubleshooting Guide


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
This knowledge base article provides basic troubleshooting steps for situations where a user is unable to print from their computer.

## Applies To
- Windows computers
- Network printers
- USB printers
- Office printers
- Print queue issues

## Common Symptoms
- Printer does not respond
- Print job stays stuck in the queue
- Printer shows “Offline”
- Printer prints blank pages
- User receives a printer error message
- Printer is powered on but does not print

## Troubleshooting Steps

### 1. Confirm the Basic Printer Status
- Check that the printer is powered on.
- Make sure there are no warning lights or error messages.
- Confirm the printer has paper and toner or ink.
- Check for paper jams.

### 2. Verify the Printer Connection
For USB printers:
- Make sure the USB cable is securely connected to both the printer and the computer.

For network printers:
- Confirm the printer is connected to the network.
- Check if the printer has a valid IP address.
- Try pinging the printer IP address from the user’s computer.

### 3. Check the Print Queue
- Open Settings > Bluetooth & devices > Printers & scanners.
- Select the printer.
- Open the print queue.
- Cancel any stuck or failed print jobs.
- Ask the user to try printing again.

### 4. Confirm the Correct Printer Is Selected
- Make sure the user is printing to the correct printer.
- Set the correct printer as the default printer if needed.
- Check that the printer is not listed as Offline.

### 5. Restart the Printer and Computer
- Turn the printer off and back on.
- Restart the user’s computer.
- Try printing a test page.

### 6. Restart the Print Spooler Service
If print jobs are stuck:
- Open Services.
- Find Print Spooler.
- Right-click and select Restart.
- Try printing again.

### 7. Reinstall or Update the Printer Driver
If the printer still does not print:
- Remove the printer from the computer.
- Download or install the correct printer driver.
- Add the printer again.
- Print a test page.

## Resolution
The issue is resolved when the user can successfully print a test page or document from their computer.

## Verification
Confirm with the user that:
- The correct printer is selected.
- The document prints successfully.
- No print jobs remain stuck in the queue.
- The printer status shows as online.

## Escalation
Escalate the ticket if:
- The printer cannot be reached on the network.
- Multiple users are affected.
- The printer has a hardware error.
- The driver installation fails.
- The printer continues to go offline after troubleshooting.

## Documentation Notes
When closing the ticket, include:
- User’s reported issue
- Printer name or IP address
- Troubleshooting steps completed
- Final resolution
- Verification with the user
