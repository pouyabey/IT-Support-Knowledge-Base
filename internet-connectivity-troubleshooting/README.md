# Internet Connectivity Troubleshooting

## How Do I Write Knowledge Base Articles?

When writing a knowledge base article, I use a clear and step-by-step structure so both end users and IT technicians can follow it easily.

1. Define the purpose of the article
Explain what issue the article covers and who should use it.

2. List common symptoms
Include the signs users or technicians may see, such as error messages, no internet access, slow connection, or application errors.

3. Add quick checks first
Start with the easiest troubleshooting steps, such as restarting the device, checking cables, confirming Wi-Fi connection, or verifying basic settings.

4. Provide step-by-step troubleshooting instructions
Write the troubleshooting process in a clear order, starting with basic checks and moving toward more technical steps.

5. Include commands, screenshots, and expected results
Add useful commands, screenshots, examples of error messages, and explain what normal or abnormal results look like.

6. Add resolution steps
Explain what usually fixes the issue and how to apply the fix safely.

7. Include verification steps
Explain how to confirm the issue is resolved, such as testing internet access, opening a website, printing a test page, or confirming with the user.

8. Add escalation criteria
Explain when the issue should be escalated to Tier 2, the network team, system administrator, vendor, or another department.

9. Add documentation notes
Include what the technician should write in the ticket, such as the issue, troubleshooting steps, resolution, and user confirmation.

10. Keep the article clear and easy to update
Use simple language, headings, bullet points, and update the article when procedures, tools, or systems change.

---

## Purpose

This article provides basic troubleshooting steps for resolving common internet connectivity issues on Windows devices.

## Common Symptoms

- No internet access
- Connected to Wi-Fi but websites do not load
- Ethernet connected but no network access
- Slow or intermittent connection
- DNS error in browser
- “No Internet, Secured” message on Wi-Fi

## Quick Checks

1. Confirm whether the issue affects one user or multiple users.
2. Check if the device is connected to the correct Wi-Fi network or Ethernet port.
3. Restart the browser or affected application.
4. Reboot the computer.
5. If multiple users are affected, restart the modem/router or escalate to the network team.

## Troubleshooting Steps

### 1. Check Wi-Fi or Ethernet Connection

- Make sure Wi-Fi is turned on.
- Confirm the user is connected to the correct SSID.
- Check Wi-Fi signal strength.
- If using Ethernet, confirm the cable is fully connected.
- Try a different Ethernet cable or port if available.

### 2. Verify IP Configuration

Open Command Prompt and run:

ipconfig /all

Check for:

- Valid IPv4 address
- Default gateway
- DNS server
- No APIPA address such as 169.254.x.x

If the device has a 169.254.x.x address, it may not be receiving an IP address from DHCP.

### 3. Test Local Network Connectivity

Run:

ping 127.0.0.1

If successful, test the default gateway:

ping <default-gateway>

If the gateway does not respond, the issue may be related to Wi-Fi, Ethernet, DHCP, or the local network.

### 4. Test Internet Connectivity

Run:

ping 8.8.8.8

If this works but websites do not load, the issue may be DNS-related.

### 5. Test DNS Resolution

Run:

nslookup google.com

If DNS fails, try flushing the DNS cache:

ipconfig /flushdns

Then test the website again.

### 6. Renew IP Address

If the device has an invalid IP address or no internet access, run:

ipconfig /release
ipconfig /renew

After renewing the IP address, test internet access again.

### 7. Restart Network Adapter

If the issue continues:

1. Open Settings.
2. Go to Network & Internet.
3. Disable the Wi-Fi or Ethernet adapter.
4. Wait a few seconds.
5. Enable the adapter again.

You can also restart the adapter from Control Panel or Device Manager.

## Escalation Criteria

Escalate the issue to Tier 2 or the network team if:

- Multiple users are affected
- The default gateway is unreachable
- DHCP is not assigning IP addresses
- DNS servers are unreachable
- The issue occurs in only one office area or access point
- A switch, router, firewall, or ISP outage is suspected
- The issue continues after basic troubleshooting

## Documentation Example

User reported no internet access while connected to office Wi-Fi. Confirmed the device was connected to the correct SSID. Ran ipconfig /all and verified the device had a valid IP address and default gateway. Ping to the gateway was successful, but nslookup failed. Flushed DNS cache and renewed the IP address. User confirmed websites loaded successfully after troubleshooting.

## Resolution

Issue resolved after flushing DNS cache and renewing the IP address.

## Prevention / Notes

- Keep network drivers updated.
- Document recurring issues by device, user, location, or access point.
- Report repeated DHCP or DNS issues to the network team.
- Confirm whether outages affect one device, one area, or the entire office before escalating.
