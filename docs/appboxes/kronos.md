# Kronos

Kronos is a powerful dashboard that gives you complete control and management over your appbox. With Kronos, you can manage various aspects of your appbox, such as claiming your Plex server, configuring CDNs, and setting up automatic restarts and updates. You can also troubleshoot issues, create support tickets, and set up custom collections. Additionally, Kronos allows you to set up backups to ensure that your data is always safe and secure.

## Claiming Your Appbox

!!! warning "Disable Two Factor Authentication"

  Before claiming your server, if you have Two Factor Authentication (2FA) Enabled in Plex, you must disable it prior to claiming your server. Once the server has been claimed, you can re-enable 2FA. More information on 2FA, including how to disable/enable it, can be found [here](https://support.plex.tv/articles/two-factor-authentication/).

1. Using the credentials which were emailed to you, log into our [Kronos Dashboard](https://kronos.blackbeard.shop).
2. Once logged in, you should see your server listed in the Dashboard, select it.
3. You will be taken to the Server Overview page. Underneath the "Plex server has not yet been claimed" warning, enter your Plex username or email address and password, then press "Claim Plex Server".
4. You should be presented with a "Success!" box. This means that the Appbox has successfully been claimed by your user, and you should now be able to log into Plex and see your appbox, either by clicking the link underneath "Plex server IP" on the Server Overview page, or by navigating to the Plex website. Make sure to use the same credentials that you used to claim the Plex Server.

## Setting up Daily Restarts

Setting up daily restarts on your appbox allows for Plex to install any necessary updates on the scheduled restart and is also a best practice to reduce the likelihood of issues occurring if your appbox is powered on for a long period of time.

1. Using the credentials which were emailed to you, log into our [Kronos Dashboard](https://kronos.blackbeard.shop).
2. Once logged in, you should see your server listed in the Dashboard, select it.
3. You will be brought to the Server Overview page. Click the profile icon on the top right of the page and choose "Account Settings," followed by "Service Settings."
4. Once here, please select a time you wish to have your appbox restart daily and select "Save."
5. Press the profile icon on the top right of the page again, selecting "Account Settings," followed by "User Settings." Change the timezone to your local timezone; this ensures that the daily restart is scheduled for the correct timezone.
