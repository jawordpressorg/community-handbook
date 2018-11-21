# Personalized Badges with InDesign

InDesign’s Data merge is a wonderful feature that allows you to generate several unique PDFs from a single CSV file. This is traditionally used to print thousands of envelopes or mailers, each with a unique address or some other varying information. We can use this feature to print a large amount of conference badges, perfect for WordCamps! This example in this article will produce a badge that includes a first and last name, Twitter handle, and a Gravatar.

If you don’t have a copy of InDesign, you can [download a trial version](http://www.adobe.com/products/indesign.html). If you have a layout program that you prefer to InDesign and have already written a script for it – or would like to work with us to write a script – please email [support@wordcamp.org](mailto:support@wordcamp.org) to tell us all about it.

### Step 1: Getting the CSV file

If you’re using CampTix to sell your WordCamp tickets, then you can export your list of attendees as a CSV file. The CSV file will include a bunch of columns that you don’t need, so you can clean it up and delete those columns in a spreadsheet editor. The only columns you need are the ones that will be on the badge (First Name, Last Name, and Twitter) plus their email so that their Gravtars can be slurped. It should look something like this:

First Name,Last Name,Email,Twitter
Kaylee,Fry,shinykaylee@gmail.com,@shinykaylee
Simon,Tam,simon.tam@osirismed.edu,@simontam
Malcolm,Reynolds,mreynolds4@browncoats.mil,@captainreynolds
Jayne,Cobb,stud1234@aol.com,@themantheycalljayne

The file won’t have the Gravatar info at this point, but we’ll get to that next.

#### Grabbing the attendees’ Gravatar

Next you’ll need to run a script that will take the CSV of CampTix attendees, download their Gravatar images (based on the email that the attendees gave), and generate a new CSV with an additional column for the images.

To run the script, you’ll need to give us two things: the CSV file with the attendees’ info and the local file path on your personal machine where you’ll keep all of the images (for the data merge to work, you have to store all of the images locally). For example:

Macintosh HD:Users:Dave:Desktop:wordcamp-badge-images:

We’re working on making this process more user-friendly, but for now it’ll be easiest if you ask a developer on your team for help.

1.  [Download a copy of the script](https://gist.github.com/iandunn/5ccc8f8a01ccb1a981c3).
2.  Move it into a WordPress installation folder
3.  Update the configuration values in the first 20 lines to match you environment
4.  From the command line, run ‘php camptix\_gravatar\_badges.php’

This will look for the Gravatars in a folder named “wordcamp-badge-images” on user Dave’s Desktop. You can read more about the path syntax and how to determine it in [this InDesign data merge help doc.](http://help.adobe.com/en_US/indesign/cs/using/WSa285fff53dea4f8617383751001ea8cb3f-6c3ca.html#WSa285fff53dea4f8617383751001ea8cb3f-6c37a) After running the script, your new CSV file should look like this:

First Name,Last Name,Email,Twitter,@Gravatar
Kaylee,Fry,shinykaylee@gmail.com,@shinykaylee,"Macintosh HD:Users:Dave:Desktop:wordcamp-badge-images:kaylee-fry.jpg"
Simon,Tam,simon.tam@osirismed.edu,@simontam,"Macintosh HD:Users:Dave:Desktop:wordcamp-badge-images:simon-tam.jpg"
Malcolm,Reynolds,mreynolds4@browncoats.mil,@captainreynolds,"Macintosh HD:Users:Dave:Desktop:wordcamp-badge-images:malcolm-reynolds.jpg"
Jayne,Cobb,stud1234@aol.com,@themantheycalljayne,"Macintosh HD:Users:Dave:Desktop:wordcamp-badge-images:jayne-cobb.jpg"

Note that the header for the image column has to begin with “@”. This lets InDesign know that that column contains images.

*Some additional things that the script does:*

*   If no Twitter handle was provided, then fill in the empty cell with their first name. Depending on the badge design, you may just want to leave that cell blank.
*   If the attendee didn’t put “@” at the beginning of their Twitter handle, add it in.
*   If the attendee has no Gravatar, add in “mystery-man.jpg” as the filename. The “mystery-man.jpg” will serve as the fallback image.

### Step 2: Setting up the InDesign file

Now that you have a proper CSV file you can create the merged document. If you have any static artwork, place it in a Master page, and then make sure that your first page has that Master page applied. Next, place text frames and image frames (if you’re using images) where you’d like the varying content to go. It’s easier to adjust the font, color, size, etc. after you have placed the content from the CSV file.

You can download [our sample template](http://cl.ly/383Z0i0Q102I), or make your own.

#### Using the Data Merge panel to place the content

Make sure you have the Data Merge panel open by going to Window > Utilities > Data Merge. Select your CSV file by going to Select Data Source… in the flyout menu.

[![screen-shot-2013-07-31-at-10-55-15-am](https://plan.wordcamp.org/files/2013/09/screen-shot-2013-07-31-at-10-55-15-am-300x169.png)](https://plan.wordcamp.org/files/2013/09/screen-shot-2013-07-31-at-10-55-15-am.png)

The panel now lists all of the headers for the columns in the CSV file. Start by dragging items from the list onto the corresponding text and image frames on the canvas. This will fill the frames with the header name wrapped in angle brackets, e.g. <>. The same will happen when you place an image from the list in an image frame, but the output will be the image specified in the path in the CSV file. To adjust how the image fills the frame, go to Content Placement Options… in the flyout menu. There are several options here such as removing blank lines if the values are empty and linking images instead of embedding them. Here’s what my Data Merge panel looks like after placing a couple things:

[![screen-shot-2013-07-31-at-11-22-33-am](https://plan.wordcamp.org/files/2013/09/screen-shot-2013-07-31-at-11-22-33-am.png)](https://plan.wordcamp.org/files/2013/09/screen-shot-2013-07-31-at-11-22-33-am.png)

### Step 3: Exporting the PDF

After you’re done, you can preview the document with the checkbox in the panel and check for correct copyfitting. Click on the arrow icon in the bottom right of the panel when you’re done to create a merged InDesign document or click on Export to PDF in the flyout menu to export a PDF directly. In the panel that appears, make sure that “Generate overset text report with document creation” is selected. This will give you a warning if any of your codes are too long to fit inside their textbox container. Here is an example of one of the badges before and after the merge:

[![screen-shot-2013-07-31-at-11-12-22-am](https://plan.wordcamp.org/files/2013/09/screen-shot-2013-07-31-at-11-12-22-am-300x197.png)](https://plan.wordcamp.org/files/2013/09/screen-shot-2013-07-31-at-11-12-22-am.png)

It’s important to note that you can have several text frames with the same header value, which is how I made the shadowed text effect. It’s just 3 different text frames on top of each other, each set in a different font.

Depending on the printer’s preference, you may need to split the generated PDF into separate ones.

The possibilities are endless! You can run the PDF through a batch Photoshop action to automatically apply some texture to the badges if you wanted.

### Help Make This Better

This process is the first iteration of this functionality, and there’s a lot of room for improvement. If you’d like to help make it better, you can contribute feedback and code to [#262-meta](https://meta.trac.wordpress.org/ticket/262).

*   [To-do](# "To-do")