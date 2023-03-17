# Things to Consider

When it comes to choosing a Plex share, there are several factors that you should consider to ensure you get the best streaming experience. It's not just about the number of libraries or the content quality, but also the location of the servers, peering to your location, and how well the service performs during peak times. Additionally, it's important to understand how they handle requests, and if they have any restrictions or limitations. In this guide, we'll go over the key things you should consider when evaluating a Plex share service.


## Quantity and Quality

To evaluate a Plex share, you can gather information about the library content that is offered. Start by selecting a library and switching from "Recommended" to "Library" view. At the top of the screen, you can see the total number of movies and TV shows available. Scroll through the selection to check if the titles you want to watch are available.

To evaluate the quality of the library, hover over the movies that interest you and click on the three dots at the bottom right of the poster. Then select "Get Info" to view details about the file being streamed. Note the video resolution, bitrate, and file size, as higher attributes generally indicate better quality.

It's important to check a variety of old and new titles from different genres to understand the scope of the library. For example, the newest Hollywood blockbuster might be available in 1080p Remux with a 30GB size, but other titles may be low-quality encodes at 1080p and 2GB.

Now that you have evaluated the quantity and quality of the titles in the library, it's important to understand the different types of file quality that may be available. Generally, there are three types of file quality: scene encodes, P2P encodes, and remux.

### Scene Encodes *(2-6Mbps at 1080p)*

Scene encodes refer to video files that have been compressed using a specific set of encoding standards created by the Scene release groups. These standards ensure that the encoded video file is of a consistent quality and format across all Scene releases, making it easy for users to know what to expect from each release.

Those who are primarily concerned with smaller file sizes and faster downloads may choose scene encodes over P2P and remux. Scene releases are typically available soon after the movie or TV show has been officially released, and the encoding process used by the scene groups usually results in a smaller file size than remux or P2P encodes. However, this often comes at the cost of reduced video and audio quality. Therefore, scene encodes may be appealing to those with slower internet connections or those who don't have a lot of storage space available for large media files. Additionally, those who are less discerning when it comes to video quality may also opt for scene encodes over other options.

### Peer-to-Peer Encodes *(4-12Mbps at 1080p)*

P2P (peer-to-peer) encodes, also known as user-generated encodes, are files that have been encoded by individual users or small groups of users, rather than larger release groups like the Scene. P2P encodes are often considered to have better quality than Scene encodes, as they are typically encoded from higher-quality sources, such as Blu-ray discs or web-dl downloads. However, the quality of P2P encodes can vary widely depending on the skill and equipment of the individual or group doing the encoding. Unlike Scene encodes, P2P encodes do not follow a specific set of rules or standards, so the quality and size of the files can vary greatly. P2P encodes are often favored by users who are looking for high-quality releases that may not have been released by the Scene yet, or who are looking for niche or lesser-known content.

People who are looking for a balance between file size and quality may choose P2P encodes over scene or remux files. P2P encodes are typically smaller in size compared to remux files but are of better quality than scene encodes. Additionally, P2P encoders often tweak their settings to achieve the best possible balance between file size and quality, resulting in a file that is optimized for streaming. This makes P2P encodes a popular choice for those who have limited storage space, slower internet speeds, or who simply want to save on bandwidth usage while still enjoying high-quality video playback.

### Remux *(20-80Mbps at 1080p)*

A remux file is a high-quality digital copy of a Blu-ray or UHD Blu-ray disc, which has been created by extracting the original video, audio, and subtitle streams from the disc without any re-encoding. This means that the video quality is exactly the same as the original disc and can be played back at the highest possible bitrate that the disc supports. Additionally, remux files typically include lossless audio tracks such as DTS-HD Master Audio or Dolby TrueHD, which provide the highest quality audio experience. Remux files are considered to be the highest quality releases available for streaming and are highly sought after by movie enthusiasts who want the best possible playback experience, but are also are typically very large in size, which can be a drawback for people with limited storage space or slower internet connections.

## Location / Peering

Sure! Here's a revised version:

When evaluating a Plex share, it's important to take into account the location and upload speed of the server. However, the internet is a complex system, and just because a server has a 1Gbit upload and you have a 1Gbit download speed, it doesn't mean you will always be able to achieve those speeds. Your location, as well as the quality of your ISP and server's network, play a crucial role in the speeds you will realistically see. For instance, a server located in Africa might only be able to upload at 2Mbit to you, while a server located a few cities away from you might be able to saturate your full 1Gbit connection.

Due to these variables, it's impossible to know the actual speed you will get from an advertised server without trying it out. This is why getting a trial is so important. Once you have access, the best way to test everything is to simply play whatever content you want. However, it's a good idea to first figure out the theoretical maximum of the server so that you can determine what you will or won't be able to watch. One way to do this is by playing the highest bitrate file available on the server and checking its bitrate information. If you're allowed multiple streams, you can open multiple browser tabs, the Plex app on your phone, and your TV to play multiple movies at the same time, mimicking the maximum use case. Even if you don't plan on watching 30Mbps Remuxes right away, it's still worth checking if you can, just in case you decide to do so in the future.

To get the smoothest streaming experience, you should ideally be able to achieve 2x the average bitrate displayed in the file, to account for spikes in network traffic. To get a rough estimate of your speed to the media server, you can visit our speed test page. Remember that the quality of your ISP and server's network, as well as your location, can significantly impact your actual speeds, so it's important to test the server thoroughly before committing to a subscription.

???+ info "Content Delivery Network"

    A Content Delivery Network (CDN) is a distributed network of servers that work together to deliver content quickly to users. When a user requests content, such as a video, the CDN automatically determines the server closest to the user and delivers the content from that server. This provides faster load times and better quality playback, as the content is delivered from a server that is geographically closer to the user. CDNs also reduce the load on individual servers, improving overall performance and reducing the likelihood of server downtime. Many Plex share services use CDNs to improve the quality of playback for their users.

## Time

The time of day can also play a significant role in the quality of your streaming experience. Many servers have limited resources, and during peak usage times, such as in the evening, you might experience slow or choppy playback. Conversely, during off-peak hours, you might find that the server performs better, and you can stream high-quality content with ease. This issue can arise if the server is oversold to maximize profits, much like how ISPs oversell their network capacity. The assumption here is that not everyone will be using the server simultaneously, which is often true. However, it is important to consider when you plan to watch and ensure that you choose a time when the server is not overloaded with other users.
