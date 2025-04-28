# Custom Tools for Building WordCamp Content

WordCamp.org provides organizers with numerous tools for managing a WordCamp. Using the custom plugins and post types, you can administer ticket sales, communicate with attendees, wrangle information on speakers, sponsors, and sessions; even on your organizing team. Then you can display it all on your public site using custom shortcodes and attributes.

When you’re in your admin panel, you’ll see several additional post types available: [tickets](#tickets), [speakers](#speakers), [sessions](#sessions), [sponsors](#sponsors), and [organizers](#organizers). It’s important to fill them out for your event, since the collected data might be aggregated and used after your event is over. We even have a way to [automatically create a grid schedule](#schedule) on your site! In this article, we’ll cover the basics of using these tools with your chosen theme.

In addition to these tools, if you look under the Posts and Pages screens in the admin panel, you’ll find some stubs for content that frequently appears on WordCamp sites. You can build off of these stubs, or trash them and start fresh with your own content.

## Tickets and Attendees

Most WordCamps sell tickets and manage attendee information via the [CampTix](https://wordpress.org/plugins/camptix/) plugin. Check out our [CampTix documentation](https://make.wordpress.org/community/handbook/wordcamp-organizer-handbook/first-steps/web-presence/using-camptix-event-ticketing-plugin/) for detailed instructions on using each of its features.

## Third-Party Services

There are various shortcodes you can use to embed data from third-party services on your WordCamp.org site, such as Livestream.com, Google Forms, MailChimp, Campaign Monitor, and many more. Please refer to the [Shortcode Embeds](https://make.wordpress.org/community/handbook/wordcamp-organizer-handbook/first-steps/web-presence/setting-up-your-wordcamp-theme/shortcode-embeds/) page for more information, and if there’s a third-party service that you think we’re missing, let us know at support@wordcamp.org.

## Speakers

Your site has a “Call for Speakers” post automatically created with a `Draft` status. It includes a contact form, and if you publish that post, form submissions will automatically create new Speaker and Session posts with a `Draft` status. You can then publish the speakers/sessions that you accept, and delete the ones you don’t.

You can also manually create new speaker posts. Use the large title area for the full name of the speaker, and the content area for a short description or speaker bio. You’ll also see fields for “Gravatar Email”, and “WordPress.org Username”; make sure you fill them out with the speaker’s e-mail address and username. Also make sure your speakers are published (as opposed to set as drafts, pending, etc), otherwise they will be hidden from the front-end. You can also create Speaker Groups, and add speakers to the different groups.

## Sessions

If you use the “Call for Speakers” post mentioned above, form submissions will automatically create new Speaker and Session posts with a `Draft` status. You can then publish the speakers/sessions that you accept, and delete the ones you don’t.

You can also manually add/edit session posts your speaker’s bios, and session descriptions. Session info can be added in the Document Settings sidebar. Don’t forget to specify the speaker for each session that you create. If a session is run by more than one speaker, like a panel, you can assign several speakers to it. If you’re running sessions in more than one track, like Users Track vs. Developers Track, make sure you assign the right track to every session. Tracks work the same way Categories do. After the event, you can add links to the slides and video on WordPress.tv, and they’ll be added to the session page.

## Sponsors

Your site has a drafted “Call for Sponsors” post, and it works similarly to the Call for Speakers post described above. Form submissions will automatically create new Sponsor posts with a `Draft` status. You can then publish the sponsors that you accept, and delete the ones you don’t.

When starting with sponsors, make sure you define your sponsor levels first, such as Gold, Silver and Bronze. By default, sponsor levels will be ordered by the level name, but you can set a manual order in Sponsors → Order Sponsor Levels by dragging levels up or down.

When adding a new sponsor, the title is used the sponsor’s name, and the content is used as the sponsor’s description/blurb (keep it short — people should be able to read these quickly!).

## Organizers

If you’d like to help attendees get to know the organizing team, you can add a bio for each members in the Organizers menu, and then display that content using the Organizers block (found in the WordCamp section).

## Volunteers

Your site has a drafted “Call for Volunteers” post, and it works similarly to the Call for Speakers post described above. Form submissions will automatically create new Volunteer posts with a `Draft` status. You can then publish the volunteers that you accept, and delete the ones you don’t.

You can also manually add/edit volunteers if you choose.

## Displaying content

There are a few custom blocks available to show the WordCamp-specific content, and these can be used in posts, pages, and the Site Editor (if you’re using a block theme, like Twenty Twenty-Two or Twenty Twenty-Three). You can add these directly to the content, or start with a block pattern.

### Patterns

Find these in the Patterns tab, click “Explore all patterns” to see the modal. This uses your live content to show a preview, so if you don’t have speakers, sessions, etc published yet, it will show “No results found.” There are also header & call to action patterns available.

[![Screenshot of the editor, pattern explorer modal, showing the WordCamp category & pattern previews.](https://make.wordpress.org/community/files/2023/06/patterns-1024x704.png)](https://make.wordpress.org/community/files/2023/06/patterns.png)

Organizers

*   Organizer grid, centered
*   ​Organizer list with bio

Sessions

*   ​Session list with description
*   ​Session list, centered

Speakers

*   ​Basic speaker grid
*   ​Speaker grid with bio
*   ​Speaker grid, centered
*   ​Basic speaker list
*   ​Speaker list with bio

Sponsors

*   Basic sponsor grid

Header

*   Centered header with menu
*   ​Short header with button

Call to action

*   ​Hero with bottom left content
*   ​Hero with center left content
*   ​Hero with centered content
*   ​Hero with top left content

### Query blocks

The patterns above use these blocks to list out the WordCamp content. These are all variations on the Query Loop block, so you can control what’s displayed for each item. For more details, [check out the Query Loop documentation](https://wordpress.org/documentation/article/query-loop-block/#how-to-customize-the-appearance).

It’s recommended to use the patterns, but if you want to create your own list, you can insert these blocks.

![](https://make.wordpress.org/community/files/2023/06/Organizers-Query.png)  
Organizers List

![](https://make.wordpress.org/community/files/2023/06/Sessions-Query.png)  
Sessions List

![](https://make.wordpress.org/community/files/2023/06/Speakers-Query.png)  
Speakers List

![](https://make.wordpress.org/community/files/2023/06/Sponsors-Query.png)  
Sponsors List

They’ll insert with a starter template using theme blocks (see below), but you can add or remove anything, and each block can be styled using block styles.

### Site Editor

If you’re using a block theme (Twenty Twenty-Two or Twenty Twenty-Three), you can use [the Site Editor](https://wordpress.org/documentation/article/site-editor/) to customize your whole site. New sites are also set up with custom templates for each content type (organizers, sessions, speakers, sponsors). These have basic information by default, but can also be fully customized.

[![Screenshot of Single item: Organizer template in Site Editor.](https://make.wordpress.org/community/files/2023/06/template-organizer-1024x683.png)](https://make.wordpress.org/community/files/2023/06/template-organizer.png)

[![Screenshot of Single item: Speaker template in Site Editor.](https://make.wordpress.org/community/files/2023/06/template-speaker-1024x759.png)](https://make.wordpress.org/community/files/2023/06/template-speaker.png)

[![Screenshot of Single item: Sponsor template in Site Editor.](https://make.wordpress.org/community/files/2023/06/template-sponsor-1024x823.png)](https://make.wordpress.org/community/files/2023/06/template-sponsor.png)

[![Screenshot of Single item: Session template in Site Editor.](https://make.wordpress.org/community/files/2023/06/template-session.png)](https://make.wordpress.org/community/files/2023/06/template-session.png)

### Theme blocks

Theme blocks are blocks that replicate template tags from classic themes, like Post Title, Post Author, etc. They can be used in the Site Editor (in block-based themes) to build your site.

There are a few custom WordCamp blocks that you can use for each content type. These display some piece of information, and can also be used in the post type or in a Query block (one of the 4 listed above). They need to be inside the content type they’re referencing — adding a Session Tracks block to a Session will show the tracks, but that block won’t show anything on an Organizer post, for example.

The default theme blocks (Post Title, Post Content, etc) are also supported for all custom content.

All of the following blocks support basic color and spacing controls.

For Organizers

*   **Avatar** An image for the organizer, either featured image (if there is one), or the Gravatar attached to their listed user account. It can be square or round, with sizes from 24px to 512px square, and can link to the organizer.
*   **Organizer Teams** The Teams (taxonomy) attached to this organizer.

For Sessions

*   **Session Categories** The Categories (taxonomy) attached to this session.
*   **Session Date & Time** The session’s date & time, with options for format. The time is always shown in the site’s timezone.
*   **Session Slides** A link to the slides URL.
*   **Session Speakers** The speakers for this session, optionally linking to their speaker page(s).
*   **Session Tracks** The Tracks (taxonomy) attached to this session.
*   **Session Video** A link to the video URL.

For Speakers

*   **Avatar** An image for the speaker, either featured image (if there is one), or the Gravatar attached to the given email. It can be square or round, with sizes from 24px to 512px square, and can link to the organizer.
*   **Speaker Sessions** The sessions that this speaker is presenting. Defaults to showing just title, but date, time, and track can be enabled. The title can link to the session.

## Schedule

After entering the sessions, you can use the Schedule block to display them in an easy-to-read table, sorted by the track and date/time.

You can also add breaks into the schedule by creating sessions and selecting the “Break, Lunch, etc” type from the Session Info metabox. Once you assign the break to all of the tracks that it will cover (in the Tracks metabox), it will automatically show up in the schedule.

The *Single-Column Layout* block style can be useful on camps that have a lot of tracks, or have a narrow layout.

## Live Schedule

The Live Schedule block shows the sessions that are currently going on right now. Many camps add it to their homepage during their event, so that attendees can quickly choose which session to attend, without having to look through the full schedule.

## YouTube Live Chat

If you’re streaming your sessions on YouTube, the *YouTube Live Chat* block can be used to embed the corresponding chat, so that you can foster community with people who couldn’t attend in person.

It’s recommended to have someone moderating the chat, in case any trolls try to disrupt it.

## Block configuration

The Speakers, Sessions, Sponsors and Organizers blocks all have similar options, so they’re all documented here. Ask in *[#wordcamp-meta](https://make.wordpress.org/community/tag/wordcamp-meta/)* if anything is unclear.

In the Block Toolbar, you can change between list and grid, and if your theme supports it, you can make the block wide or full-width.

A grid of items can be 2, 3, or 4 columns, this is changed in the sidebar under Grid Layout. If you don’t see a sidebar, click the 3 dots in the toolbar and “Show block settings”

Also in the sidebar, you can control the Avatar (speakers, organizers) or Featured Image (sessions, sponsors) for each item. You can show or hide the image, and control its size and alignment here.

Under Content Settings (still in the sidebar), you can control the content for each item. Try these out yourself, you can see the immediate preview in the editor.

## Translation

Some of the text on your site will be output by plugins and themes, and it might not have been translated into your language yet. If you find words that aren’t translated, you can help fix that!

1.  Open [the WordCamp project](https://translate.wordpress.org/projects/meta/wordcamp) at translate.wordpress.org
2.  Find your locale in the list
3.  Review [the Translator Handbook](https://make.wordpress.org/polyglots/handbook/tools/glotpress-translate-wordpress-org/) to learn how to translate strings

The translated strings should appear on your site automatically within 24 hours of being approved by an editor. If they don’t, leave a message in *the [#meta-wordcamp](https://make.wordpress.org/community/tag/meta-wordcamp/)* channel on [Slack](https://chat.wordpress.org) and one of the developers will help.

## Miscellaneous

Check out the **WordCamp** section of the block inserter for all of our custom blocks.

**Embed a menu** in a post or page with the \[menu\] shortcode

\[menu menu="Menu Name" menu\_class="extra-css-class" depth="1"\]

Here is [a quiz](https://wordpress.org/contributor-training/quiz/custom-tools-for-building-wordcamp-content-2/) on this article. Read [quizzes](https://make.wordpress.org/community/handbook/wordcamp-organizer/quizzes/) page if you have any questions about quizzes and how to navigate them.

*   [To-do](# "To-do")