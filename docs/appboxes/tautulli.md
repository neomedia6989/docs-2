# Tautulli

Tautulli is a powerful tool that can be used to monitor and track activity on a Plex Media Server. It can be used to track things like who is watching what, when they are watching it, and how they are watching it. Tautulli can also be used to generate notifications, such as when someone starts watching a new movie or TV show.

To use Tautulli, you first need to install it via the Kronos dashboard. Once it is installed, you can configure it and start using it to monitor your Plex Media Server.

???+ tip "Varys: an iOS Alternative"
    
    Varys for Plex is a third-party app that connects to your Plex Media Server and uses data from Tautulli to provide you with a more detailed look at your Plex Media Server's activity. For example, you can see how many users are currently streaming from your server, what they are streaming, and how much bandwidth they are using. You can also see what media items are most popular, and how much storage space they are using. Varys is a paid application, but drastically extends the functionality of Tautulli to include features such as the [Plex Dance](https://www.plexopedia.com/plex-media-server/general/plex-dance/).

Below, you will provide an overview of Tautulli and its features, benefits, and how to use it. It will also include links to further documentation and support resources.

### Monitor usage

Tautulli can help you monitor how much of your appbox's resources are being used by your users. You can use this information to determine if you need to upgrade your appbox or if you need to limit the number of users who can access your server at the same time. You can also track who is transcoding and how many users are actively transcoding and watching at the same time. This will help you determine if it is needed to upgrade plans. Please note that audio transcoding is not counted and users should mostly be concerned about video transcoding.

### Track Activity

Tautulli can help you track what your users are watching and when they are watching it. This information can be used to determine what content is popular and what content is not. For example, you can create a collection of the most popular movies on your appbox, or you can create a collection of movies that you think your users would enjoy, based on their past viewing habits.

<figure markdown>
![(/media/tautulli-monitor.png)](https://docs.blackbeard.media/media/tautulli-monitor.png)
  <figcaption></figcaption>
</figure>

### Generate Notifications

Tautulli can generate notifications when certain events occur, such as when a new user starts watching a movie or TV show. These notifications can be used to provide a better experience for your users by letting them know when new content is available or when they have new messages from other users.

???+ tip "Get Notified About Transcoding"
    
    Tautulli offers a notification system that allows you to receive alerts whenever a user starts transcoding a media file. This can be useful in situations where you want to monitor the performance of your server or want to ensure that your users are not overloading your system. To set up this notification, you can create a custom notification agent within Tautulli and set it to trigger whenever a user begins transcoding. From there, you can choose to receive an email, push notification, or other alert. With this feature, you can stay on top of your server's performance and ensure a smooth streaming experience for all users.
    
### Provide Access to Watch History

Tautulli can provide your users with access to their watch history, which can be used to help them find the content they are looking for or to help them keep track of what they have watched. This information can also be helpful for users who want to track their viewing habits over time or who want to identify any trends in their viewing. In addition, Tautulli can help users troubleshoot problems by showing if they are direct playing or transcoding content as well as the required bandwidth of the file they are watching.

<figure markdown>
![(/media/tautulli-track.png)](https://docs.blackbeard.media/media/tautulli-track.png)
  <figcaption></figcaption>
</figure>

#### Enable 'Allow Guest Access to Tautulli'
 
Tautulli requires you to enable guest access, which is a useful feature if you want to allow your friends and family to access your Plex Media Server without giving them full access to your account. Enabling guest access is a straightforward process, and in the following guide, we will show you how to do it step by step.

1. Open Tautulli on your web browser and log in.
2. Click on the Settings icon in the top-right corner.
3. Click on the 'Web Interface' tab.
4. Toggle the switch next to 'Allow Guest Access to Tautulli'.
5. Click on the 'Users' tab.
6. Click on 'Edit Mode' in the top-right corner.
7. Toggle the lock icon next to each user you want to enable guest access for.
8. Click on 'Save Changes' in the top-right corner to save your changes.

By following these steps, you can enable guest access to Tautulli and grant specific users the ability to access Tautulli as a guest.

??? tip "Automate Guest Access with Python"
    
    By default, Tautulli will not have guest access enabled for new users even after you allow guest access for all users. To automate the process of enabling guest access for Tautulli users, you can use a Python script like the one below. Before running the script, you will need to configure it with your Tautulli URL and API key. We recommend setting the script to run on a cron schedule so that it runs automatically at set intervals. Please note that you still need to enable 'Allow Guest Access to Tautulli'.
    
    ```  py title="Enable Guest Access"                                                                    
    #!/usr/bin/env python
    # -*- coding: utf-8 -*-

    """Enable or disable all users remote access to Tautulli.

    Author: DirtyCajunRice
    Requires: requests, python3.6+
    """
    from __future__ import print_function
    from __future__ import unicode_literals

    from requests import Session
    from json.decoder import JSONDecodeError
    
    # Change to 'False' to disable all guest access #
    ENABLE_REMOTE_ACCESS = True

    TAUTULLI_URL = 'ADD URL HERE'
    TAUTULLI_API_KEY = 'ADD API KEY HERE'

    # Do not edit past this line #
    session = Session()
    session.params = {'apikey': TAUTULLI_API_KEY}
    formatted_url = f'{TAUTULLI_URL}/api/v2'

    request = session.get(formatted_url, params={'cmd': 'get_users'})

    tautulli_users = None
    try:
        tautulli_users = request.json()['response']['data']
    except JSONDecodeError:
        exit("Error talking to Tautulli API, please check your TAUTULLI_URL")

    allow_guest = 1 if ENABLE_REMOTE_ACCESS else 0
    string_representation = 'Enabled' if ENABLE_REMOTE_ACCESS else 'Disabled'

    users_to_change = [user for user in tautulli_users if user['allow_guest'] != allow_guest]

    if users_to_change:
        for user in users_to_change:
            # Redefine ALL params because of Tautulli edit_user API bug
            params = {
                'cmd': 'edit_user',
                'user_id': user['user_id'],
                'friendly_name': user['friendly_name'],
                'keep_history': user['keep_history'],
                'allow_guest': allow_guest
            }
            changed_user = session.get(formatted_url, params=params)
            print(f"{string_representation} guest access for {user['friendly_name']}")
    else:
        print(f'No users to {string_representation.lower()[:-1]}')
    ```

### Generate Reports

Tautulli can also be used to generate reports that can be used to track progress over time, identify trends, and make informed decisions about how to improve to improve the appbox. For example, you can use a report to see how many users you have added in the past month, or to see which shows and movies are most popular. You can also see how much bandwidth your viewers are using, or to see if any of your users are constantly transcoding by viewing their play history.

<figure markdown>
![(/media/tautulli-graphs.png)](https://docs.blackbeard.media/media/tautulli-graphs.png)
  <figcaption></figcaption>
</figure>
