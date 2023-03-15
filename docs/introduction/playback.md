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

When joining a share, server owners usually explicitly mention which of these you're allowed to do and how much of each. Let's break down an example: A share allows 2 direct plays / 1 transcode: This means at any given time you will be able to have two devices direct playing content, and one of them may transcode video, just not both at the same time.

[![Direct Play vs Transcode](../media/quality-vs-quantity.png "Direct play vs Transcode")](https://docs.blackbeard.media/media/direct-play-vs-transcode.png)

???+ danger "Transcoding 4K"

    You'll often see shares explicitly disallow video transcoding of 4k content, and for good reason. It stresses the resources of the server to an extreme amount. A single 4K transcode the resources enough for ~8x 1080p transcodes. Worst of all, the quality of the 4K is stream is severely compromised, AND Plex is unable to tonemap HDR properly, which leads to a washed out image, as seen below.

### How do you avoid transcoding?

So enough about the evils of transcoding, how do you actually avoid it? As I mentioned earlier, this is usually dependent on the device's capability and the application you are using. But for most devices, you should be able to avoid transcoding, simply by going into Settings > Video > Set quality to Original/Maximum/Direct Play only. We will go further the settings for each client below. Enabling subtitles can also sometimes lead to transcoding if your device doesn't natively support them. The best way to avoid these issues is to use the devices which have the highest compatibility and support for a wide variety of formats. Here are some general good devices and tips:

#### What device should I buy for Plex?

<div class="grid" markdown>
=== "Nvidia Shield Pro"
    * Powerful hardware: The Shield Pro is equipped with a powerful Tegra X1+ processor and 3GB of RAM, which makes it capable of handling demanding video codecs and high bitrate streams without any lag or buffering.
    * Wide codec support: The Shield Pro supports a wide range of video and audio codecs, including H.265 (HEVC), VP9, and Dolby Vision, which allows for direct playback of most media files without transcoding.
    * 4K HDR streaming: The Shield Pro supports 4K HDR and DolbyVision streaming, which provides high-quality video playback with vibrant colors and deep contrast.
    * Ethernet port: The Shield Pro has a Gigabit Ethernet port, which allows for fast and stable network connectivity and reduces the risk of buffering or playback issues.
=== "Apple TV 4K"
    * A12 Bionic Chip: The Apple TV 4K is equipped with the A12 Bionic chip, which makes it one of the most powerful streaming devices on the market, capable of handling demanding video codecs and high bitrate streams.
    * Wide codec support: The Apple TV 4K supports a wide range of video and audio codecs, including H.265 (HEVC), HDR10, Dolby Vision, and Dolby Atmos, which allows for direct playback of most media files without transcoding.
    * 4K HDR streaming: The Apple TV 4K supports 4K HDR streaming, which provides high-quality video playback with vibrant colors and deep contrast.
    * Ethernet port: Depending on model, the Apple TV 4K has a Gigabit Ethernet port, which allows for fast and stable network connectivity and reduces the risk of buffering or playback issues.
    * Infuse Pro: Infuse Pro is good for Plex streaming on iOS because it offers a user-friendly interface and supports a wide range of video and audio codecs, including high-resolution formats such as 4K DolbyVision and Dolby Atmos.
=== "FireStick 4K Max"
    * Powerful hardware: The FireStick 4K Max is equipped with a powerful quad-core 1.8 GHz processor and 2GB of RAM, which makes it capable of handling demanding video codecs and high bitrate streams without any lag or buffering.
    * Wide codec support: The FireStick 4K Max supports a wide range of video and audio codecs, including H.265 (HEVC), HDR10, HDR10+, and Dolby Vision, which allows for direct playback of most media files without transcoding.
    * 4K HDR streaming: The FireStick 4K Max supports 4K HDR and DolbyVision streaming, which provides high-quality video playback with vibrant colors and deep contrast.
    * Wi-Fi 6 and Ethernet support: The FireStick 4K Max has Wi-Fi 6 and Ethernet support, which allows for fast and stable network connectivity and reduces the risk of buffering or playback issues.
</div>

???+ tip "Pro-tip"

    When on a computer, *always* try to use the Plex Media Player app, instead of the browser players (i.e. Chrome). You will get tone-mapping support, subtitle support, and better video/audio support. You will almost never have to transcode when using the official app.

## Recommended quality settings

By default, Plex's out-of-the-box quality settings limit the bandwidth to between 2-4Mbps, which means that many files will have to be transcoded to meet this limit. However, this can result in decreased video quality and increased server load. The good news is that adjusting the quality settings for your specific client can lead to optimum playback without unnecessary transcoding. To do this, simply select your client below and follow the recommended settings for the best possible playback experience:

### Media Clients
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

### Mobile Clients
<div class="grid cards" markdown>
- :simple-android: __[Android Devices](#)__
- :simple-ios: __[Apple Devices](#)__
</div>

By adjusting these settings, you can ensure that your media is streamed in the best possible quality without causing unnecessary server strain.
