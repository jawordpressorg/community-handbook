# Notify &#8211; Connecting with Your WordCamp Attendees

Notify is a tool built into all WordCamp sites via the Camptix plugin, which allows you to notify your WordCamp Attendees (i.e people who have purchased tickets) via email. This is useful for sending them specific information that is relevant to their attending the WordCamp and getting the best experience from WordCamp.  

You can access the Notify feature in your WordCamp site from **Tickets** -> **Attendees** and then clicking the **Notify** tab.

![](https://make.wordpress.org/community/files/2018/07/001.png)

## Filtering the attendee list for Notify emails.

In order to send a Notify email, you will need to determine who will receive this email (building up the **To:** list). This is possible by creating conditions which the attendees must match, in order to include them in the list. For example, you might want to send an email to all attendees who have purchased a specific ticket type, or all attendees who have purchased a ticket after a certain date.  

You can select whether or not the attendees must match all of the conditions you’ve created or any of the conditions you’ve created. This is selected from the first field in the filter conditions section by selecting either any or all in the the ‘Attendees matching’ dropdown.

![](https://make.wordpress.org/community/files/2018/07/002.png)

You can then define your conditions. Conditions are created using the three dropdowns which follow this format – *Field* (first dropdown), *Comparison* (second dropdown) *Value* (third dropdown).

![](https://make.wordpress.org/community/files/2018/07/003.png)

Depending on the status and activity on your WordCamp site the options in these three dropdowns may vary.  

On a brand new WordCamp site the *Field* dropdown only contains Purchased Ticket, Purchase Date and Coupon code used, whereas a site close to the actual WordCamp date includes fields from the ticket purchase form like Dietary Requirements and WordPress skill level.  

The *Value* dropdown will either correspond with the *Field* selected (for example selecting Purchased Ticket changes the *Value* field to the available ticket types) or a simple text box, in which you can type the value you’re searching for. Depending on which type of *Field* you select, will determine which options are available in *Value* for that condition.  

The *Comparison* dropdown options change depending on the *Field* selected and the possible *Values* for that field. If the *Values* are specific it shows **is/is not**, being a specific *Field/Value* match. If the *Field* is a date field, it allows for **before** or **after** that date, and if the *Value* option is a text field it contains **is, is not, contains, does not contain, starts with and does not start with**.  

**Is** and **is not** mean the search will performed will be an exact match (or not), **contains** and **does not contain** will do partial string matches and **starts with** and **does not start with** will perform partial matches but on the beginning of the *Field* data being searched.  

## A note on date fields

If the *Field* you have selected is a date field (ie Purchase Date) then the *Value* option changes to a text box. In this text box you can enter any valid English string date. For example, 6/28/2018, 28-06-2018 and 18-06-28 are all valid string dates.  

To avoid potential ambiguity, it’s best to use the (YYYY-MM-DD) date format (2018-06-28)  

Finally you can also add multiple conditions by which to filter your list.

![](https://make.wordpress.org/community/files/2018/07/004.png)

## Message content

Once you’ve defined your conditions, you can enter an email **Subject** and a **Message** to be sent to the list. The **Message** field supports a predefined list of shortcodes (**\[first\_name\], \[last\_name\], \[email\], \[ticket\_url\]**) you can add to the email, which will be replaced with the actual attendee data. This is a nice way to personalize the notification email. You can also make use of a predefined set of HTML tags, which are listed below the message area.

![](https://make.wordpress.org/community/files/2018/07/005.png)

## Preview and send

You can use the **Preview** button to preview what the email will look like before sending. The preview will display under the **Message** text area.

![](https://make.wordpress.org/community/files/2018/07/006.png)

Finally the **Send Emails** button will send the mail to the selected recipients.  

<!--
*   [To-do](# "To-do")
-->
