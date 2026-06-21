# User Cannot Access Internet While Other Devices Work


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

# https://www.youtube.com/@pouyabeyranvand1688



## Purpose
This article provides troubleshooting steps for a user who cannot access the internet while other devices on the same network are working.

## Scenario
A user reports that their computer cannot access the internet, but other websites or devices on the same network are working.

## Common Symptoms
- User cannot open websites
- Browser shows connection error
- Other users or devices can access the internet
- Wi-Fi or Ethernet may show connected
- Issue affects only one computer

## Possible Causes
- Wi-Fi or Ethernet connection issue
- Incorrect IP address configuration
- DNS issue
- Browser cache or proxy issue
- VPN issue
- Firewall or security software blocking access
- Network adapter problem

## Troubleshooting Steps

### 1. Confirm that other devices on the same network can access the internet.
   - Ask the user if other devices on the same Wi-Fi or network are working.
   - If other devices are working, focus on the affected computer.
   - If multiple devices are not working, check the router, switch, access point, or ISP.

### 2. Check physical connection or Wi-Fi connection.
   - If using Ethernet, make sure the cable is connected properly.
   - If using Wi-Fi, confirm the computer is connected to the correct network.
   - Disconnect and reconnect to the network if needed.

### 3. Test another website.
   - Try opening a different website.
   - This helps confirm whether the issue is with one website or general internet access.

### 4. Test with another browser.
   - Try Chrome, Edge, or Firefox.
   - If the internet works in another browser, the issue may be browser-related.

### 5. Restart the browser and computer.
   - Close and reopen the browser.
   - Restart the computer if the issue continues.

### 6. Check IP address configuration.
   - Open Command Prompt.
   - Run this command:

   ipconfig /all

   - Check for:
     - IPv4 Address
     - Subnet Mask
     - Default Gateway
     - DNS Servers

   - If the computer has an IP address starting with 169.254, it may not be getting an IP address from DHCP.
   - To release and renew the IP address, run:

   ipconfig /release

   ipconfig /renew

### 7. Test network connectivity with ping.
   - First, test the default gateway:

   ping [default-gateway-ip]

   Example:

   ping 192.168.1.1

   - If the gateway replies, the computer can communicate with the local network.
   - Next, test internet connectivity using a public IP address:

   ping 8.8.8.8

   - If ping 8.8.8.8 works, but websites do not open, the issue may be DNS-related.
   - If ping 8.8.8.8 fails, the issue may be network, firewall, gateway, or internet connection related.

### 8. Test DNS resolution.
   - Test if the computer can resolve a website name:

   nslookup google.com

   - You can also test with ping:

   ping google.com

   - If ping 8.8.8.8 works but ping google.com fails, DNS is likely the problem.

### 9. Flush DNS cache.
   - Open Command Prompt as Administrator.
   - Run this command:

   ipconfig /flushdns

   - Then test the website again.
   - If needed, also run:

   ipconfig /release

   ipconfig /renew

### 10. Check proxy and VPN settings.
   - Check if the user is connected to a VPN.
   - Disconnect the VPN and test internet access again.
   - Check proxy settings:
     Settings > Network & Internet > Proxy
   - Make sure no incorrect proxy is enabled unless required by the organization.

### 11. Disable and re-enable the network adapter.
   - Open Control Panel.
   - Go to:
     Control Panel > Network and Internet > Network Connections
   - Right-click the Wi-Fi or Ethernet adapter.
   - Click Disable.
   - Wait a few seconds.
   - Right-click again and click Enable.

   Command option:

   ncpa.cpl

### 12. Restart the router only if multiple users are affected.
   - Do not restart the router if only one user has the issue.
   - If multiple devices cannot access the internet, restart the router or escalate to network support.

### 13. Escalate if the issue continues.
   - Escalate the ticket if:
     - The computer cannot get a valid IP address
     - The default gateway is unreachable
     - DNS does not work after troubleshooting
     - The network adapter may be damaged
     - Firewall, security software, or company network policy may be blocking access
     - Multiple users are affected

## Resolution
Document what fixed the issue, such as DNS reset, proxy disabled, browser issue, or network adapter reset.

## Notes
If other devices are working, the problem is most likely related to the user's device, browser, DNS, VPN, proxy, or adapter settings.
