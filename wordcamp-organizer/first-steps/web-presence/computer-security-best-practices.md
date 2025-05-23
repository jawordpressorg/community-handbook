# Computer security best practices

As a WordCamp.org admin-level user, your account has access to sensitive information and the ability to make potentially damaging changes. We take security seriously, but security is only as strong as its weakest link, so it is important that you go above and beyond to make sure your personal computer, passwords, and data are secure.

**You are a target.** Contributors have been specifically targeted in the past (personal accounts included), so always be on the lookout and be sure to immediately report anything strange to us. For a good read on why this is important, and why even one insecure account can lead to escalation, [see how Mat Honan at Wired got hacked](https://www.wired.com/2012/08/apple-amazon-mat-honan-hacking/). Here are some things you need to do and keep in mind before gaining Super Deputy access. Some things seem tough at first, but after a while they become habits and are second nature.

## General Password Hygiene

*   Never give your password, passphrase, or passcode to anyone else, no matter how nicely they ask and regardless of their familial or romantic status.
*   No two passwords should **ever** be the same – even if they are “throw away” passwords.
*   To manage these passwords, you should use a password manager. [1Password](https://1password.com/) and [LastPass](https://www.lastpass.com/) are two we recommend. Lastpass has some cool features, but 1Password has an infinitely better design. This is a SPOF (single point of failure), so use a long passphrase (at least four words) with special characters.
*   Be sure to use [high entropy passwords](https://en.support.wordpress.com/selecting-a-strong-password/#how-to-create-a-passphrase) everywhere. If you are using a randomly generated password, it should be at least 24 characters and have numbers, mixed case letters, and symbols. Use passphrases for the passwords you need to “remember”, like your Apple account, your computer, and your password manager.
*   Passwords and passphrases should not be constructed from known phrases. For example, “Ph’nglui mglw’nafh Cthulhu R’lyeh wgah’nagl fhtagn1.” is a bad password even though it has varying capitalization, punctuation, spaces, and is an excellent length. That password was [cracked in *minutes*](https://arstechnica.com/information-technology/2013/08/thereisnofatebutwhatwemake-turbo-charged-cracking-comes-to-long-passwords/) because it was a known fictional phrase from the H.P. Lovecraft short story *The Call of Cthulhu*. Avoid all known phrases, as it is likely that a given phrase is on or will be on a password cracker word list. Instead, mix and match disparate words to create a truly unique password or passphrase.
*   Do not store the 1Password file in Dropbox or any other online service *unless* you have enabled 2-step authentication for that service *and* your 1Password file has a very strong master password.  The safest thing to do is to just make a local backup in case your computer is damaged or lost. But we understand that syncing to multiple devices is very handy.
*   Do not store any passwords in a Google Doc or other online service, even if you have enabled 2-step authentication. Again, use a password manager to secure your passwords.

## Web

*   Enable [2-factor authentication](http://searchsecurity.techtarget.com/definition/two-factor-authentication) (2FA) for every important site that supports it.
    
    *   [Never use SMS-based 2FA](https://www.schneier.com/blog/archives/2016/08/nist_is_no_long.html), unless it’s the only option. Whenever possible, use an app to generate the one-time passwords.
    
    *   Here are some setup guides for a few sites: [Apple](https://support.apple.com/kb/HT5570), [Facebook](https://www.facebook.com/help/909243165853369/?helpref=hc_fnav), [Twitter](https://support.twitter.com/articles/20170388), [Dropbox](https://www.dropbox.com/help/363/en), [GitHub](https://help.github.com/articles/about-two-factor-authentication/), [LastPass](https://support.logmeininc.com/lastpass/help/enable-multifactor-authentication-lp010002), [Box](https://support.box.com/hc/en-us/articles/360044195853-Configuring-Two-Step-Login-Verification), [Gmail](https://support.google.com/accounts/answer/180744?hl=en), [Yahoo](http://help.yahoo.com/kb/index?page=content&y=PROD_ACCT&locale=en_US&id=SLN5013), [GoDaddy](https://www.godaddy.com/help/what-is-2-step-verification-31995), [LinkedIn](https://www.linkedin.com/help/linkedin/answer/531/two-step-verification-overview?lang=en), [Dreamhost](https://help.dreamhost.com/hc/en-us/articles/216013897-Multifactor-Authentication-overview), [Namecheap](https://www.namecheap.com/support/knowledgebase/article.aspx/9253/45/how-to-two-factor-authentication), [PayPal](https://www.paypal.com/us/cgi-bin?cmd=xpt/Marketing_CommandDriven/securitycenter/PayPalSecurityKey-outside&bn_r=o), and [Microsoft/Live.com](http://windows.microsoft.com/en-au/windows/two-step-verification-faq).
    *   For a more comprehensive list of sites supporting 2-factor authentication, see [Two Factor Auth List](http://twofactorauth.org/), and enable 2-factor authentication on each that you use.
*   For your self-hosted WordPress site you can use the [Google Authenticator](https://wordpress.org/plugins/google-authenticator/) or the [Duo Security](https://duo.com/docs/wordpress) plugin.
*   Make sure all your WordPress installations are following the best practices for security.
*   **Do not** store your 2-factor recovery codes online or in your password manager. Print them and put them in a safe place in your house instead.
*   Ensure that you are using strong passwords everywhere, even on accounts not directly connected to WordPress.org. [GitHub](https://github.com/) is a good example. 1password allows you to sort your logins by “Password Strength” so you can easily prioritize which accounts need better passwords.

## Computer

A lot of contributors uses Macs, which are generally pretty good but still need anti-virus, secure device password, and encryption set up properly. Similar advice applies to Windows and Linux.

*   Set a system [passphrase](https://en.support.wordpress.com/selecting-a-strong-password/#how-to-create-a-passphrase) (at least four words) on your computer, even if it is a desktop and you live alone. Make sure the password is required to wake from sleep or from the screen saver.
*   Have the screen saver turn on in 15 minutes or less if unattended. You can configure [a shortcut](https://www.macworld.com/article/1049080/software/lockscreen.html) to enable the screen saver, which you should do whenever you get up from your computer.  If you use Alfred, you can have it “lock.”
*   Encrypt your hard drive. You can use [FileVault](https://support.apple.com/kb/HT4790) on OS X, and [BitLocker](https://www.howtogeek.com/192894/how-to-set-up-bitlocker-encryption-on-windows/) or [DiskCryptor](https://ssd.eff.org/en/node/49 "How to: Encrypt Your Windows Device") on Windows. On Linux systems, encryption is usually offered when you install your system, but if you’ve already installed it, then you will probably need to re-install.
*   Make sure your backups are encrypted. [Here’s how on OS X Time Machine](https://support.apple.com/en-euro/guide/mac-help/mh11421/mac).
*   Install and run anti-virus software with the latest virus definitions. [Microsoft Security Essentials](https://support.microsoft.com/de-de/help/14210/security-essentials-download) is good for Windows 7 (it is built into Windows 8 and up under the name Windows Defender) and [Sophos](https://home.sophos.com/mac) for OS X. Both are free. (If you have trouble with proxy connections after installing Sophos, [try this workaround](https://cloudup.com/cCq4WF7KUVM).)
*   When connecting to any WordPress.org sites, always use the proxy.
*   Your SSH private key **must** have a strong passphrase. Neither the passphrase nor the key itself should be stored online in a service like Dropbox. You should make a backup of the key to an encrypted external hard drive, Time Capsule, or USB stick. **Never** store the key and the passphrase in the same place.
*   Turn on your firewall.
*   Consider running a “reverse firewall” like [Little Snitch](https://www.obdev.at/products/littlesnitch/index.html), it is noisy at first, but then gets quieter as you set up your rules.
*   *After you have set up two-factor authentication for your Apple account,* you should [turn on Find My Mac](https://www.apple.com/icloud/setup/mac.html) to allow your device to be remotely locked and wiped if the need ever arises.
*   Make sure your home router firmware is current and you aren’t using the default password. Also review any port forwarding settings to make sure they are all needed and expected. Remove anything you are not currently using. (We have seen hacked routers, which means the router can capture your traffic.)
*   Don’t use wireless keyboards from Microsoft, because they are vulnerable to eavesdropping. Use a Bluetooth keyboard instead.

## Phones and Tablets

*   [Don’t use a simple passcode](https://support.apple.com/kb/HT4113) (4 digits). Use a strong one, if it is all digits, you will still get the fast number entry form rather than a full keyboard.
*   If you are on Android, [encrypt your device](http://www.howtogeek.com/141953/how-to-encrypt-your-android-phone-and-why-you-might-want-to/). iOS turns on “Data Protection” [automatically](http://searchconsumerization.techtarget.com/tip/How-iOS-encryption-and-Data-Protection-work) when you set a passcode [which is not great](http://www.zdziarski.com/blog/?p=2149) but better than nothing.
*   You can use [Google Authenticator](https://support.google.com/accounts/answer/1066447?rd=1), [Duo Security](https://www.duosecurity.com/), [Authy](https://www.authy.com/) or [FreeOTP](https://fedorahosted.org/freeotp/) (which is FOSS) to scan your two-factor codes.
*   SMS is very insecure, so use a messaging app with end-to-end encryption instead, and encourage your contacts to as well.
    *   [Signal](https://www.signal.org/) is the gold standard, and can replace the default SMS app. Wire and Threema are also good.
    *   [WhatsApp and FB Messenger are problematic](https://www.securemessagingapps.com/), but still much better than SMS.
    *   If you want to dig deep, or secure messaging is critical for you, be aware [that there’s a lot of complexity](https://www.eff.org/deeplinks/2018/03/secure-messaging-more-secure-mess).
*   Add a PIN to your cell carrier account to [protect against SIM swapping](https://www.vice.com/en_us/article/zm8a9y/how-to-protect-yourself-from-sim-swapping-hacks).
*   Use [iCloud’s Find My Phone on iOS](https://www.apple.com/icloud/features/find-my-iphone.html). On Android use the Google’s [Android Device Manager](https://www.google.com/android/devicemanager) and it’s [app](https://play.google.com/store/apps/details?id=com.google.android.apps.adm&hl=en), [Cerberus anti theft](https://www.cerberusapp.com/) or [Lookout](https://play.google.com/store/apps/details?id=com.lookout&hl=en).
*   Consider scanning your two-factor codes into two devices, like a phone and a tablet.
*   iOS: Having it erase your device after 10 passcode fails is up to you, but we generally do not recommend it, as sometimes pockets or kids can set this off.
*   iOS: [Encrypt your to-computer backups](https://cloudup.com/cuVfSHIiFY0).

## Is It All Worth It?

Yes. Think of how much you value everything on your computer and on web services: photos of your loved ones, correspondence, financial information, your writing. Multiply that by all the people who have shared their information on a WordPress.org/WordCamp.org/community website. Even a single contributor getting hacked puts every other contributor and all our users at risk. We trust organizers to take this seriously.

## We’re At Your Service

*   If you notice anything suspicious on your accounts such as weird behavior or emails you don’t recognize, [let us know immediately](mailto:support@wordcamp.org).
*   If you have any questions about anything above, [let us know](mailto:support@wordcamp.org).

<!--
*   [To-do](# "To-do")
-->
