# Plex Clients - Troubleshooting

Sometimes, when you use an app like Plex to watch movies or TV shows, things might not work quite right. Maybe the video stops playing or the app freezes up. If this happens, one thing you can try is closing the app and opening it again. This is like turning something off and then turning it back on. It can help the app start fresh and might fix the problem. Another thing you can try is signing out of the app and then signing back in. This can also help the app start fresh and might fix any problems you were having.

If you are still having issues, please refer to the information below to hopefully resolve your issues.

## Basic Troubleshooting

If you're experiencing issues with the Plex app, don't worry - there are several steps you can take to troubleshoot the problem. Here are some basic troubleshooting steps to help get you started:

1. Ensure "Allow Insecure Connections" is **enabled**. This can be found in your server settings under Network.
2. Ensure the server is online and accessible. You can check the status of our share servers **[here](https://uptime.blackbeard.media/status/home)** and appboxes on the Kronos dashboard.
3. Check that the Plex app is up-to-date.
4. Restart the Plex app on your device.
5. Restart your device.
6. Uninstall and reinstall the Plex app on your device.
7. If you're still experiencing issues, you can consult the documentation below and/or create a **[support ticket](https://discord.com/channels/532304048200744982/921503213432242196)** where we will be happy to help.

## Video Playback Issues

There are a few things you can try to fix these issues. First, you can [check your internet connection](/troubleshooting/#understanding-internet-speed-and-your-connection) to make sure it's strong enough to stream videos. If your internet is slow or weak, the video might not play smoothly.

Another thing you can try is [adjusting the quality settings for the video](/clients/other/). If the video is set to play at a really high quality, but your internet or device can't handle it, then you might need to lower the quality to make it work better.

Finally, you can [optimize your network settings](/troubleshooting/#improving-video-streaming-by-changing-dns), which means adjusting the settings on your device or router to make sure that everything is working as well as it can. This can help videos play more smoothly and without any issues.

???+ tip "Scan Missing Media Tool"

    Our web portal features a tool called [Scan Missing Media](https://blackbeard.media/scan-media) that can help subscribers resolve various playback issues, such as receiving an error message stating "Cannot play media, ensure that the drive is mounted". These types of errors often occur when upgrading media files (e.g. from 720p to 1080p) and the Plex metadata becomes outdated. By running the [Scan Missing Media](https://blackbeard.media/scan-media) tool, subscribers can update the Plex metadata and typically resolve playback errors.

## Audio Playback Issues

Sometimes when you're watching a movie or TV show on Plex, the sound might not be working quite right. Maybe it sounds too quiet, too loud, or distorted.

There are a few things you can try to fix these issues. First, you can adjust the audio settings for the video. This means changing things like the volume, bass, treble, and other sound settings to make sure that the audio is working as well as it can.

Another thing you can try is updating the audio drivers on your device. This is like making sure that the device knows how to play the sound correctly. If the drivers are old or outdated, the sound might not work well.

Finally, you can check for compatibility issues with your device or platform. This means making sure that the device you're using to watch the video and the platform you're using to play it on (like Windows, Mac, or Android) are working together correctly. If they're not, you might need to find a different way to watch the video or use a different device.

???+ note "Lossless Audio"

    Please note that lossless audio formats, like DTS-HD MA and TrueHD, may require audio passthrough to be enabled on most devices. This means that the device is able to pass the audio signal through to another device, like a receiver, to decode the audio.

## Subtitle Issues

Sometimes when you watch a movie or TV show on Plex, the words that show what the people are saying (called "subtitles") might not work right. They might not show up on the screen, or they might not match what the people are saying.

To fix these issues, you can try a few things. First, you can adjust the settings for the subtitles. This means changing things like the size or color of the words, or how fast they show up on the screen. You can also check if the subtitles work with the movie or show you're watching.

If the subtitles still don't work, you can try downloading new ones and making them match with what the people are saying on the screen. If you're a Share subscriber, you can upload new subtitles to [our website](https://blackbeard.media/subtitles-upload). If you're an Appbox subscriber, you can upload new subtitles through the Plex user interface.

???+ note "Subtitles and Transcoding"

    When troubleshooting playback issues on Plex, it's important to note that subtitles can often force the video to transcode, which can cause playback issues. Therefore, turning off subtitles should be one of the first things to try when troubleshooting transcoding issues.

## Device Compatibility Issues

Sometimes when people try to use Plex on a device, it might not work the way they want it to. This means that the device you're trying to use Plex on might not work well with Plex.

To fix this, there are a few things you can try. To start with, check out our [recommended settings guides](/clients/other/). Beyond those guides, you can check if there are any updates or compatibility issues with the device or platform you're using. This means making sure that the device you're using is compatible with Plex and that it's up-to-date.

To make sure you're getting the best possible video quality on Plex, there are a few things you can check. First, make sure that HDR and DV are enabled if you're watching content that supports these features. Additionally, ensure that your device's maximum h.264 level is sufficient to handle the video being played.

Next, check that Direct Play and Direct Stream are enabled, as this will ensure that the video is played in its original quality without any transcoding that could reduce the quality.

You can also set the streaming quality to maximum to ensure the best possible video playback. Additionally, turn off 'Automatically Adjust Quality' and 'Quality Suggestions' to prevent Plex from changing the video quality during playback. Finally, ensure that 'Use Recommended Settings' is turned off so that you can manually adjust settings for optimal performance.

Finally, if none of these things work, you might need to try using a different device or platform to watch your videos on Plex.

???+ note "Important information about Plex for various older smart TVs"

    Since September 2021, some older smart TVs (e.g. Samsung, LG, Vizio, Hisense, and other unsupported TV platforms) will no longer be able to use "secure connections" to communicate with Plex Media Servers. Please ensure that your app is set to allow insecure connections as instructed by Plex for a possible workaround if you notice issues when using a known affected model: [Click here to learn more](https://forums.plex.tv/t/important-information-about-plex-for-smart-tvs-after-september-30-2021/746506/1)

## Understanding 4K Streaming Issues on Plex

When you watch movies or shows, sometimes you might want to watch them in really high quality, which is called 4K. But sometimes, if your internet isn't very fast, or if the thing you're watching isn't made in a certain way, it might not work very well on Plex.

One thing that's important is the way that the movie or show is made, which is called the "codec". Some codecs work better than others for 4K videos. If the codec isn't supported by Plex, then you might not be able to watch the 4K video on Plex.

Another thing that's important is the amount of information that's in the video, which is called the "bitrate". If the video has too much information, then your internet might not be able to handle it and the video might pause or not play well.

Finally, some 4K videos have special features called HDR or DV, which make the colors and brightness look even better. But if your device or TV doesn't support these features, then the video might not work very well or look very good.

So, if you want to watch 4K videos on Plex, you need to make sure that your internet is fast enough, the video uses a supported codec, the bitrate isn't too high, and your device or TV supports any special features like HDR or DV. If you're not sure if something will work, you can always try it and see how it goes!

## Chromecast Subtitle Playback Issues on Plex

Some Chromecast models lack hardware support for certain subtitle types, so the Plex server must "burn in" the subtitles into the video stream, which can cause the transcoder to stall and freeze playback. This issue can be particularly frustrating for users who want to watch foreign-language content or movies with subtitles. It is recommended to check the compatibility of your Chromecast model with the subtitle types you plan to use before attempting to stream with Plex or to disable sub-titles when viewing on a Chromecast.

## Audio Playback Issues on Samsung and LG Plex App

If you're using Samsung or LG Plex apps, it's important to note that these apps do not play back many files with DTS audio. To work around this issue, we recommend forcing the client to transcode by changing the maximum bitrate to lower than the original bitrate of the file or utilizing a streaming device, such as an Apple TV 4K, FireStick 4K Max, or Nvidia Shield Pro, that supports DTS audio. By doing so, you can ensure smooth playback with minimal interruptions.
