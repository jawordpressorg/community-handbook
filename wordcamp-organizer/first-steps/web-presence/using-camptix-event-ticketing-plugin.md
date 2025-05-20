# Using CampTix Event Ticketing Plugin

CampTix is an easy-to-use, free and open source event ticketing plugin for WordPress. The plugin is now integrated into the WordCamp Central network.

This article includes info on [payment gateways](#payment-gateways) for different currencies, [creating tickets](#creating-tickets), giving [refunds](#refunds), [managing](#attendees) and [displaying attendees](#attendees-list), [tracking attendance](#tracking-attendance), [failed purchase attempts](#failed-purchases), and other CampTix [tools](#tools).

## Tickets and Coupons

### Selecting a Payment Gateway

There are multiple payment gateways (e.g., Stripe, PayPal, PagSeguro, etc) that CampTix can use to collect payment from attendees. The main differences between them are the currencies they accept, and their popularity in different regions of the world.

**If you want to use Stripe or PayPal** **and your event is running its money through WPCS**, then your gateway is already enabled by default, and you can start [creating tickets](https://make.wordpress.org/community/handbook/wordcamp-organizer/first-steps/web-presence/using-camptix-event-ticketing-plugin/#creating-tickets) whenever you’re ready.

**If you want to use PayPal but your event is handling the money locally** (outside the US/Canada), then go to CampTix > Setup > Payment tab, and select “None” in the Predefined Account field, and click on the “Save Changes” button. Fields for entering your PayPal API details will then appear. Enter the details of the PayPal account you plan to use to collect ticket revenue, then click “Save Changes” again.

**If PayPal doesn’t support your currency, or attendees in your city prefer another gateway**, then it’s very important that you select a gateway early on in the organizing process. We’ll need to coordinate the setup with you, and if we don’t already have a plugin to support that gateway, we’ll ask your community to create one.

That process might only take a few days, but if a new plugin needs to be created, then it could take a few weeks, or even a few months. If you don’t get started on that process early, then you might not be able to open ticket sales when you plan to. To get started, contact your mentor or a deputy. Make sure the gateway you want to use is approved before you start writing code.

The gateways/currencies we currently support are:

*   **KDCpay**: INR
*   **Instamojo** – INR
*   **MercadoPago**: ARS, BRL, MXN, VEF, COP
*   **PayFast**: ZAR
*   **PayPal**: AUD, CAD, EUR, GBP, JPY, USD, NZD, CHF, HKD, SGD, SEK, DKK, PLN, NOK, HUF, CZK, ILS, MXN, BRL, MYR, PHP, TWD, THB, TRY
*   **PagSeguro** – BRL
*   **PayStack** – NGN
*   **RazorPay** – INR
*   **Stripe** – AED, AFN, ALL, AMD, ANG, AOA, ARS, AUD, AWG, AZN, BAM, BBD, BDT, BGN, BMD, BND, BOB, BRL, BSD, BWP, BZD, CAD, CDF, CHF, CNY, COP, CRC, CVE, CZK, DKK, DOP, DZD, EGP, ETB, EUR, FJD, FKP, GBP, GEL, GIP, GMD, GTQ, GYD, HKD, HNL, HRK, HTG, HUF, IDR, ILS, INR, ISK, JMD, KES, KGS, KHR, KYD, KZT, LAK, LBP, LKR, LRD, LSL, MAD, MDL, MKD, MMK, MNT, MOP, MRO, MUR, MVR, MWK, MXN, MYR, MZN, NAD, NGN, NIO, NOK, NPR, NZD, PAB, PEN, PGK, PHP, PKR, PLN, QAR, RON, RSD, RUB, SAR, SBD, SCR, SEK, SGD, SHP, SLL, SOS, SRD, STD, SZL, THB, TJS, TOP, TRY, TTD, TWD, TZS, UAH, USD, UYU, UZS, WST, XCD, YER, ZAR, ZMW, BIF, CLP, DJF, GNF, JPY, KMF, KRW, MGA, PYG, RWF, UGX, VND, VUV, XAF, XOF, XPF
*   **TrustPay / TrustCard** – BGN, CZK, EUR, GBP, HRK, HUF, NOK, RON, TRY, USD

### Creating Tickets

After your payment methods have been set up, browse to **Tickets** and create a new ticket, just like you would create a new post or page. Tickets have a few different options and fields, here’s a quick overview:

*   **Ticket Title** – as the name suggests, this is the ticket title which will be displayed on the ticketing page, an will appear in your PayPal reports and receipts
*   **Ticket Excerpt** – this is a description of what the ticket includes, like lunch, a T-shirt, parking and so on. The excerpt will appear below the ticket title on the ticketing page.
*   **Price** – the price of one ticket in the selected currency. You can change the currency **Tickets > Setup**
*   **Quantity** – the maximum number of tickets to sell. As soon as this amount of tickets is sold, the ticket is no longer visible on the ticketing page.
*   **Availability** – optional fields to restrict the availability of the ticket purchase to certain dates. You can use these fields to create early-bird tickets at a cheaper price. To avoid selling tickets during or after your event, it’s a good idea to set the tickets end date to the date of your event.
*   **Questions** – you can use this section to build the form users have to fill in, before they can purchase their tickets. Make sure you use the built-in question types when appropriate, to enable additional features. For example, the **T-shirt Size** question type will enable sponsors to [view aggregate size counts](https://central.wordcamp.org/t-shirt-sizes/), so they can send the right number of each size to your camp.
*   **Microsponsor ticket** – Any sponsorship under $250 USD or equivalent is called a microsponsorship. To reduce administrative burden, organizers can create a microsponsor ticket instead of a sponsor invoice. You can create a microsponsor ticket the same way you create a regular ticket. The organizer team can also decide if they want to acknowledge microsponsors on the Sponsors page or on a separate page on the WordCamp site.

You can save your ticket at any time, and as soon as you’re comfortable with the ticket settings, hit **Publish**.

If you’d like to test ticket purchases while in sandbox mode, just [sign up for a PayPal sandbox account](https://developer.paypal.com/api/rest/sandbox/accounts/), and then go through the normal checkout process. When you get to PayPal, use that username/password for the sandbox account instead of a real account, and PayPal will create a simulated transaction, rather than charging a real credit card.

### Opening Registration

The first step to opening registration is to **take CampTix out of sandbox mode**. To do that you’ll need to visit the **Tickets > Setup > Payment** screen. If you’re using PayPal, then select *WordPress Community Support PBC* from the **Predefined Account** list. If you’re using another payment gateway, then select *No* for the **Sandbox Mode** option.

The second step is to **publish the Tickets page** that was automatically created when your site was setup. It contains the \[camptix\] shortcode, which generates the registration form that attendees will fill out in order to purchase a ticket.

Make sure you only have one page with the \[camptix\] shortcode, and use that page for pretty much everything:

*   List tickets available for purchase
*   Show the attendee and checkout form
*   Show a receipt after returning from PayPal
*   Show an edit attendee information form

The text before and after the shortcode will be shown in all the above cases, so don’t write things like “use the form below…” since there might be no form at all, if there are no more tickets available for sale.

Please include a refund policy on your registration page, saying that refunds are only available within 60 days of any ticket purpose, or declaring that refunds will not be available if you decide not to give refunds.

Please also include a copy of your Recording Policy on the registration page. Here’s an example:

> For community-building and promotional purposes, there will be volunteer and/or professional photographers and videographers at the WordCamp event. By attending the event, you consent to your image being used in resulting photos or videos that may show your participation in the WordCamp.

### Reservations

Reservations allows you to create a block of reserved tickets that will not appear on the public registration page, but can be accessed through a secret URL. Go to Tickets > Setup > Beta (tab) and **Enable Reservations**. Once reservations are enabled, you can create reserved ticket blocks at the very bottom of the Ticket Edit screen. The name of the reserved block of tickets will appear in the secret ticket URL, and reserved tickets are not automatically free — so if you want to provide free, reserved tickets for sponsors or speakers, you’ll need to share the secret reserved ticket URL as well as a coupon code with those folks. If you click **Release** next to a reserved ticket block in the Ticket Edit screen, those released tickets will return to the public pool of tickets. If you click **Cancel**, the reserved tickets will be removed entirely, rather than released into the public pool.

### Creating and Using Coupons

Coupons are discount codes you can give to your attendees. To create a new coupon code, browse to **Tickets > Coupons** and create a New Coupon. The fields are quite self-explanatory:

*   **Title** – the coupon code. This is the code people will type in to get their discount. It’s **not** case sensitive, so Coupon will work the same as COUPON or cOuPOn.
*   **Discount** – can either be a fixed amount or a percentage, which will be deducted from the ticket price. If a ticket price is $10 and the discount is set to $3 or 30%, people will be able to purchase the ticket for $7.
*   **Quantity** – the maximum number of times this coupon can be used. Note, that if the coupon quantity is more than one, an event attendee can purchase as much tickets as the coupon quantity will allow them to. This means they are not restricted to a single coupon usage per purchaser. If you’d like a coupon to be used only once, create a coupon and set the quantity to one.
*   **Applies to** – check the tickets that should be discounted when this coupon code is used. Note that when you create a new ticket, it **will not** automatically be discounted by the saved coupons. You will have to add them explicitly.
*   **Availability** – similar to tickets availability, defines the date period when the coupon can be used.

You can save the coupon as a draft at any point, but it has to be **Published** in order to work.

Also, if no coupons are available (because they’re not published, the quantity is 0, or the availability date has passed) then the field that attendees use to enter a coupon code on the registration form will not be shown.

#### Auto-filling coupon codes 

Coupon codes can be auto-filled in the ticket form by using a special link in the format: `city.wordcamp.org/tickets/?tix_coupon=CODE#tix`. Replace “city.wordcamp.org/tickets/” with the URL of your tickets page and “CODE” with your coupon code (not case sensitive). Doing this makes it easier for attendees to use codes and removes any chance of typos!

### Refunds

The Refunds feature allows an attendee to cancel the ticket they purchased and get a full refund. Once a ticket is refunded, it goes back into the pool of available tickets for someone else to buy.

They can access the refund form by clicking on the link in the confirmation e-mail they were sent when they purchased the ticket. If you need to send them the link manually, or want to submit the refund form on their behalf, you can edit their Attendee record and then look for the “Access token” link inside the Attendee Information metabox. Opening that link will take you to the page where you can access the refund form.

If refunds are turned on, but you don’t see the link to the refund form, it may be because the user purchased their ticket with a 100% coupon code, in which case there’s nothing to refund. If you’d like to return their ticket to the pool of available tickets, you can delete their Attendee post.

Refunds are turned off by default, but you can enable them by going to the **Tickets > Setup** screen. If you’d like, you can choose a cut-off date, after which refunds will no longer be available. That can be useful if you want to have a final head-count a few days before the event starts, or avoid fluctuations in the budget close to the event.

On average, we’ve noticed that about 1-2% of tickets will be refunded, but your mileage may vary.

## Attendees

Under **Tickets > Attendees** you will find a list of people who have signed up (or who have tried to sign up) for your event. You can use the search box to find attendees by name, e-mail, transaction ID, etc. Attendees can have several different statuses:

*   **Published** – the form was filled out and payment was completed successfully.
*   **Draft** – an attendee has filled the purchase form and sent to a payment gateway, but has not completed the payment yet. Draft attendees will be set to **Timeout** if they never return from the chosen payment gateway, or **Published** if they complete the process.
*   **Pending** – the payment was made, but was not completed yet, usually caused by echeck payments, or other payments that need to be reviewed. Pending payments will be processed as soon as their status is changed at the payment gateway if IPN is configured. Pending payments count towards the ticket totals, and are exported together with Published payments. If IPN has not been set up, you will have to process pending payments manually.
*   **Cancelled** – used when the buyer cancels their payment at the payment gateway.
*   **Timeout** – when a purchase has been initiated but never completed, a **Draft** ticket will turn into this state.
*   **Failed** – used when the payment gateway fails to collect payment, usually because the credit card was declined due to the wrong name/address being entered, insufficient funds, etc. See [Failed Purchase Attempts](https://make.wordpress.org/community/handbook/wordcamp-organizer/first-steps/web-presence/using-camptix-event-ticketing-plugin/#failed-purchases) for more details.
*   **Refunded** – when a ticket is refunded, initiated by the buyer or the seller. You’ll need a properly configured IPN to make this work.

You can further click on any of the attendees is the list to learn more about them. **Note** that changing statuses, creating or deleting attendees manually, may cause errors in your Revenue reports, so try to avoid that as much as possible.

If you want to **track attendance**, you can check the ‘Attended the event’ checkbox on each Attendee post, then use the **Summarize** and **Export** tools to see how many people attended, or get a list of everyone who attended.

### Failed Ticket Purchases

**It’s normal** to see a small percentage of attendees listed as Failed in CamptTix. This happens when the payment gateway rejects their payment method (e.g., PayPal rejected their credit card). That usually happens because **the attendee entered their payment details incorrectly, or because the credit card has reached it’s limit**. It’s also possible that their bank has detected suspicious activity on the card, and temporarily frozen it.

Sometimes company credit cards also have additional fraud restrictions in place, like only allowing purchases from certain merchant codes. Our Stripe merchant code is `8299 (Educational Services)`.

If an attendee contacts you because they’re having trouble registering, the first step is to ask them to **double-check that they are entering everything correctly**. It’s important to check more than just the card number, because sometimes banks will reject transactions if the address, phone number, etc don’t match their records exactly. If they have changed their address or phone number, but haven’t updated their bank, that could be the problem.

If that doesn’t work, then the next step is to **try using a different payment method**, like a debit card, a PayPal account balance, etc.

If that still doesn’t work, then the best thing to do is ask the attendee to **contact their bank** to find out exactly why the transaction was declined. To protect their privacy, the bank doesn’t provide us the exact reason why they rejected the payment, so the bank is the only entity that can help them.

If you run into any problems, you can also ask a developer for help in the [#meta-wordcamp](https://make.wordpress.org/community/tag/meta-wordcamp/) channel on Slack.

### Attendees List

You can create a list of attendees on any page by using the `[camptix_attendees]` shortcode. This will create a list of avatars, names, URLs and Twitter handles if provided by the attendees. You can style the list with CSS, each item is fairly easy to target with selectors. You can change the number of columns [using CSS](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Columns/Using_multi-column_layouts), or with the `columns` attribute, like this:

```
[camptix_attendees columns="2"]
```

As of version 1.2, the default number of columns is three.

You can pass a comma-separated list of ticket IDs to the *tickets* parameter if you want to restrict the list to only attendees who’ve purchased certain tickets.

```
[camptix_attendees tickets="1143,1144"]
```

You can pass a pipe-separated list of Question titles to the *questions* parameter if you want to show attendees’ answers to custom questions asked on the registration form. Before publicly showing a question, make sure that it isn’t something attendees would consider private.

```
[camptix_attendees questions="What's your interest in WordPress?|Are you coming in from out of town?"]
```

## Tracking Attendance

You can also use CampTix at the registration table during the event, to check-in attendees in real-time. There is a special page on the site that registration volunteers can access with a mobile device or laptop, and check each person in as they show up.

To enable the special page, visit **Tickets > Setup > Attendance UI**, then click *Yes* to enable the UI, and *Generate a new secret link*, then *Save Changes.* 

Then, copy/paste the secret link into an e-mail to your registration volunteers, and ask them to visit it and test it out, so that they understand how it works. They’ll need to keep the e-mail handy so they can pull up the page during registration.

It’s a good idea to remind them to bring a laptop or mobile device on the day of the event, along with a charger. You’ll need to provide electricity and power strips at the registration table.

For convenience, the page does not require volunteers to log in to the website, only that they have the secret link, so to avoid any malicious changes by random Internet trolls, you should wait until a day or two before the event to enable the page, and then disable it when registration closes.

## Admin Flags

Admin Flags are a feature that allows you to define a list of special flags that can be toggled for every attendee through the admin UI. Flags are not visible to attendees but can be seen and filtered in exports.

To create an Admin Flag, go to *Tickets → Setup* and click the *Admin Flags* tab.

In addition to filtering exports, you can also use Admin Flags to filter the list of attendees output by the `[camptix_attendees]` shortcode, using the `has_admin_flag` attribute. For example, if you have a flag with the slug `volunteer`, you can show a list of just the attendees who are volunteering with:

```
[camptix_attendees has_admin_flag="volunteer"]
```

You can specify multiple flags, separated by commas, but keep in mind that it will only display attendees who have **all** of the specified flags enabled.

## Summaries, Revenue, and more

If you browse to **Tickets > Tools** you’ll see a bunch of cool stuff that will help you with your ticketing workflow. Here’s a brief description of each section:

*   **Summarize** – allows you to create a quick summary of all purchased tickets by their various fields, including ticket type, purchase date, coupon code, and all the various questions you have added to your tickets. This section will help you determine what T-shirt sizes to order, or the number of attendees who require a parking space. You can also export the chosen summary to CSV.
*   **Revenue** – will give you a quick snapshot of the financials and the total number of tickets sold and remaining. You can compare this data with your PayPal reports to make sure everything is going smooth.
*   **Export** – allows you to export all your attendee data in various formats. This is useful when you need to work with a badge-printing company (you can just send them the CSV), or print a registration list, or just backup your CampTix data.
*   **Notify** – allows you to send e-mails to attendees, including the ability to target messages to only certain subsets of attendees. It’s useful to send out reminders, or offers, before or after your event. You can even use shortcodes in your messages to make them more personalized. Hit the **Preview** button to see what a message will look like. At the bottom of the page you’ll also find a History of sent messages.

Here is [a quiz](https://wordpress.org/contributor-training/quiz/using-camptix-event-ticketing-plugin-2/) on this article. Read [quizzes](https://make.wordpress.org/community/handbook/wordcamp-organizer/quizzes/) page if you have any questions about quizzes and how to navigate them.

<!--
*   [To-do](# "To-do")
-->
