# TODO.md

This file lists changes I need to make to my sites in order to bring them up-to-date with the latest recommended techniques.

These changes are based on what I am learning by going through the Analytics Academy's Google Analytics for Beginners class.

# Changes Needed - From the Google Analytics for Beginners Class

## From Part 1 of the Google Analytics for Beginners Class

### From Part 1, Section 3 (1.3 Google Analytics setup):

- Move the tracking code snippet from the end of the file to just after the `<head>` tag.

### From Part 1, Section 4 (1.4 Demo):

**DONE.**

- Create three views for each site, as demonstrated in this section:
  - Raw Data
  - Test View
  - Master View
- Create filter for my IP address in the Test View
- Test the filter
- Copy it to the Master View
- Extra: while we're at it, go ahead and link up my AdSense account:
  - Admin -> Property -> (Under Product Linking) AdSense Linking
  - Select AdSense for Content -> Continue
  - Link all views -> Enable Link -> Done
  - AdSense acct number: pub-2594011034406643

## From Part 1 of the Google Analytics for Beginners Class

**DONE.**

### From Part 1, Section 3 (3.1 Audience reports):

- In Analytics: Enable Demographics and Interest Reports:
  - Click Audience in left nav -> Demographics -> Overview
  - Click Enable and wait a day or two
  - OR: Admin -> Property tab -> Property Settings
  - Turn on "Enable Demographics and Interest Reports" -> Save

# Changes Needed - From the Advanced Google Analytics Class

## From Part 2 of the Advanced Google Analytics Class

### From Part 2, Section 1 (2.1 Managing multiple accounts):

References:

- Link to section: https://support.google.com/analytics/answer/7165242?hl=en
- Link at end of section: https://support.google.com/analytics/answer/1033876?hl=en

- Set up cross-domain tracking for seeourminds.com and groja.com

**Note:** This is easier using Google Tag Manager, so hold off on this until after taking that class.

### From Part 2, Section 5 (2.5 Understand user behavior with Event Tracking):

#### Section 2.5: Event Tracking

References:

- Link to section: https://analytics.google.com/analytics/academy/course/7/unit/2/lesson/5

SeeOurMinds.com: write up a short measurement plan and set up goals and conversions for the following actions:

- Home page, minor conversion:
  - click on one of the main buttons
- Gallery page, minor conversions:
  - Click on "Show the Whole Story"
  - Click on an image to enter a gallery
  - Click on an image to see its image page
- Image page, minor conversions:
  - Click on "Explain the [color]"
  - Click on "Show the Whole Story"
- Major conversions:
  - Complete one of the quizzes - must capture which one
  - Sign up for the email list

**Note:** Set up **only** these goals for now.
This is probably easier to do with Google Tag Manager, so hold off on doing
more than this until after taking that class.

### From Part 2, Section 6 (2.6 More useful configurations):

#### Section 2.6: Site Search

- Second drop down on this page is about setting up site search.
  - https://analytics.google.com/analytics/academy/course/7/unit/2/lesson/6

**We will want to do this eventually, for seeourminds.com, at least, but not right now.**

References:

- Transcript of video: https://support.google.com/analytics/answer/7165643?hl=en

### More Ideas, From After Taking the Class

#### Link Analytics to Search Console

**DONE.**

Learned from clicking on alerts (bell icon in header).

- Admin -> (Under Property, Product Linking) All Products
- Search console (scroll down if necessary) -> Link Account

#### Enable Enhanced Link Attribution (??)

**Maybe later.**

Learned from looking at the Property Settings.

- In-page Analytics:
  - Admin -> (Under Property) Property Settings
  - Enable Enhanced Link Attribution
  - Need to change the tracking code required
  - "How to setup..." link says the extension will no longer receive updates
  - Hmmm.  Looks like this may be going away, and I am not sure what this does anyway.
  - **Check out later**

