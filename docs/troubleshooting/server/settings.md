# Appboxes - Recommended Settings

Plex Media Server is a powerful media management tool that allows users to organize and stream their media collections across a variety of devices. With so many features and settings, it can be overwhelming for new users to navigate. However, with our recommendations for each setting, you can make the most out of your appbox experience. From library organization and playback settings to server optimization and remote access, we will guide you through each setting to ensure that you are getting the most out of your media server.

To access these settings, we will be using a web browser to view the Plex server, going to settings, and then going through every tab of Settings, starting with 'General' and ending with 'Extras'. Additionally, we will explain a few more tabs in the 'Manage' category, including 'Libraries' and 'Troubleshooting'.

## General

- Set a 'Friendly name'
- Toggle 'Push Notifications'
- Change 'Server update Channel' to match your Kronos settings.

<figure markdown>
![(/media/appbox-settings-general.png)](https://docs.blackbeard.media/media/appbox-settings-general.png)
  <figcaption></figcaption>
</figure>

## Remote Access

Remote Access settings depend on whether or not a Content Delivery Network (CDN) is enabled. If a CDN is enabled, Remote Access needs be disabled for the most benefit. On the other hand, if there is no active CDN, Remote Access should be enabled and working correctly.

<figure markdown>
![(/media/appbox-settings-remote-cdn.png)](https://docs.blackbeard.media/media/appbox-settings-remote-cdn.png){ width=600 }
  <figcaption>An appbox utilizing a CDN</figcaption>
</figure>
<figure markdown>
![(/media/appbox-settings-remote-nocdn.png)](https://docs.blackbeard.media/media/appbox-settings-remote-nocdn.png){ width=600 }
  <figcaption>An appbox without a CDN</figcaption>
</figure>

## Agents

It's recommended to leave the Agents tab in the Plex Media Server settings at its default settings.

## Library

- **Uncheck** 'Scan my library automatically'
- **Uncheck** 'Scan my library periodically'
- **Check** 'Run scanner tasks at a lower priority'
- Set 'Generate video preview thumbnails' to **never**
- Set 'Generate intro video markers' to **as a schedules task and when media is added** or **never**
- Set 'Generate credits video markers' to **never**
- Set 'Generate chapter thumbails' to **as a schedules task and when media is added** or **never**
- Set 'Analyze audio tracks for loudness' to **never**
- Set 'Analyze audio tracks for sonic features' to **never**
- Set 'Database Cache Size (MB)' to **2048**


<figure markdown>
![(/media/appbox-settings-library.png)](https://docs.blackbeard.media/media/appbox-settings-library.png){ width=400 }
  <figcaption></figcaption>
</figure>

## Plugins

It's recommended to leave the Plugins tab in the Plex Media Server settings at its default settings.

## Network

- **Disable** 'Enable server support for IPv6'
- Set 'Secure connections' to **Preferred**
- Set 'Terminate Sessions Paused for Longer Than' to between **5** and **30**
- **Disable** 'Enable Relay'
- 'Custom server acess URLs' will depend on the use of a CDN

<figure markdown>
![(/media/appbox-settings-network-1.png)](https://docs.blackbeard.media/media/appbox-settings-network-1.png)
  <figcaption></figcaption>
</figure>
<figure markdown>
![(/media/appbox-settings-network-2.png)](https://docs.blackbeard.media/media/appbox-settings-network-2.png)
  <figcaption></figcaption>
</figure>

## Transcoder

- Set 'Transcoder Quality' to **Prefer higher speed encoding**
- Set 'Transcoder default throttle buffer' to **300**
- Set 'Background transcoding x264 preset' to **Very fast**
- **Check** 'Enable HDR tone mapping'
- **Uncheck** 'Disable video stream transcoding
- **Check** 'Use hardware acceleration when available'
- **Check** 'Use hardware-accelerated video encoding'
- **^^DO NOT CHANGE^^ 'Maximum simultaneous video transcode'**
    *Changing this setting may result in you losing your appbox*

<figure markdown>
![(/media/appbox-settings-transcoder.png)](https://docs.blackbeard.media/media/appbox-settings-transcoder.png)
  <figcaption></figcaption>
</figure>

## Languages

The Languages tab in settings should be set to the best fit your preferred languages.

## DLNA

- **Uncheck** 'Enable the DLNA Server'

## Scheduled Tasks

Ensure that you have had us change your time zone to match your location so that these settings will match.

- Time at which tasks run and stop running will dependent on your usecase
- **Uncheck** 'Backup database every three days'
- **Check** 'Optimize database every week'
- **Check** 'Remove old bundles every week'
- **Check** 'Remove old cache files every week'
- **Uncheck** 'Refresh local metadata every three days'
- **Uncheck** 'Update all libraries during maintenance'
- **Uncheck** 'Upgrade media analysis during maintenance'
- **Uncheck** 'Refresh library metadata periodically'
- **Uncheck** 'Perform extensive media analysis during maintenance'

<figure markdown>
![(/media/appbox-settings-tasks.png)](https://docs.blackbeard.media/media/appbox-settings-tasks.png)
  <figcaption></figcaption>
</figure>

## Extras

The Extras tab should be set to match your preferences on Cinema Trailers.

## Manage > Libraries

Appbox owners have the ability to tailor their user's viewing experience by controlling what shows and movies are recommended to them. This is done through the Libraries tab, where server admins can manage which recommendation rows will appear on their player app home screens when a source is pinned in the sidebar. Additionally, admins can control the Recommended tab for each individual library and the home screen rows when a shared user has the library pinned in the sidebar. This level of control allows Appbox owners to personalize the recommendations for their users and ensure that they are seeing content that is relevant to their interests.

### Recommended Collections to Pin and Order

Below is a list of collections we recommend to pin to the Library Recommended and/or Home screens, as well as the recommended order for them. These collections are available in [our default Plex Meta Manager configuration](/troubleshooting/server/pmm) for each library.

<figure markdown>
![(/media/appbox-manage-libraries-movies.png)](https://docs.blackbeard.media/media/appbox-libraries-movies.png)
  <figcaption>Recommended settings for movie libraries</figcaption>
</figure>
<figure markdown>
![(/media/appbox-manage-libraries-tv.png)](https://docs.blackbeard.media/media/appbox-manage-libraries-tv.png)
  <figcaption>Recommended settings for TV libraries</figcaption>
</figure>
