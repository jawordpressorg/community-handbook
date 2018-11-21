# Personalized Badges with HTML/CSS

To create personalized badges with HTML and CSS, browse to **Tickets > Tools > Generate Badges**, or open the Customizer and click on *CampTix HTML Badges*. Once you launch the tool, the badges are automatically generated for you, based on the Attendee posts in CampTix.

Below you’ll find an example of what the tool looks like. In the left pane, you can **customize** the badges, and in the right pane, you can **preview** them. Each badge has a **front** side and a **back** side, which are identical. The back side is shown upside-down, so that it will be printed right-side-up. The front has a mark for punching holes, so that the badges can be hung on lanyards.

![create-badges-with-html-css](https://make.wordpress.org/community/files/2016/04/create-badges-with-html-css.png)

## Avatars

The images on each badge are pulled from the attendee’s [Gravatar](https://gravatar.com) account. If the attendee doesn’t have a Gravatar, a default image will be shown. You can use the *Notify* tool (Tickets > Tools > Notify) to encourage attendees to create a Gravatar. Make sure to tell them that they need register with Gravatar using the same e-mail address that they purchased a ticket with.

## Customizing the Design

You can customize how the badges look by editing the CSS shown in the left-hand pane, and you’ll get a live preview every time you make a change.

The underlying markup has **plenty of CSS classes to help with customization**.

Here are a few examples of changes you can make with CSS:

*   Create different badges for speakers, sponsors, etc by targeting `attendee.ticket-{ticket_slug}` and/or `attendee.coupon-{coupon_slug}` ; for example, give volunteer badges a different background color, so that they’re easy for attendees to find.
*   Tweak badges for specific individuals, by targeting `.attendee-{name}`; for example, give long names a smaller font size so that they fit on the badge.
*   Give all last names a smaller font size than the first name.

There are also plenty of empty `<div>` elements that you can re-purpose for arbitrary design features.

The width and height dimensions of each badge are based on 8.5 x 11 pages.

After making your changed, you can hit the **Save** button to save them. If you want to throw away your changes and switch back to the default design, you can use the **Reset to Default** button.

## Printing

Once you’re ready, just click on the **Print** button and **save them as a PDF**,  then send that file to a local print shop for printing and cutting. You can [check out a sample PDF](https://make.wordpress.org/community/files/2016/04/sample-html-css-badges.pdf) to get a better idea of what it will look like.

## Tips

*   Print a sample PDF after you finish customizing the design, and check with your printer to make sure they can print and cut the badges. That way you won’t run into any surprises when it’s time to do the full order.
*   In Firefox’s print options, you can turn on background colors and background images, and also remove header/footer lines.
*   If you accidentally reset to the default CSS, you can restore your previous CSS by clicking on the CSS textarea and then using the `control-z` keyboard shortcut.

*   [To-do](# "To-do")