# Transcode vs Direct Play

## Transcode

If you play video via plex and reduce the streaming quality to anything lower then its original quality, then the video will be considered to be "transcoding". Plex is essentially taking the original file and converting it to a different file that you can stream. This requires processing power resources from a server. Video can be transcoded due to a variety of reasons:

### Slow Connection

If the connection from your client to a Plex server only allows for 10mbps, and if the file you are playing is averaging 40Mbps, the Plex server will attempt to transcode the HQ video into a 10mbps stream so that you can get smooth playback without stuttering, pausing, or buffering. This is usually most apparent on slower connections or on mobile devices with slow roaming connections.

### Client Support

Without getting too technical, each client (tv, phone, PC, web player) and the different Plex apps have different capabilities based on your device's codec support. What this means is that if you attempt to play Video A (encoded in the H.265 codec) on Client A, and this Client A doesn't support that codec, it WILL transcode it to a different codec that it CAN play, once again requiring server resources.

### Subtitles

Similar to the above point, some clients don't support being able to display the video stream and the subtitle stream at the same time, and so, if you turn on subtitles, Plex will create a second video with the subtitles burned in, so that your client sees the two streams merged as one, and is able to show subtitles. This is considered transcoding.

## Direct Play

Streaming of video exactly in the format stored on the server, with no transcoding. This requires relatively little server resources (CPU/GPU), but will require usually more upload bandwidth since you're streaming it in the original quality. This is the ideal way of playing content since most servers usually have more bandwidth than CPU/GPU resources. Not only is it better for the server, it is also best for YOU. You get to view content in the highest original quality, the quality that you are quite possibly paying for. Direct Stream, is the direct playing of video, but the transcoding of audio. This doesn't strain the server much and when shares mention 'No Transcoding,' they're only referring to video transcoding, and can be considered the same as Direct Play for all intents and purposes.

## What does this actually mean to me when joining a share?

When joining a share, server owners will usually explicitly mention which of these you're allowed to do and how much. Let's break down an example:
A share allows 2 Direct Plays/1 Transcode. This means at any given time you will be able to have two devices direct playing content, and one of them may transcode video, just not both at the same time.

> **Transcoding 4K:** You'll often see shares explicitly disallow video transcoding of 4k content, and for good reason. It stresses the resources of the server to an extreme amount. A single 4K transcode the resources enough for ~8x 1080p transcodes. Worst of all, the quality of the 4K is stream is severely compromised, AND Plex is unable to tonemap HDR properly, which leads to a washed out image, as seen below.

[![Direct Play vs Transcode](../media/quality-vs-quantity.png "Direct play vs Transcode")](https://docs.blackbeard.media/media/direct-play-vs-transcode.png)
