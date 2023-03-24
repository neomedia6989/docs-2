# Appboxes - Troubleshooting

When running a private instance of Plex through an appbox, it's not uncommon to encounter issues or errors that prevent a seamless streaming experience for your users. Troubleshooting these problems can be challenging, especially if you're not familiar with the inner workings of the Plex server. In this guide, we'll explore common issues that users may encounter when using an appbox, and provide solutions and tips to help you resolve them.

## How to Check Appbox Status

To check the status of your appbox on the Kronos dashboard, follow these steps:

1. Log in to your Kronos dashboard and select your appbox server.
2. On the server dashboard, look for the status section to see if the server is running.
3. If the server is not running, click on the 'Restart' button in the status section to restart the server.
4. Wait for the server to restart, which may take a few minutes, and then refresh the page to check the server status again.

If you encounter any issues with your appbox server, restarting the server using these steps can often help resolve the problem and is the first recommended step in troubleshooting.

## Appbox Connectivity Issues

Check the appbox status on the Kronos dashboard after selecting your server. If it appears to be down, but Kronos says it's up, we will need to troubleshoot network settings. The troubleshooting process for appbox connectivity may vary depending on whether the CDN is enabled or not.

### CDN Enabled

1. If you are using CDN, verify that your custom access URL within the Network section of the Settings is working and is the correct URL for you. To verify the correct URL, take note of your 'Service ID' from the Kronos dashboard. The URLs should be `http://XXX.blackbeard.brrrrrr.net,https://XXX.blackbeard.brrrrrr.net`, where XXX is your Service ID.
2. Next, we will verify that the URL redirect is active and working properly. Copy and paste each custom access URL (one with `http://` and one with `https://`) into the browser and ensure they go to Plex.
3. Go back to the Network Settings page and ensure that 'Enable server support for IPv6' is **disabled**, 'Secure connections' is set to **Preferred**, and 'Enable Relay' is **disabled**.
4. Click on Remote Access on the left sidebar, then ensure Remote Access is disabled and restart your appbox from the Kronos dashboard.
5. Your appbox should now be connectable from any device using the Plex app.

### CDN Disabled

1. If you are not using CDN, start by ensuring that Remote Access is enabled in the Settings. 
2. If it is enabled but says "Not available outside your network," please take note of the port number from the Kronos dashboard, then toggle the check the box next to 'Manually specify public port' and enter the port number from the Kronos dashboard and click Retry.
3. Your appbox should now be connectable from any device using the Plex app.

## Invited Users Having Issues

Troubleshooting Plex clients involves identifying the specific issue the user is experiencing and then taking steps to resolve it. This can include checking network settings, updating software, clearing caches, and adjusting playback settings. Common issues may include video playback issues, audio playback issues, subtitle issues, device compatibility issues, and understanding 4K streaming issues on Plex. By working with the user to identify the specific issue and taking the appropriate steps to resolve it, the user can enjoy their content without interruption. Please see our [client troubleshooting section](/troubleshooting/client/) for more assistance.

## Performance / Stability Issues

Plex servers may require routing maintenance to ensure proper connectivity and availability. To help with this, Kronos will attempt to run as many maintenance tasks as possible, but it relies on users to set up daily restarts. To do this, users can refer to [this link](/appboxes/kronos/#setting-up-daily-restarts) on how to set a daily restart. However, if users continue to experience issues such as extreme latency, missing content, or loss of connectivity, please submit a [support ticket](https://discord.com/channels/532304048200744982/921503213432242196).

???+ tip "Check for Plex Updates"
    
    It is highly recommended to have daily restarts set for your appbox. Part of the maintenance Kronos does during daily restarts is to ensure you have the most up-to-date version of the Plex Media Server, and if daily restarts are disabled then you may miss vital updates which may impact the performance of your appbox.
    
    
