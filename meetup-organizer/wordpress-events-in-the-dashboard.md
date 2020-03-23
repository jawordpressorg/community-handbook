# WordPress Events in the Dashboard

Since WordPress 4.8, there has been [Dashboard widget](https://make.wordpress.org/community/2017/06/07/wordpress-4-8-adds-events-to-the-dashboard-news-widget/) showing upcoming local events. The widgetWidget A WordPress Widget is a small block that performs a specific function. You can add these widgets in sidebars also known as widget-ready areas on your web page. WordPress widgets were originally created to provide a simple and easy-to-use way of giving design and structure control of the WordPress theme to the user. shows upcoming WordCamps and meetupMeetup All local/regional gatherings that are officially a part of the WordPress world but are not WordCamps are organized through [https://www.meetup.com/](https://www.meetup.com/). A meetup is typically a chance for local WordPress users to get together and share new ideas and seek help from one another. Searching for ‘WordPress’ on meetup.com will help you find options in your area. events inside wp-admin, making it easier for people to find out what’s happening in their local communities.  

If a site has multiple users, each one will be shown the events that are close to their individual location. The dashboard widget will try to automatically detect their location, but they’ll also be able to enter any city they like. Users can click on a pencil icon and type in the location of their choice. Automatic location detection and the event data for the pluginPlugin A plugin is a piece of software containing a group of functions that can be added to a WordPress website. They can extend functionality or add new features to your WordPress websites. WordPress plugins are written in the PHP programming language and integrate seamlessly with WordPress. These can be free in the WordPress.org Plugin Directory https://wordpress.org/plugins/ or can be cost-based plugin from a third-party is provided by an [api.wordpress.org endpoint](https://codex.wordpress.org/WordPress.org_API#Events).  

The radius for pulling events from users location is 100 kilometers for meetups and 350 kilometers for WordCamps. Events for each location are cached for 12 hours.

*   ![](https://make.wordpress.org/community/files/2018/08/PixelSnap-2018-07-30-at-22.24.03.png)
    
    Dashboard widget showing upcoming WordPress events based on detected user location.
    
*   ![](https://make.wordpress.org/community/files/2018/08/PixelSnap-2018-07-30-at-22.27.01.png)
    
    Dashboard widget showing upcoming WordPress events based on location user inputted
    

### How can I attend an event that I see in the WordPress Events and News widget?

If you see an event on the Events and News widget that you would like to attend, just click on the event name to be taken to a page with more information. You’ll be able to RSVP for the meetup event via meetup.com, or buy a ticket for a WordCampWordCamp WordCamps are casual, locally-organized conferences covering everything related to WordPress. They're one of the places where the WordPress community comes together to teach one another what they’ve learned throughout the year and share the joy. [Learn more](https://central.wordcamp.org/about/). on the local WordCamp website. If you have any trouble, you can email [support@wordcamp.org](mailto:support@wordcamp.org) for more information. And welcome to the WordPress community!

### I belong to a WordPress meetup group, and our events don’t show up on the widget! Is it broken?

Only groups that are part of the WordPress meetup chapter program are listed on the widget. If your local group’s events aren’t showing up, it’s possible that it just hasn’t joined the chapter program yet! Joining is free, and requires following a few good-faith rules that were created by a group of volunteer meetup organizers. Information on joining the WordPress meetup program can be found [here](https://make.wordpress.org/community/meetups/).

### What information is collected, and what is it used for?

The plugin sends each user’s timezone, locale, and partially anonymized IP address to api.wordpress.orgWordPress.org The community site where WordPress code is created and shared by the users. This is where you can download the source code for WordPress core, plugins and themes as well as the central location for community conversations and organization. [https://wordpress.org/](https://wordpress.org/), in order to determine their location, so that they can be shown events that are close to that location. If the user requests events near a specific city, then that is also sent. The data is not stored permanently, not used for any other purpose, and not shared with anyone outside of WordPress.org, with the exception of any conditions covered in the [WordPress.org privacy policy](https://wordpress.org/about/privacy/).

### How to debug functionality and report a bug?

*Following instructions and details are bit developer orientated. If you don’t feel comfortable with code and technical terms, the [#community-events](https://make.wordpress.org/community/tag/community-events/)* [*Slack*](https://make.wordpress.org/chat/) *channel is the place to get help and report problems with WordPress Events functionality.*  

Before submitting a bug report, please check that you are not in a local development environment and expecting Events APIAPI An API or Application Programming Interface is a software intermediary that allows programs to interact with each other and share data in limited, clearly defined ways. to detect your location. That will not work, since location detection can’t be done with IP address of local environment. Currently, the ip2location database is used as the source for detection and the data is updated oncea month.  

On the Dashboard side, the Events widget saves a few database records to store necessary data. One is \`community-events-location\` inside \`wp\_usermeta\`, which stores either the location detected or the location manually set by each user. The other record is a transient to store the cached event data. That transient is shared across users, so if you have 500 users, but they’re all in Seattle, then there will only be 1 transient to cache the events for all of them.  

If you are availabe to add plugins and read error logs, add this plugin to your \`mu-plugins\` [https://core.trac.wordpress.org/raw-attachment/ticket/41217/log-community-events-requests.php](https://core.trac.wordpress.org/raw-attachment/ticket/41217/log-community-events-requests.php). It will give you the exact api.wordpress.org/events URLURL A specific web address of a website or web page on the Internet, such as a website’s URL www.wordpress.org that is being queried, making it easier to troubleshoot parameters.

Possible bugs can be discussed in [#meta-wordcamp](https://make.wordpress.org/community/tag/meta-wordcamp/) on [Slack](https://make.wordpress.org/chat/) and reported in [Meta Trac](https://meta.trac.wordpress.org/) ticket if the bug seems to be in the Events API. Bugs in Dashboard widget can be reported in [Core Trac](https://core.trac.wordpress.org/).

*   [To-do](# "To-do")