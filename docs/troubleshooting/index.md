# Troubleshooting & Tips

We understand that technology can sometimes be tricky, but don't worry, we have got you covered. In this section, beyond the general tips below, we have organized our tips and solutions into two categories to make it easier for you to navigate: Plex Clients and Plex Servers. 

If you are an end user streaming content, our Plex Clients section provides tips on how to optimize your streaming experience, troubleshoot common issues, and get the most out of your device.

If you are an appbox subscriber running a Plex Server, our Plex Servers section provides helpful solutions to common issues, tips on how to optimize your server's performance, and advice on how to troubleshoot problems with your server.

## Understanding Internet Speed and Your Connection

Internet speed is like how fast you can ride your bike to get to a friend's house. When you want to watch a video on the internet, your computer has to ask the internet to send it the video. If your internet speed is slow, it might take a long time for your computer to get the video, like when you ride your bike slowly to get to your friend's house.

But, if your internet speed is fast, your computer can get the video really quickly, like when you ride your bike really fast to get to your friend's house.

Sometimes, the internet might not be fast enough to send the video to your computer quickly, even if your internet speed is really fast. This can happen when the video is coming from far away, like from another country.

That's why we have something called a CDN (Content Delivery Network) that helps make sure the video gets to your computer as fast as possible. It's like having a special bike lane that's smoother and faster so you can get to your friend's house more quickly.

