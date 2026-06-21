# Outlook Not Sending or Receiving Emails

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
This article provides basic troubleshooting steps for Microsoft Outlook when a user cannot send or receive emails.

## Scenario
A user reports that Outlook is not sending emails, not receiving emails, or both. The issue may be related to internet connectivity, Microsoft 365 service health, Outlook profile problems, cached mode, mailbox configuration, or local application issues.

## Common Symptoms
- Outlook does not send emails
- Outlook does not receive new emails
- Emails are stuck in the Outbox
- Outlook shows disconnected or trying to connect
- User can access email through Outlook Web App but not desktop Outlook
- Send/Receive fails with an error
- Outlook opens but mailbox does not update
- Outlook is slow or freezes during sync

## Possible Causes
- Internet connection issue
- Microsoft 365 service issue
- Outlook profile corruption
- Incorrect account settings
- Cached Exchange Mode issue
- Large mailbox or full mailbox
- Add-in conflict
- Outdated Outlook application
- Credential or authentication issue
- Local OST file issue

## Troubleshooting Steps

1. **Confirm the issue with the user.**
   - Ask when the issue started.
   - Ask if the user cannot send, receive, or both.
   - Ask if emails are stuck in the Outbox.
   - Ask if Outlook shows any error message.
   - Ask if the issue happens only in Outlook or also in Outlook Web App.

2. **Check internet connectivity.**
   - Open a browser and test a website.
   - Confirm the computer is connected to Wi-Fi or Ethernet.
   - If needed, run:

   `ping 8.8.8.8`

   `ping google.com`

   - If internet is not working, troubleshoot the network first.

3. **Check Microsoft 365 service health.**
   - Check if Microsoft 365 or Exchange Online is experiencing an outage.
   - In a company environment, check the Microsoft 365 Admin Center service health page if you have access.
   - If there is a known outage, document it and inform the user.

4. **Test Outlook Web App.**
   - Ask the user to sign in to Outlook on the web.
   - Test sending and receiving emails from the browser.
   - If Outlook Web App works, the issue is likely local to the Outlook desktop app or computer.
   - If Outlook Web App does not work, the issue may be account, mailbox, licensing, or Microsoft 365 service related.

5. **Check Outlook connection status.**
   - Open Outlook.
   - Look at the bottom-right corner.
   - Check if it says:
     - Connected
     - Working Offline
     - Trying to connect
     - Disconnected

   - If Outlook is in offline mode, go to:

   `Send / Receive > Work Offline`

   - Make sure Work Offline is turned off.

6. **Check Send/Receive.**
   - In Outlook, go to:

   `Send / Receive > Send/Receive All Folders`

   - Check if emails start syncing.
   - Check for any send/receive error messages.

7. **Check the Outbox.**
   - Open the Outbox folder.
   - Look for stuck emails.
   - If an email has a large attachment, remove it or save it as a draft.
   - Try sending a small test email.

8. **Restart Outlook.**
   - Close Outlook completely.
   - Open Task Manager.
   - Make sure Outlook is not still running in the background.
   - If needed, end the Outlook process.
   - Reopen Outlook and test again.

9. **Start Outlook in Safe Mode.**
   - Open Run with Windows + R.
   - Type:

   `outlook.exe /safe`

   - Test sending and receiving emails.
   - If Outlook works in Safe Mode, an add-in may be causing the issue.

10. **Disable Outlook add-ins.**
   - Open Outlook.
   - Go to:

   `File > Options > Add-ins`

   - Manage COM Add-ins.
   - Disable unnecessary add-ins.
   - Restart Outlook and test again.

11. **Check mailbox storage.**
   - Check if the mailbox is full.
   - In Outlook, go to:

   `File > Tools > Mailbox Cleanup`

   - If the mailbox is full, ask the user to delete or archive old emails.

12. **Check account credentials.**
   - If Outlook keeps asking for a password, check saved credentials.
   - Open Control Panel.
   - Go to:

   `Credential Manager > Windows Credentials`

   - Remove old Microsoft Office or Outlook credentials if needed.
   - Reopen Outlook and sign in again.

13. **Repair the Outlook profile.**
   - Open Control Panel.
   - Go to:

   `Mail > Email Accounts`

   - Select the account.
   - Click Repair.
   - Follow the prompts.
   - Restart Outlook and test again.

14. **Create a new Outlook profile.**
   - Open Control Panel.
   - Go to:

   `Mail > Show Profiles`

   - Click Add.
   - Create a new profile.
   - Add the user's email account.
   - Set the new profile as default.
   - Open Outlook and test sending and receiving.

15. **Reconfigure the account if needed.**
   - Remove and re-add the email account if the profile repair does not work.
   - In a company environment, confirm account settings before removing anything.
   - Make sure the user knows Outlook may take time to resync the mailbox.

16. **Check for Outlook updates.**
   - Open Outlook.
   - Go to:

   `File > Office Account > Update Options > Update Now`

   - Install available updates.
   - Restart Outlook and test again.

17. **Repair Microsoft Office.**
   - Open Run with Windows + R.
   - Type:

   `appwiz.cpl`

   - Select Microsoft 365 or Microsoft Office.
   - Click Change.
   - Run Quick Repair first.
   - If the issue continues, run Online Repair.

18. **Escalate if the issue continues.**
   - Escalate the ticket if:
     - Outlook Web App also does not work
     - Microsoft 365 service health shows an outage
     - The mailbox or license needs admin-level changes
     - The user cannot authenticate
     - The Outlook profile cannot be repaired
     - Emails are missing or mailbox data may be corrupted
     - Multiple users are affected

## Resolution
Document what fixed the issue. Examples may include turning off Work Offline, clearing stuck Outbox emails, testing Outlook Web App, disabling add-ins, repairing the Outlook profile, creating a new Outlook profile, updating Outlook, or repairing Microsoft Office.

## Notes
Testing Outlook Web App is important because it helps identify whether the issue is local to the Outlook desktop app or related to Microsoft 365, Exchange Online, the mailbox, or the user account.
