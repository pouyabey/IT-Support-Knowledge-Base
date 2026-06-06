# Printer Not Printing – Troubleshooting Guide

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
