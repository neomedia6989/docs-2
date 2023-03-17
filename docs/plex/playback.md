# Playback and Playback Quality in Plex

## Playback

Playback works very similar to how it does on other streaming services; on streaming devices, if you push the play button on a title, playback should begin immediately. If you press select/OK/enter, you'll be taken to the information page about a title. For movies this will include a summary and other information. For a TV show, this will go to a list of seasons. And from there you can select a season to view the list of individual episodes.

On a desktop client, when the mouse is over the title image, a Play button will be visible - if you click that, playback should begin. If you click elsewhere, the process will be similar to selecting on a streaming device.

## Playback Quality

Plex playback quality is dynamic and tries to adjust to the capabilities of your player and to the available internet bandwidth. However out of the box, the quality settings in most Plex players are very conservative of either 2Mbps or 4Mbps, which we highly recommend increasing.

To increase the quality of your playback experience, locate the settings in your Plex app, and navigate to the Video Settings section. Typically you should try to set Video Quality to Original or Maximum if possible. If you then find playback stutters or pauses frequently, reduce the quality setting until you achieve smooth playback. This will ensure that media is played on your device at the highest quality possible and can help reduce strain on the Plex server.

## Transcode vs Direct Play

### Transcode

If you play video via Plex and reduce the streaming quality to anything lower then its original quality, then the video will be considered to be "transcoding"; Plex is essentially taking the original file and converting it to a different file that you can stream. This requires processing power resources from a server. Video can be transcoded due to a variety of reasons:

#### Slow Connection

If the connection from your client to a Plex server only allows for 10Mbps, and if the file you are playing is averaging 40Mbps, the Plex server will attempt to transcode the HQ video into a 10Mbps stream so that you can get smooth playback without stuttering, pausing, or buffering. This is usually most apparent on slower connections or on mobile devices with slow roaming connections. Please be aware that the bitrate shown in Plex is the average bitrate and you may require up to twice as much bandwidth to be able to direct play the video without issues.

#### Client Support

Without getting too technical, each client (PC, TV, phone, web player, etc.) and the different Plex apps have different capabilities based on your device's codec support. What this means is that if you attempt to play a video (encoded in the H.265 codec) on a given device, but this client doesn't support that codec, it will transcode it to a different codec that it can play, once again requiring server resources and lowering quality. The main things to look for in regards to client support include the following:

- [x] **Codec support:** The client needs support the codecs used in your media files to avoid transcoding. Common codecs include H.264, H.265 (HEVC), and VP9.
- [x] **Audio support:** The client needs support the audio formats used in your media files. Common audio formats include AAC, AC3, EAC3, and DTS.
- [x] **Subtitle support:** The client needs to be able to display subtitles for any media files you watch without the need for transcoding.
- [x] **HDR support:** If you are watching HDR content, the client needs support HDR playback to ensure the best possible viewing experience. This is very important in regards to DolbyVision.
- [x] **Resolution support:** The client needs be able to handle the resolution of your media files without the need for transcoding. For example, if you are watching 4K content, the client needs to be able to play it without downsampling it to 1080p.

#### Subtitles

To further expand on the point above, some clients don't support being able to display the video stream and the subtitle stream at the same time, and so, if you turn on subtitles, Plex will create a second video with the subtitles burned in, so that your client sees the two streams merged as one, and is able to show subtitles. This is considered transcoding. If you are presented with an option for subtitles, always try to select `.SRT` subtitles, as they have are compatible with the most devices.

### Direct Play / Stream

Direct playing is streaming of video exactly in the format stored on the server, with no transcoding. This requires relatively little server resources (CPU/GPU), but will require usually more upload bandwidth, since you're streaming it in the original quality. This is the ideal way of playing content since most servers usually have more bandwidth than CPU/GPU resources. Not only is it better for the server, it is also best for YOU. You get to view content in the highest original quality, the quality that you are quite possibly paying for.

Direct streaming is when you are direct playing the video but the transcoding audio of the file. This doesn't strain the server much and when shares mention 'No Transcoding', they're typically only referring to video transcoding - so direct streaming can usually be considered the same as direct playing for all intents and purposes.

### Why you should care about transcoding?

When joining a share, server owners usually explicitly mention which types of playback are allowed and how much of each. For example, a share may allow 2 direct plays and 1 transcode. This means that at any given time, you will be able to have two devices direct playing content, and one device may transcode video, but not both at the same time. Transcoding can put a significant strain on the server's resources, leading to buffering or playback issues for other users. Additionally, transcoding can reduce the quality of the video and audio being streamed. Direct playing, on the other hand, allows for the highest quality playback and puts less strain on the server, resulting in smoother playback for everyone. As such, it's often recommended to direct play files whenever possible and to limit transcoding as much as possible.

