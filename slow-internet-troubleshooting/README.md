# Slow Internet Troubleshooting

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
This article provides basic troubleshooting steps for identifying why a user's internet connection is slow.

## Scenario
A user reports that the internet is slow. Websites may load slowly, video calls may freeze, cloud apps may be delayed, or downloads may take longer than expected.

## Common Symptoms
- Websites load slowly
- Video calls freeze or disconnect
- Downloads are slow
- Cloud apps are delayed
- Browser takes a long time to open pages
- Wi-Fi feels slower than usual
- Only one device is slow
- Multiple users report slow internet

## Possible Causes
- Weak Wi-Fi signal
- Network congestion
- ISP issue
- DNS issue
- VPN or proxy slowing traffic
- Background downloads or updates
- Cloud sync apps using bandwidth
- Incorrect IP, gateway, or DNS settings
- Browser issue
- Router, switch, firewall, or access point issue

## Troubleshooting Steps

1. **Ask who is affected.**
   - Ask if the issue affects only one user, multiple users, one device, or the entire network.
   - If only one device is affected, focus on that computer.
   - If multiple users are affected, check Wi-Fi, switch, router, firewall, ISP, or network congestion.

2. **Check Wi-Fi or Ethernet connection.**
   - Check if the user is connected through Wi-Fi or Ethernet.
   - Wi-Fi can be slow because of weak signal, distance from the access point, interference, or too many connected devices.
   - Ethernet is usually more stable.
   - If Ethernet is fast but Wi-Fi is slow, the issue is likely Wi-Fi related.

3. **Run a speed test.**
   - Run a speed test to check download speed, upload speed, and latency.
   - Compare the result with the expected internet speed.
   - If speed is low for multiple users, the issue may be network or ISP related.

4. **Ping a public IP address.**
   - Open Command Prompt.
   - Run:

   `ping 8.8.8.8`

   - This tests internet connectivity without depending on DNS.
   - Check for high latency or packet loss.
   - High ping time or packet loss can make the internet feel slow.

5. **Ping a website name.**
   - Run:

   `ping google.com`

   - This tests connectivity using a domain name.
   - If ping 8.8.8.8 works but ping google.com is slow or fails, DNS may be the problem.
   - Slow DNS can make websites take a long time to start loading.

6. **Test DNS resolution.**
   - Run:

   `nslookup google.com`

   - This checks whether the DNS server can translate a website name into an IP address.
   - If nslookup is slow or fails, websites may load slowly or not open at all.

7. **Check IP configuration.**
   - Run:

   `ipconfig /all`

   - Check:
     - IPv4 Address
     - Default Gateway
     - DNS Servers
     - DHCP status

   - A wrong DNS server can make websites slow to load.
   - A wrong default gateway can cause connection problems.
   - A 169.254.x.x IP address means the computer did not get a valid IP address from DHCP.
   - If the computer is using the wrong adapter or wrong network settings, internet speed or access may be affected.

8. **Check Task Manager for bandwidth usage.**
   - Press Ctrl + Shift + Esc.
   - Go to the Processes tab.
   - Click the Network column to sort applications by network usage.
   - Look for apps using high bandwidth, such as:
     - OneDrive
     - Windows Update
     - Browser downloads
     - Teams
     - Backup software
     - Cloud sync apps
     - Antivirus updates

   - If one app is using high network bandwidth, other apps may feel slow.

   More detailed option:

   `resmon`

   - Open Resource Monitor.
   - Go to the Network tab.
   - Review network activity by process.

9. **Check VPN and proxy settings.**
   - Check if the user is connected to a VPN.
   - Disconnect VPN temporarily and test again if allowed.
   - VPN can slow internet because traffic goes through another server.
   - Check proxy settings:

   `Settings > Network & Internet > Proxy`

   - A misconfigured or overloaded proxy can slow browsing.

10. **Check browser performance.**
   - Test another browser.
   - Check if too many tabs are open.
   - Disable unnecessary extensions.
   - Clear browser cache if needed.
   - If only one browser is slow, the issue may be browser-related.

11. **Decide where the issue is coming from.**
   - Device-side issue:
     - Only one computer is slow.
     - Check browser, VPN, proxy, background apps, malware, or network adapter.

   - Wi-Fi-side issue:
     - Wi-Fi is slow but Ethernet is fine.
     - Check signal strength, access point, interference, or distance.

   - DNS-side issue:
     - Ping to IP works, but websites or name resolution are slow.
     - Check DNS server settings and test with another DNS if approved.

   - ISP or network-side issue:
     - Multiple users are affected.
     - Speed test is slow for multiple devices.
     - Check router, switch, firewall, access point, or ISP connection.

12. **Escalate if the issue continues.**
   - Escalate the ticket if:
     - Multiple users are affected
     - Packet loss is high
     - Latency is high
     - DNS is slow or failing
     - Speed test results are much lower than expected
     - Router, switch, firewall, or ISP issue is suspected
     - Network equipment requires admin access

## Resolution
Document what fixed the issue. Examples may include moving closer to the access point, switching from Wi-Fi to Ethernet, stopping a large download, disabling VPN, fixing DNS settings, restarting network equipment, or escalating to the ISP or network team.

## Notes
Slow internet troubleshooting is about narrowing down the cause. Start by checking who is affected, then test connection type, speed, latency, DNS, IP configuration, bandwidth usage, VPN, proxy, and browser behavior.
