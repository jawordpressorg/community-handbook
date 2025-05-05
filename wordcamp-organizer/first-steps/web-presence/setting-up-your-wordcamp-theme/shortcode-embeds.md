# Shortcode Embeds

In addition to the shortcodes that allow you to display WordCamp [speakers](https://make.wordpress.org/community/handbook/wordcamp-organizer-handbook/first-steps/web-presence/custom-tools-for-building-wordcamp-content/#speakers), [sessions](https://make.wordpress.org/community/handbook/wordcamp-organizer-handbook/first-steps/web-presence/custom-tools-for-building-wordcamp-content/#sessions), [sponsors](https://make.wordpress.org/community/handbook/wordcamp-organizer-handbook/first-steps/web-presence/custom-tools-for-building-wordcamp-content/#sponsors), [organizers](https://make.wordpress.org/community/handbook/wordcamp-organizer-handbook/first-steps/web-presence/custom-tools-for-building-wordcamp-content/#organizers), and [tickets](https://make.wordpress.org/community/handbook/wordcamp-organizer-handbook/first-steps/web-presence/using-camptix-event-ticketing-plugin/#creating-tickets) — we even have a way to [automatically create a grid schedule](https://make.wordpress.org/community/handbook/wordcamp-organizer-handbook/first-steps/web-presence/custom-tools-for-building-wordcamp-content/#schedule) now, hurray! — WordCamp.org supports several shortcode embeds, which allows you to quickly embed content such as Google Maps, Slideshare presentations and other material on your posts and pages. This page describes each available shortcode.

## Livestream.com

If you’re live streaming your event with Livestream.com, WordCamp.org allows you to embed the live stream player in your post or page using the `[livestream]` shortcode. The shortcode accepts the following attributes:

*   **width** – specifies the width of the player in pixels
*   **height** – specifies the height of the player in pixels
*   **url** – specifies the livestream URL for the player

Please note that the **url** must contain a URL from the **new.livestream.com** or ****cdn.livestream.com**** domain.

## Ustream.tv

You can also stream your event via Ustream.tv with the shortcode. For example:

```
[ustream id=36117299 width=480 height=302]
```

*   **id** – specifies the id of the stream
*   **live** – set to 1 if streaming live; or omit it for a recorded video
*   **width** – specifies the width of the player in pixels
*   **height** – specifies the height of the player in pixels

## DaCast.com

You can also stream your event via DaCast.com with the \[dacast\] shortcode. For example:

```
[dacast broadcaster_id="012345" channel_id="67890" width="640" height="360"]
```

*   **broadcaster\_id** – the ID of the account
*   **channel\_id** – the ID of the channel
*   **width** – specifies the width of the player in pixels
*   **height** – specifies the height of the player in pixels

## StreamText.net

You can also add captions to your live streams with StreamText.net and the \[streamtext\] shortcode.

```
[streamtext event="IHaveADream"]
```

The following additional parameters are optional:

*   **ff** – the font family
*   **fs** – the font size
*   **spacing** – the line spacing
*   **fgc** – the foreground (text) color
*   **bgc** – the background color
*   **header** – display the header
*   **footer** – display the footer
*   **controls** – display the UI controls so the user can set the colors, fonts, etc. *header* must be *true* for this to work.
*   **chat** – display the chat box

## Eventbrite

If your WordCamp is running ticketing through the third-party service Eventbrite, you can embed the ticketing form using the `[eventbrite]` shortcode with the following attributes:

*   **width** – specifies the width of the player in pixels or %
*   **height** – specifies the height of the player in pixels
*   **id** – specifies the ID of your event. This is the “eid” argument of your embed URL

## Google Forms

To embed a Google Form in your post or page, you can use the `[googleapps]` shortcode, though it’s easier to simply copy and paste the embed code given when sharing a Google Form, into your post or page, which will automatically be converted into the proper shortcode with attributes. For example:

```
[googleapps domain="docs" dir="spreadsheet/embeddedform" query="formkey=dDdDZ2ZnVWFtRjNlZGp6cnl6a0d0S2c6MQ" width="760" height="639"]
```

You can then control the width and height of your embedded form by changing the shortcode attributes.

## Gravatar

You can use the Gravatar shortcode to easily embed a gravatar in any post. The two available attributes are the e-mail address and the size of the avatar in pixels.

```
[gravatar email='email@address.com' size='50']
```

## MailChimp

You can include a MailChimp subscription form using the MailChimp shortcode. You’ll need your list URL as the only shortcode attribute, which you can obtain from your MailChimp account. Edit your list and select For Your Website → Signup Form Link Code from the list navigation menu. You’ll be given a short link to your form:

[![MailChimp](https://plan.wordcamp.org/files/2012/10/Screen-Shot-2013-01-08-at-3.45.34-PM.png)](https://plan.wordcamp.org/files/2012/10/Screen-Shot-2013-01-08-at-3.45.34-PM.png)

Visit that URL, which will redirect you to the full URL of your subscription form, which contains “list-manage.com”. That full URL is the one you’ll need to use with the MailChimp shortcode:

[![Screen Shot 2013-01-08 at 3.48.20 PM](https://plan.wordcamp.org/files/2012/10/Screen-Shot-2013-01-08-at-3.48.20-PM.png)](https://plan.wordcamp.org/files/2012/10/Screen-Shot-2013-01-08-at-3.48.20-PM.png)

Enter that URL as an attribute with the MailChimp shortcode, like this:

```
[mailchimp url="http://example.us6.list-manage2.com/subscribe?u=3fbb5a8dfe2d6ff73c390a87e&id=a00d08b369"]
```

This will result in a MailChimp subscription form, which you can further customize with CSS. Please note, that if you’d like to use the name field with your list, the Field Tag in your field settings on MailChimp should say “NAME” (all caps).

## Campaign Monitor

The Campaign Monitor shortcode allows you to embed a newsletter subscription form, powered by CM. The shortcode has one required attribute, which is the form URL. You can get this form URL when “creating a subscribe form” for your list: when you generate the code for your subscription form, the form element’s action attribute will be set to this URL.

[![Campaign Monitor Shortcode](https://plan.wordcamp.org/files/2012/10/Screen-Shot-2012-11-27-at-4.43.06-PM.png)](https://plan.wordcamp.org/files/2012/10/Screen-Shot-2012-11-27-at-4.43.06-PM.png)

```
[campaign-monitor url="http://username.createsend.com/t/t/s/sjlk/"]
```

Embed reversal will also work. If you copy the generated form HTML from Campaign Monitor, paste it in your HTML editor on WordCamp.org and hit Save, it should be automatically converted into a shortcode with the correct attributes.

## WordPress.tv & VideoPress

Once the WordCamp videos have been published on WordPress.tv, you can embed the video back on your WordCamp site.

The shortcode is:

```
[wpvideo abcdefgh]
```

For full instructions on how to add a video to your WordCamp site, please refer to the page [Adding videos to your WordCamp site](https://make.wordpress.org/community/handbook/wordcamp-organizer/video/adding-videos-to-your-wordcamp-site/).

## Other Embeds

The default [WordPress Embeds](https://codex.wordpress.org/Embeds#Okay.2C_So_What_Sites_Can_I_Embed_From.3F) are also supported, such as YouTube, Vimeo, Twitter, Flickr and more. In addition to that, [Jetpack Embeds](http://jetpack.me/support/shortcode-embeds/) are also active for services like Polldaddy, Google Maps, Slideshare and more.

If there’s a third-party service you’d like to use with your WordCamp site, and think other organizers can benefit from it, feel free to [get in touch](http://central.wordcamp.org/contact-us/), we’re always open to suggestions.

*   [To-do](# "To-do")