???+ danger "Transcoding 4K"

    It's common for shares to explicitly disallow video transcoding of 4K content, and for good reason. It puts an extreme amount of stress on the server's resources. A single 4K transcode can consume resources equivalent to ~8x 1080p transcodes. Worst of all, the quality of the 4K stream is severely compromised, and Plex is unable to properly tonemap HDR, resulting in a washed-out image. If the 4K version is unplayable, it's recommended to play the 1080p version instead, as this will provide a better viewing experience without compromising the server's resources or video quality

<figure markdown>
![(../media/direct-play-vs-transcode.png "Direct play vs Transcode")](https://docs.blackbeard.media/media/direct-play-vs-transcode.png){ width=750 }
    <figcaption>An example of direct playing versus transcoding</figcaption>
</figure>

### How Do You Avoid Transcoding?

When streaming media, there are factors outside of your control that may cause transcoding, such as the source file's compatibility with your device or internet speed. However, there are still some things you can do on your end to optimize your streaming experience. First, make sure you have a stable internet connection with enough bandwidth to handle the highest quality available for your media. Next, go into your device's streaming app settings and select the highest quality available, such as Original/Maximum/Direct Play only. Avoid using subtitles if possible, as they can sometimes cause transcoding if your device doesn't support them natively. Using a device that has high compatibility and support for various formats can also help reduce the likelihood of transcoding. While you may not have control over the media, these steps can help ensure the best streaming experience possible.

???+ tip "Pro-tip"

    When on a computer, *always* try to use the Plex Media Player app, instead of the browser players (i.e. Chrome). You will get tone-mapping support, subtitle support, and better video/audio support. You will almost never have to transcode when using the official app.

#### What Device Should I Buy for Plex?

<div class="grid" markdown>
=== "Nvidia Shield Pro"
    * Equipped with a powerful Tegra X1+ processor and 3GB of RAM, which makes it capable of handling demanding video codecs and high bitrate streams without any lag or buffering.
    * Supports a wide range of video and audio codecs, including H.265 (HEVC), VP9, and Dolby Vision, which allows for direct playback of most media files without transcoding.
    * Supports 4K HDR and DolbyVision streaming, which provides high-quality video playback with vibrant colors and deep contrast.
        * The Shield Pro is the only device on this list that will support all profiles of DolbyVision
    * Has a Gigabit Ethernet port, which allows for fast and stable network connectivity and reduces the risk of buffering or playback issues.
=== "Apple TV 4K"
    * Equipped with the A12 Bionic chip, which makes it one of the most powerful streaming devices on the market, capable of handling demanding video codecs and high bitrate streams.
    * Supports a wide range of video and audio codecs, including H.265 (HEVC), HDR10, Dolby Vision, and Dolby Atmos, which allows for direct playback of most media files without transcoding.
    * Supports 4K HDR streaming, which provides high-quality video playback with vibrant colors and deep contrast.
    * Depending on model, the Apple TV 4K has a Gigabit Ethernet port, which allows for fast and stable network connectivity and reduces the risk of buffering or playback issues.
    * Infuse Pro is good for Plex streaming on iOS because it offers a user-friendly interface and supports a wide range of video and audio codecs, including high-resolution formats such as 4K DolbyVision and Dolby Atmos.
        * Infuse is highly recommended as the default Plex app will struggle with 4K and will be unable to play DolbyVision or direct play DTS HD MA / TrueHD audio.
=== "FireStick 4K Max"
    * Equipped with a powerful quad-core 1.8 GHz processor and 2GB of RAM, which makes it capable of handling demanding video codecs and high bitrate streams without any lag or buffering.
    * Supports a wide range of video and audio codecs, including H.265 (HEVC), HDR10, HDR10+, and Dolby Vision, which allows for direct playback of most media files without transcoding.
    * Supports 4K HDR and DolbyVision streaming, which provides high-quality video playback with vibrant colors and deep contrast.
    * Has Wi-Fi 6 and Ethernet support, which allows for fast and stable network connectivity and reduces the risk of buffering or playback issues.
</div>

#### Recommended Quality Settings

By default, Plex's out-of-the-box quality settings limit the bandwidth to between 2-4Mbps, which means that many files will have to be transcoded to meet this limit. However, this can result in decreased video quality and increased server load. The good news is that adjusting the quality settings for your specific client can lead to optimum playback without unnecessary transcoding. To do this, simply select your client below and follow the recommended settings for the best possible playback experience:

##### Media Clients
<div class="grid cards" markdown>
- :simple-amazonfiretv: __[Amazon FireTV](#)__
- :simple-android: __[Android TV](#)__
- :simple-apple: __[AppleTV](#)__
- :simple-kodi: __[Kodi](#)__
- :simple-lg: __[LG / WebOS](#)__
- :material-plex: __[Plex Media Player](#)__
- :material-plex: __[Plex Web Player](#)__
- :simple-roku: __[Roku](#)__
- :simple-xbox: __[Xbox](#)__
</div>

##### Mobile Clients
<div class="grid cards" markdown>
- :simple-android: __[Android Devices](#)__
- :simple-ios: __[Apple Devices](#)__
</div>

By adjusting these settings, you can ensure that your media is streamed in the best possible quality without causing unnecessary server strain.
