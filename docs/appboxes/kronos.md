# Kronos

Kronos is a powerful dashboard that gives you complete control and management over your appbox. With Kronos, you can manage various aspects of your appbox, such as claiming your Plex server, configuring CDNs, and setting up automatic restarts and updates. You can also troubleshoot issues, create support tickets, and set up custom collections. Additionally, Kronos allows you to set up backups to ensure that your data is always safe and secure.

## Claiming Your Appbox

1. Using the credentials which were emailed to you, log into our [Kronos Dashboard](https://kronos.blackbeard.shop).
2. Once logged in, you should see your server listed in the Dashboard, select it.
    
    <figure markdown>
    ![(../media/kronos_server_select.png "Once logged in, you should see your server listed in the Dashboard, select it.")](https://docs.blackbeard.media/media/kronos_server_select.png){ width=750 }
      <figcaption></figcaption>
    </figure>
    
3. You will be taken to the Server Overview page. Underneath the "Plex server has not yet been claimed" warning, enter your Plex username or email address and password, then press "Claim Plex Server".
    
    <figure markdown>
    ![(../media/kronos_claim.png "Press 'Claim Plex Server'.")](https://docs.blackbeard.media/media/kronos_claim.png){ width=650 }
      <figcaption></figcaption>
    </figure>
    
4. You should be presented with a "Success!" box. This means that the Appbox has successfully been claimed by your user, and you should now be able to log into Plex and see your appbox, either by clicking the link underneath "Plex server IP" on the Server Overview page, or by navigating to the Plex website. Make sure to use the same credentials that you used to claim the Plex Server.

!!! warning "Create a Support Ticket"
    
    After claiming your Plex server, it is important that you do not initiate any manual scans as our autoscan system will ensure that everything is fully updated. Instead, we kindly ask that you create a support ticket on our Discord channel and include your time zone so that we can update the docker container accordingly. This step is crucial to ensure that your server is up-to-date and running smoothly. 
    We appreciate your cooperation and support in maintaining the quality of our service.

## Setting up Daily Restarts

Setting up daily restarts on your appbox allows for Plex to install any necessary updates on the scheduled restart and is also a best practice to reduce the likelihood of issues occurring if your appbox is powered on for a long period of time.

1. Using the credentials which were emailed to you, log into our [Kronos Dashboard](https://kronos.blackbeard.shop).
2. Once logged in, you should see your server listed in the Dashboard, select it, as shown above.
3. You will be brought to the Server Overview page. Scroll down and please select a time you wish to have your appbox restart daily and select "Save." You may also opt into Plex beta builds if you are have PlexPass and daily backups.
    
    <figure markdown>
    ![(../media/kronos_restart.png "Select the time to restart and if you want daily backups and Plex beta builds")](https://docs.blackbeard.media/media/kronos_restart.png){ width=750 }
      <figcaption></figcaption>
    </figure>
    
4. Now, we need to set your timezone in Kronos. Click the profile icon on the top right of the page and choose "Account Settings," followed by "Service Settings."
    
    <figure markdown>
    ![(../media/kronos_user_settings.png "Click here to go to user settings")](https://docs.blackbeard.media/media/kronos_user_settings.png){ width=750 }
      <figcaption></figcaption>
    </figure>
    
5. Select "User Settings".
    
    <figure markdown>
    ![(../media/kronos_user_settings2.png "Click here to go to user settings")](https://docs.blackbeard.media/media/kronos_user_settings2.png){ width=750 }
      <figcaption></figcaption>
    </figure>
    
6. Once here, change the timezone to your local timezone; this ensures that the daily restart is scheduled for the correct timezone.
    
    <figure markdown>
    ![(../media/kronos_timezone.png "Select your local timezone")](https://docs.blackbeard.media/media/kronos_timezone.png){ width=750 }
      <figcaption></figcaption>
    </figure>
    
## Kronos Dashboard

<figure markdown>
![(../media/kronos_dashboard.png "The Kronos Dashboard")](https://docs.blackbeard.media/media/kronos_dashboard.png){ width=750 }
  <figcaption></figcaption>
</figure>

The Kronos dashboard also provides a range of tools for troubleshooting and customization. These tools can help you optimize your Plex server and ensure a seamless streaming experience for your users. Some of the things you can do on the Kronos dashboard include:

### Restarting the Server

If you encounter any issues with your Plex server, you can use the dashboard to restart the server. This can help resolve many common problems and ensure that your server is running smoothly.

### Unclaiming the Server

If you need to move your Plex server to a different account, you can use the unclaim option on the dashboard to release the server from your account.

### Resetting the Plex Config

If you have made changes to your Plex server's settings and want to revert to the default configuration, you can use the reset option on the dashboard.

### Rebuilding the Plex Server

If your Plex server is experiencing issues that cannot be resolved through other troubleshooting methods, you can use the rebuild option on the dashboard. This will completely wipe the server and start over with a fresh installation.

### Enabling a CDN

A Content Delivery Network (CDN) can help improve the streaming performance of your Plex server by distributing content across multiple servers. You can enable a CDN on the Kronos dashboard to enhance your server's performance.

### Installing and Managing Tautulli

Tautulli is a third-party tool that can be used to monitor and analyze the performance of your Plex server. You can install and manage Tautulli directly from the Kronos dashboard.
