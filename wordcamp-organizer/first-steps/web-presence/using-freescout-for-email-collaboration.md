# Using FreeScout for email collaboration

## Overview

  
Shared inbox software provides a collaborative space for WordCamp teams to answer emails jointly. Shared inboxes can also aggregate multiple email accounts into one inbox for streamlined management. Below are some of the benefits of using a shared inbox for your WordCamp;

*   Multiple inbox support for flagship WordCamps (flagship@wordcamp, flagship-sponsors@wordcamp, flagship-venue@wordcamp etc)
*   Assign user permissions
*   Tags / labels
*   Workflows (auto-assign, auto-reply etc based on conditions)
*   Read receipt
*   Saved replies (saves sponsor replies, welcome emails, attendee FAQ)

## FreeScout

FreeScout is the super lightweight free open source help desk and shared inbox written in PHP7 (Laravel 5.5 framework). It is self-hosted and very similar to HelpScout or other shared mailbox services.

*   Some of the additional features require paid modules ranging from $2 – $20 one-off payment.

![](https://lh4.googleusercontent.com/nyNyK5uEWSryeTGg3sjn321KmxDpwIPksS32cuJxEByIwkuueiCN1-NhrzsJhwfvAEMLRwJUxm-5-4fu2ZG_7zc2BAwwfcwk81iJiZNfsVH2ceicfi6Omoc1QltMe99D2QSz2EZk=s1600)

![](https://lh4.googleusercontent.com/sr5xVUklp1k_YeEK6oMAYPP7vwC10HFVDLjAwWUVW9acOsUNjs5-RrzEqv10I1W30_w3qaT0cfsUk4kr8IfgZx7RybCla4zaJ7TwUJo5KPv5-GKFHfCIPSjMgBFpzNxKaitZXyja=s1600)

## Requirements

FreeScout is a pure PHP/MySQL application just like WordPress, so it can be easily deployed even on shared hosting.

### Installing in a Shared Hosting server

Many shared hosting comes with the Softaculous script installer pre-installed. From your control panel, navigate to Softaculous and search “FreeScout”.

![](https://lh6.googleusercontent.com/371mCjw9Fh2pfkTa88nswQsu5gc8bV7bDhYfAqApRM0pl2VYyrq0n3HC7HJp6fTaz0UwAHeZsO9jLVYxk4FQp4btoCZuYE0j3MGZjlCTr-njom7q8EpqC0q2cuJv68bKl6sA9o4J=s1600)

### Installing in a Cloud hosting provider

Please follow official installation instructions from Freescout here;  
https://github.com/freescout-helpdesk/freescout/wiki/Installation-Guide

## Setting up WordCamp email with FreeScout

As a WordCamp organizer, you should have received a WordCamp Gmail address such as city@wordcamp.org.

In order to set up your WordCamp Gmail with Freescout, please follow the following steps;

**Step 1: Setup a Two Factor Authentication**  
Visit https://myaccount.google.com/security and click 2-Step Verification and set up your phone number to secure the account.

**Step 2: Create an App password**  
Visit https://myaccount.google.com/apppasswords and create a new App Password for FreeScout. Copy the password that you created in this step to be used in your FreeScout setup.

![](https://lh6.googleusercontent.com/XLcPQmqMrsyofsOFg9u2uI9MVkOf_eqsXphShCmj-VucKjX-ZxnGWGlmb1iJFJEW1QAz0ut8-LHic1vvdn2kdM9tO5IStjJhY3uSEZP9FHpxr01_Es89t2pGRLFkNBy0uQaKBqt_=s1600)

**Step 3: Setup new Mailbox in FreeScout**  
Go to Manage > Mailboxes > New to add a new Inbox in your FreeScout instance. Enter the basic details as required.

![](https://lh6.googleusercontent.com/EE4D7KczApFAqG9TLQ7mxesXuBHtLzdZVRAm3YBum4SqaoJUD7yBxcyPsnDa8-itFffMoBNk-B5UotCeotSGqOySqg7QrkTWX4_zW_KJD7LwUOcJjrD5Ohb5pOzeclX3RcFx8lij=s1600)

**Step 4: Setup Outgoing Mails**  
In the next screen, set up the outgoing mails or SMTP. Use the settings below to set up your WordCamp email. Replace the username with your WordCamp email and the Password is the app password you created in Step 2 (Take note that this is not your WordCamp Gmail password).

![](https://lh5.googleusercontent.com/Gxvw4Vak7tFi_nI1YgwYjtyh6bQDNRUHbB-kPs-U-c9iPu4E2dZjirvjnUBuffqjZzgoAitgWGGo9ZrEosT0fJeWW6rDkMahnTz7yz7C-qeNqDQ0aIHdgXC63nUIQ61nJz6oEQcl=s1600)

**Step 5: Setup Incoming Mails**  
Finally, set up the incoming email. Click on the Fetching emails tab and set it up as the following example. Replace the username with your WordCamp email and the Password is the app password you created in Step 2 (Take note that this is not your WordCamp Gmail password).

![](https://lh6.googleusercontent.com/_0c-LLh_4UA_iW4YG3IY4SXMLT0_41rBzEdFW8yeyq9hWXriZNdVESvGQ1jQ8VdsELsa1Gac2hxQnRDieFtKv2BElnxLED7jOb3wRab5r5zbe7P6wyVFC-qI21Au9YafFmSVq0a4=s1600)

Important Note: Make sure you save all settings before clicking “Check connection” or “Send test mail”.

Repeat Step 1 to Step 5 to add other inboxes if you have more than one email ID for your WordCamp such as sponsors@ or venue@.

## Managing Users

Now that you have configured FreeScout inboxes, the next step is to add fellow organizers to access and collaborate in conversations.

![](https://lh6.googleusercontent.com/Uf3GWuyuJfQ9EtsrH7lSzrpS9c7RZxjonOP1GzxIn_ZKO1mIA7pvsIQkgwcNmNxpS37VvdIx6v-Z6iq_JRkk6qPifLewYD5R0VyoBJFpYctTz0ZZS3KhuQTHpCsEMIO-S3KEz5Fc=s1600)

### Adding a new Organizer / Co-Organizer / Wrangler

To add new users to your FreeScout, go to Manage > Users > New. Fill up the form and the user will receive an invitation email.

### Useful Modules

Below are some of the useful modules (which are not free);

TAGS – Allow tag issues such as “Sponsors”, “Attendee”  
https://freescout.net/module/tags/

WORKFLOW – Allow set automation. Such as auto-forward email, Add tags when containing specific subject, etc.  
https://freescout.net/module/workflows/

*   [To-do](# "To-do")