<h1>Week 2 Helpdesk Exercise</h1>
<p>The second week of doing some ticket handling exercises</p>
<a href = "https://sysdesks.com/app/tickets">Source</a>

<h2>Ticket 1</h2>
<!-- picture1-->
<p>Problem Description: 
The user experienced recurring Active Directory account lockouts after updating her domain password on her desktop computer. The root cause was her mobile device continuing to send background authentication requests using her cached, expired password, which repeatedly exceeded the domain's invalid logon threshold.</p>
<p>Solution & Resolution Steps: 
To resolve the lockouts, the stale corporate account profile was removed from her mobile phone to stop invalid background sign-in attempts, after which her user object was manually unlocked in Active Directory Domain Services. Once the account was active again, her account was re-added to the mobile device using the new password, successfully restoring cross-device functionality without triggering further lockouts. </p>
<p>Recommendations for Prevention
To prevent similar lockouts in the future, users should be instructed to immediately update or sign out of their corporate accounts on all secondary devices (mobile email, VPN, cached Wi-Fi) as soon as they perform a domain password change on their primary desktop.
</p>
<!-- picture2-->

<h2>Ticket 2</h2>
<!-- picture1-->
<p>Problem Description
The user reported that the Windows taskbar Search feature was completely unresponsive and non-functional. Upon investigation, the root cause was determined to be that the underlying Windows Search (WSearch) system service had unexpectedly stopped running, preventing the operating system from processing search queries or indexing local files. </p>
<p>Solution & Resolution Steps
To restore functionality, the service was re-enabled by opening the Services management console (services.msc), scrolling down to locate Windows Search, right-clicking to access Properties, ensuring the startup type was set to Automatic (Delayed Start), clicking Start under Service status to initiate the service, and finally clicking Apply and OK to confirm the taskbar Search bar was immediately responsive.</p>
<p>Recommendations for Prevention
To prevent this issue from recurring, ensure the Windows Search service startup type remains set to Automatic (Delayed Start) so it launches automatically on boot, and check for pending Windows updates or run a system file check (sfc /scannow) if the service continues to terminate unexpectedly.</p>
<!-- picture1-->

<h2>Ticket 3</h2>
<!-- picture1-->
<p>Problem / Request Description
The request was for the provisioning of a new user account in Active Directory, requiring the creation of the account in the correct organizational unit and sending initial access credentials to the end user.</p>
<p>Solution & Resolution Steps
To fulfill the request, the user account was provisioned in Active Directory Domain Services by navigating to the designated department's Organizational Unit (OU), selecting the option to create a new user, populating the required account details (including full name, username, and initial account attributes), and securely transmitting the temporary password to the user.
</p>
<!-- picture1-->

<h2>Ticket 4</h2>
<!-- picture1-->
<p>Problem / Request Description
The user reported that an application's interface language was incorrectly configured to German instead of English, making the interface unreadable and preventing the employee from performing daily operational tasks.</p>
<p>Solution & Resolution Steps
To resolve the display issue, the application settings were navigated by locating the configuration/edit section (Bearbeiten / Einstellungen), identifying the active language preference set to German (Deutsch), and updating the selection back to English (Englisch) to immediately restore the standard user interface language.</p>
<p>Recommendations for Prevention
To prevent unexpected language changes, ensure that regional and language settings in group policies or global application deployment packages are configured to default to system locale settings, and remind users to review preferences before applying profile configuration changes.</p>
<!-- picture1-->

<h2>Ticket 5</h2>
<!-- picture1-->
<p>Problem Description
The user reported that NorthMail was fully operational on her mobile phone but non-functional on her laptop, failing to send or receive emails. Upon investigation, the root cause was determined to be that the mail client on the laptop had been toggled into Offline Mode, preventing it from establishing an active server connection to sync incoming or outgoing messages.</p>
<p>Solution & Resolution Steps
To restore email synchronization, the mail client was brought back online by opening NorthMail on the laptop, navigating to the Send/Receive (or Work Offline) section in the ribbon/settings menu, clicking the Work Offline toggle to disable offline mode, and verifying that the status bar updated to Connected, which immediately allowed pending emails to send and new messages to receive.
</p>
<p>Recommendations for Prevention
To prevent similar occurrences, users should be informed about the "Work Offline" status indicator in the client application and reminded to check their network connection status bar at the bottom of the mail window before reporting email synchronization failures.</p>
<!-- picture1-->

<h2>Key Learning this week:</h2>
<p>This week of exercise taught me to pay attention on small settings changes, because sometimes the problem is just that simple, just a one click away from being fixed. </p>
