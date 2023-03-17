# Kronos

Kronos is a powerful dashboard that gives you complete control and management over your appbox. With Kronos, you can manage various aspects of your appbox, such as claiming your Plex server, configuring CDNs, and setting up automatic restarts and updates. You can also troubleshoot issues, create support tickets, and set up custom collections. Additionally, Kronos allows you to set up backups to ensure that your data is always safe and secure.

## Claiming Your Appbox

1. Using the credentials which were emailed to you, log into our [Kronos Dashboard](https://kronos.blackbeard.shop).
2. Once logged in, you should see your server listed in the Dashboard, select it.
  
  <figure markdown>
  ![(../media/kronos_server_select.png "Select your new server")](https://docs.blackbeard.media/media/kronos_server_select.png){ width=750 }
  </figure>
  
3. You will be taken to the Server Overview page. Underneath the "Plex server has not yet been claimed" warning, enter your Plex username or email address and password, then press "Claim Plex Server".
  
  <figure markdown>
  ![(../media/kronos_claim.png "Click here to claim your server")](https://docs.blackbeard.media/media/kronos_claim.png){ width=600 }
  </figure>
  
4. You should be presented with a "Success!" box. This means that the Appbox has successfully been claimed by your user, and you should now be able to log into Plex and see your appbox, either by clicking the link underneath "Plex server IP" on the Server Overview page, or by navigating to the Plex website. Make sure to use the same credentials that you used to claim the Plex Server.

## Setting up Daily Restarts

Setting up daily restarts on your appbox allows for Plex to install any necessary updates on the scheduled restart and is also a best practice to reduce the likelihood of issues occurring if your appbox is powered on for a long period of time.

1. Using the credentials which were emailed to you, log into our [Kronos Dashboard](https://kronos.blackbeard.shop).
2. Once logged in, you should see your server listed in the Dashboard, select it, as shown above.
3. You will be brought to the Server Overview page. Scroll down and please select a time you wish to have your appbox restart daily and select "Save." You may also opt into Plex beta builds if you are have PlexPass and daily backups.
  
  <figure markdown>
  ![(../media/kronos_restart.png "Select the time to restart and if you want daily backups and Plex beta builds")](https://docs.blackbeard.media/media/kronos_restart.png){ width=750 }
  </figure>
  
4. Now, we need to set your timezone in Kronos. Click the profile icon on the top right of the page and choose "Account Settings," followed by "Service Settings."
  
  <figure markdown>
  ![(../media/kronos_user_settings.png "Click here to go to user settings")](https://docs.blackbeard.media/media/kronos_user_settings.png){ width=750 }
  </figure>
  
5. Select "User Settings".
  
  <figure markdown>
  ![(../media/kronos_user_settings2.png "Click here to go to user settings")](https://docs.blackbeard.media/media/kronos_user_settings2.png){ width=750 }
  </figure>
  
6. Once here, change the timezone to your local timezone; this ensures that the daily restart is scheduled for the correct timezone.
  
  <figure markdown>
  ![(../media/kronos_timezone.png "Select your local timezone")](https://docs.blackbeard.media/media/kronos_timezone.png){ width=750 }
  </figure>
  