If you want to check how fast your internet is, you can use a special tool called a speed test. We have two different speed tests you can use: [one to test your direct connection to our servers](https://speedtest.blackbeard.brrrrrr.net/), and [another to test your speed to the closest CDN node](https://speedtest.brrrrrr.net/). It's like checking how fast you can ride your bike in different directions to get to your friend's house.

If your speed test results are poor, it might mean that your internet speed is too slow. It's like when you ride your bike too slowly and it takes a long time to get to your friend's house. In that case, you might need to ask your parents if they can help you get a faster internet speed so you can watch videos more quickly.

## Ethernet vs. Wi-Fi for Video Streaming

When you use the internet to watch a video, your computer or tablet talks to the internet using something called Wi-Fi or Ethernet. Wi-Fi is like a magic spell that lets your computer talk to the internet without any wires. Ethernet is like a magic string that lets your computer talk to the internet with a special wire.

Now, if you use Wi-Fi, it's like trying to have a conversation with your friend while you're running around in the park. Sometimes you might hear your friend, but other times it might be hard to hear them or you might not hear them at all. This is because Wi-Fi can get interrupted by things like walls, other people's Wi-Fi, or even a microwave oven!

On the other hand, if you use Ethernet, it's like having a conversation with your friend while sitting at a table. You can hear your friend very clearly because there's nothing in the way. This is because Ethernet uses a special wire that goes directly from your computer to the internet.

So, if you want to watch videos on the internet without any interruptions, it's a good idea to use Ethernet instead of Wi-Fi. That way, your computer can talk to the internet without any obstacles in the way, and you can watch your videos smoothly and without any interruptions.

## Closing Apps and Disconnecting Devices to Improve Video Streaming

Have you ever played with too many toys at the same time and couldn't find the one you wanted to play with? That's kind of like what happens when there are too many devices using the internet at the same time. When that happens, the internet can get slow and it might take longer for your videos to load. So, it's a good idea to close any apps that are not being used and to disconnect any devices that are not being used, so that your video streaming can be fast and smooth!

## Improving Streaming Performance: Clearing Cache and Cookies

When you watch videos on your computer or TV, sometimes little bits and pieces of the videos get stored in your device so they can play faster later on. These bits and pieces are called "cache". Cookies are little pieces of information that websites leave on your device so they can remember your preferences.

Sometimes, the cache and cookies can build up and make the videos load slowly. To make them play faster, you can clear the cache and cookies. Here's how you can do it on different devices:

- **For smart TVs and streaming devices:** Go to the settings on your TV or streaming device and find the option to clear the cache and cookies. You may need to look in the "System" or "General" settings. Follow the prompts to clear the cache and cookies.
- **For PCs:** If you're using a web browser like Chrome, Firefox or Edge, you can usually clear the cache and cookies by going to the settings or options menu. Look for the "Privacy" or "Security" section, and you should find an option to clear browsing data. Follow the prompts to clear the cache and cookies
- **For consoles:** Clearing the cache and cookies may vary depending on the type of console you have. Look for the option to clear cache and cookies in the settings or preferences menu, and follow the prompts to clear them.

???+ failure "Restarting / Uninstalling Plex"
    
    If you're still experiencing issues with your video streaming quality, you can try signing out of the app and signing back in to see if that helps. If all else fails, you can try uninstalling and reinstalling the app to see if that helps improve performance.

## Improving Video Streaming by Changing DNS

When you want to watch a video on the internet, you have to tell your computer where to find it. It's like telling your friend where to find a toy in your messy room.

DNS (Domain Name System) is like a map that helps your computer find the video you want to watch. It tells your computer the address where the video is located on the internet, just like your mom might tell your friend the location of the toy in your room.

Sometimes, the map your computer is using might not be the best one, and it might take a long time for your computer to find the video. It's like trying to find a toy in your room using a really old and messy map.

By changing your DNS to a better one, it's like getting a new and improved map that helps your computer find the video faster. It's like having a new and organized map of your room that makes it easier for your friend to find the toy. So, changing your DNS can make it faster and easier for your computer to find and play the video you want to watch!

Here's how you can change your DNS settings on various devices:

### On a PC (Windows)

1. Open the Start menu and click on the Settings icon (gear icon / :fontawesome-solid-gear: ).
2. Click on "Network & Internet".
3. Click on "Change adapter options".
4. Right-click on the network connection you want to change and select "Properties".
5. Scroll down and select "Internet Protocol Version 4 (TCP/IPv4)" and click on "Properties".
6. Select "Use the following DNS server addresses" and enter 1.1.1.1 and 1.0.0.1 or 8.8.8.8 and 8.8.4.4 for Cloudflare or Google DNS respectively.
7. Click on "OK" to save the changes.

### On a Mac

1. Click on the Apple menu and select "System Preferences".
2. Click on "Network".
3. Select the network connection you want to change and click on "Advanced".
4. Click on the "DNS" tab.
5. Click on the "+" button to add a new DNS server and enter 1.1.1.1 and 1.0.0.1 or 8.8.8.8 and 8.8.4.4 for Cloudflare or Google DNS respectively.
6. Click on "OK" to save the changes.

### On a Smart TV

Note that the steps may vary depending on your TV brand and model.

1. Press the "Menu" button on your remote.
2. Go to "Settings" or "Network Settings".
3. Select "DNS Settings" or "Manual DNS Settings".
4. Enter 1.1.1.1 and 1.0.0.1 or 8.8.8.8 and 8.8.4.4 for Cloudflare or Google DNS respectively.
5. Save the changes and restart your TV.

### On a Streaming Device (Android TV, Apple TV, Fire TV, Roku, etc.)

Note that the steps may vary depending on your streaming device.

1. Go to the "Settings" menu on your device.
2. Select "Network" or "Internet".
3. Select "DNS Settings" or "Configure DNS".
4. Select "Manual" or "Custom".
5. Enter 1.1.1.1 and 1.0.0.1 or 8.8.8.8 and 8.8.4.4 for Cloudflare or Google DNS respectively.
6. Save the changes and restart your device.

By changing your DNS server to 1.1.1.1 or 8.8.8.8, you should notice a significant improvement in your internet connection speed and video streaming quality. If you are still experiencing issues after changing your DNS, there may be other factors affecting your internet connection such as your router, network congestion or hardware issues.

## Using a VPN for Video Streaming: Benefits and Considerations

Watching videos on the internet is like getting a pizza delivered to your house. Sometimes, the pizza delivery person has to take a really long and slow route to get to your house, and it can take a long time for your pizza to arrive.

A VPN (Virtual Private Network) is like having a special delivery person who knows all the best shortcuts and can get your pizza to you faster. They can avoid traffic and take a faster route to your house, which means you get your pizza quicker!

But, a VPN can also help keep your information safe and secure while you're watching videos. It's like having a secret password that only you and the pizza delivery person know, so no one else can steal your pizza or your information.

However, our video service already has a special delivery person that knows all the best routes and shortcuts to get your videos to you quickly. It's like having a magic pizza delivery person who always knows the fastest way to your house. This way, you can watch your videos quickly without needing to use a VPN.

So, while a VPN can make your videos even faster and keep your information secure, most people don't need to use one because our service already has a magic delivery person to make sure your videos get to you quickly and easily.

## Disable Hardware Acceleration

Hardware acceleration is like having a helper to do some tasks for you so that you don't have to do them yourself. But sometimes, this helper can make things slower or not work properly.

So, when you're watching videos on some devices, like a computer, you can turn off this helper to try to make the videos play better. This might help the videos play more smoothly and not freeze or stop in the middle.

For some devices, like Apple TV, there's also a special setting you can choose that's called "Old" or "Legacy" player. This can also help the videos play better. It's like using an older version of the helper that might work better for some videos.
