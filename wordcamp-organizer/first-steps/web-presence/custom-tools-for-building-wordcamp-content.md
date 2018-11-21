# Custom Tools for Building WordCamp Content

WordCamp.org provides organizers with numerous tools for managing a WordCamp. Using the custom plugins and post types, you can administer ticket sales, communicate with attendees, wrangle information on speakers, sponsors, and sessions; even on your organizing team. Then you can display it all on your public site using custom shortcodes and attributes.

When you’re in your admin panel, you’ll see several additional post types available: [tickets](#tickets), [speakers](#speakers), [sessions](#sessions), [sponsors](#sponsors), and [organizers](#organizers). It’s important to fill them out for your event, since the collected data might be aggregated and used after your event is over. We even have a way to [automatically create a grid schedule](#schedule) on your site! In this article, we’ll cover the basics of using these tools with your chosen theme.

In addition to these tools, if you look under the Posts and Pages screens in the admin panel, you’ll find some stubs for content that frequently appears on WordCamp sites. You can build off of these stubs, or trash them and start fresh with your own content.

## Tickets and Attendees

Most WordCamps sell tickets and manage attendee information via the [CampTix](https://wordpress.org/plugins/camptix/) plugin. Check out our [CampTix documentation](https://make.wordpress.org/community/handbook/wordcamp-organizer-handbook/first-steps/web-presence/using-camptix-event-ticketing-plugin/) for detailed instructions on using each of its features.

## Third-Party Services

There are various shortcodes you can use to embed data from third-party services on your WordCamp.org site, such as Livestream.com, Google Forms, MailChimp, Campaign Monitor, and many more. Please refer to the [Shortcode Embeds](https://make.wordpress.org/community/handbook/wordcamp-organizer-handbook/first-steps/web-presence/setting-up-your-wordcamp-theme/shortcode-embeds/) page for more information, and if there’s a third-party service that you think we’re missing, let us know at support@wordcamp.org.

## Speakers

Start by adding a new speaker. Use the large title area for the full name of the speaker, and the content area for a short description or speaker bio. You’ll also see fields for “Gravatar Email”, and “WordPress.org Username”; make sure you fill them out with the speaker’s e-mail address and username. Also make sure your speakers are published (as opposed to set as drafts, pending, etc), otherwise they will be hidden from the front-end.

After you have filled out all the speakers, you can display a list on a post or page, using the \[speakers\] shortcode. It’ll output all the published speakers with their avatars. No styles will be applied, but the generic markup has easy-to-target classes, which you can use to style your speakers list.

Here’s a list of attributes, which can be used with the \[speakers\] shortcode:

show\_avatars

Show or hide avatars in the speakers list. Available values: “true” or “false”. Defaults to “true”.

avatar\_size

The size in pixels of the speakers avatars. Available values: Any positive integer. Defaults to 100.

speaker\_link

Where the speakers name should link to, if anything. Available values: “permalink” for the speaker’s individual post, or leave blank to not link anywhere. Defaults to not linking anywhere.

orderby

The field used to sort the speakers. Available values: “date”, “title”, “rand”. ≈Defaults to “date”.

order

The order in which the speakers are sorted. Available values: “desc”, “asc”. Defaults to “desc”.

track

Output speakers from a particular track only. Available values: A comma-separated list of track slugs.

groups

Output speakers from a particular group only. Available values: A comma-separated list of group slugs.

## Sessions

After you’ve added all your speaker’s bios, you can proceed to describing their sessions. Don’t forget to specify the speaker for each session that you create. If a session is run by more than one speaker, like a Q&A, you can assign several speakers to it, by separating them with a comma. If you’re running sessions in more than one track, like Users Track vs. Developers Track, make sure you assign the right track to every session. Tracks work the same way Categories do.

When you’re done adding sessions, you can use the \[sessions\] shortcode to display them to attendees. By default, it will output all sessions in the order you created them (ascending, by date). You can further configure the shortcode output using various attributes:

date

The date to pull sessions from, in [ISO-8601 format](http://xkcd.com/1179/) (YYYY-MM-DD). Defaults to showing all dates.

show\_meta

Show or hide session meta (speaker name, track) in the sessions list. Defaults to “false”.

show\_avatars

Show or hide the avatars of the speakers assigned to each session. Defaults to “false”.

avatar\_size

The size in pixels of the speakers avatars. Defaults to 100.

tracks

Output sessions from a particular track only. Available values: A comma-separated list of track slugs, or ‘all’. Defaults to ‘all’.

speaker\_link

Where the speaker’s name should link to. Available values: “*anchor*” (to link to their bio, if you’re using the \[speakers\] shortcode on the same page), “*wporg*” (to link to their WordPress.org profile), “*permalink*” (to link to their Speaker post), “none”. Defaults to ‘wporg’.

orderby

The field used to sort the sessions. Available values: “date”, “title”, “rand”, “session\_time”. Defaults to “date”. Note that “date” sorts by when the session post was published, while “session\_time” sorts by when the session will occur.

order

The order in which the sessions are sorted. Available values: “desc”, “asc”. Defaults to “desc”.

If you fill in the Slides URL field on each Session post, then a link will automatically be created in the \[sessions\] shortcode.

## Sponsors

When starting with sponsors, make sure you define your sponsor levels first, such as Gold, Silver and Bronze. By default, sponsor levels will be ordered by the level name, but you can set a manual order in Sponsors → Order Sponsor Levels by dragging levels up or down.

When adding a new sponsor, the title is used the sponsor’s name, and the content is used as the sponsor’s description/blurb (keep it short — people should be able to read these quickly!). Display sponsors using the \[sponsors\] shortcode.

You can further configure the shortcode output using these attributes:

link

Set the value to “website” to make the sponsor’s name and logo link to their website, or “post” to link to the sponsor’s post. Defaults to “none”.

title

Defaults to “visible”. Any other values, like “none”, will omit the title.

content

The default value “full” will print the content. The value “excerpt” will print the first 55 words of the content, adding a ‘continue reading’ (with hidden screen reader title) at the end. Any other value, like “none”, will hide the content, so only the logo and/or title will be shown.

excerpt\_length

Sets the number of words to be used in the excerpt (default is 55).

The sponsor’s **featured image** is used as their logo. It should have minimum dimensions of **600 x 220** pixels. For best results, use a **30:11** aspect ratio.

Examples:

\[sponsors\] – Shows sponsors with no links  
\[sponsors link=”website”\] – Shows sponsors and links to their website

## Schedule

After entering the sessions, you can use the \[schedule\] shortcode to display them in an easy-to-read table, sorted by the track and date/time.

You can also add breaks into the schedule by creating sessions and selecting the “Break, Lunch, etc” type from the Session Info metabox. Once you assign the break to all of the tracks that it will cover (in the Tracks metabox), it will automatically show up in the schedule.

date

The date to pull sessions from, in [ISO-8601 format](http://xkcd.com/1179/) (YYYY-MM-DD). Defaults to showing all dates.

tracks

Select which tracks will appear in the schedule. Available values: A comma-separated list of track slugs, or “all”. The track columns will appear in the same order that you enter them into this value. Defaults to “all”.

speaker\_link

Where the speaker’s name should link to. Available values: “anchor” (to link to their bio, if you’re using the \[\[speakers\]\] shortcode on the same page), “wporg” (to link to their WordPress.org profile), “permalink” to link to their individual Speaker post, “none”. Defaults to ‘anchor’.

session\_link

Where the sessions’s name should link to. Available values: “anchor” (to link to its description, if you’re using the \[\[sessions\]\] shortcode on the same page), “permalink” (to link to the session post), “none”. Defaults to ‘permalink’.

**Example for a Multi-day WordCamp:**

<h2>Friday, July 26th, 2013</h2>
\[schedule date="2013-07-26" tracks="users,designers,developers" speaker\_link="wporg" session\_link="anchor"\]

<h2>Saturday, July 27th, 2013</h2>
\[schedule date="2013-07-27" tracks="users,designers,developers" speaker\_link="wporg" session\_link="anchor"\]

## Organizers

If you’d like to help attendees get to know the organizing team, you can add a bio for each members in the Organizers menu, and then display that content using the \[organizers\] shortcode.

show\_avatars

Show or hide the avatars of the speakers assigned to each session. Defaults to “true”.

avatar\_size

The size in pixels of the speakers avatars. Defaults to 100.

orderby

The field used to sort the sessions. Available values: “date”, “title”, “rand”. Defaults to “date”.

teams

(optional) Determines which teams to show. Accepts a comma-separated list of team slugs. Defaults to showing all teams when left empty.

### Examples:

*   \[organizers show\_avatars=”false”\]
*   \[organizers avatar\_size=”200″ orderby=”rand”\]
*   \[organizers teams=”speaker-wrangers”\]
*   \[organizers teams=”speaker-wrangers,sponsor-wranglers”\]

## Translation

Some of the text on your site will be output by plugins and themes, and it might not have been translated into your language yet. If you find words that aren’t translated, you can help fix that!

1.  Open [the WordCamp project](https://translate.wordpress.org/projects/meta/wordcamp) at translate.wordpress.org
2.  Find your locale in the list
3.  Review [the Translator Handbook](https://make.wordpress.org/polyglots/handbook/tools/glotpress-translate-wordpress-org/) to learn how to translate strings

The translated strings should appear on your site automatically within 24 hours of being approved by an editor. If they don’t ping @*iandunn* or @*coreymckrill* in* the [#meta-wordcamp](https://make.wordpress.org/community/tag/meta-wordcamp/)* channel on [Slack](https://chat.wordpress.org).

## Miscellaneous

**Embed a menu** in a post or page with the \[menu\] shortcode

\[menu menu="Menu Name" menu\_class="extra-css-class" depth="1"\]

Tip: Here is [a quiz](https://community-self-training.mystagingwebsite.com/quiz/custom-tools-for-building-wordcamp-content-2/) on this article. Read [quizzes](https://make.wordpress.org/community/handbook/wordcamp-organizer/quizzes/) page if you have any questions about quizzes and how to navigate them.

*   [To-do](# "To-do")