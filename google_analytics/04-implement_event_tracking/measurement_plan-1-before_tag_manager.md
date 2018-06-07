# always_learning_google_products/google_analytics/04-implement_event_tracking/measurement_plan-1-before_tag_manager.md

Measurement plan for events we want to track right away, before digging into Google Tag Manager.

# Processes

Adapting these processes for my own purposes.

In fact, I am not doing either of these right now, because I have only a few things I want to track.

**These processes are just to think about,** for future reference.

## From Webris.org

1. Document Business Objectives
2. Create Goals / Strategies
3. Choose Key Performance Indicators (KPIs)
4. Set Targets/Benchmarks
5. Determine Reporting and Segments
6. Analyze, Adjust and Improve

- Reference: https://webris.org/how-to-create-web-analytics-measurement-plan/

## From www.freshegg.co.uk

1. Define your objectives and key performance indicators (KPIs)
2. Consider data segmentation requirements and set targets
3. Create an implementation plan
4. Define the format and frequency for reporting

- Reference: https://www.freshegg.co.uk/blog/analytics/performance-measurement/how-to-create-a-measurement-plan-and-why-you-really-need-one

# Goals: Business Objectives

Some of these may seem atypical, but at this point this is what I want to know.

- Minor conversions:
  - Determine whether people are clicking on the buttons on the Home Page
  - Determine whether people are clicking on the "Explain the [Color]" buttons
  - Determine whether people are clicking on the "Show the Whole Story" buttons
- Major conversions:
  - Note when people complete one of the quizzes - and note which one they do
  - Note when people sign up for the email list, what were they doing before signing up

# Events to Set up on SeeOurMinds.com

Set up goals and conversions on SeeOurMinds.com for the following actions:

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
  - Sign up for the email list
  - Complete one of the quizzes

# Categories, Actions, and Labels

These values are what I really need to decide on before updating the code.

Speaking of "Values," apparently they need to be integers.
Originally I had most of Actions set to "Click," but was seeing no events.
Now I suspect that was because I was using strings for the Values i.e., the values now used as Labels.
Updated all events to use the old Labels as the new Actions, the old (string) Values as the new Labels,
and send 1 as the Value.

## Home Page, Minor Conversion:

- Click on one of the main buttons
  - Category: Button
  - Action: Leave Home Page
  - Label: [See Your Mind, See Their Minds, See My Mind, Learn More]
  - Value: 1
- **DONE**

## Gallery List Page, Minor Conversions:

- Click on a link to enter a gallery
  - Category: Link
  - Action: Enter Gallery
  - Label: [Gallery Page Name]
  - Value: 1
- **DONE**

- Click on an image to enter a gallery
  - Category: Image
  - Action: Enter Gallery
  - Label: [Gallery Page Name]
  - Value: 1
- **DONE**

- Click on [More] or [Less] to show or hide the entire gallery list page teaser
  - Category: Link
  - Action: See Gallery List Page Teaser
  - Label: [Gallery Name]
  - Value: 1
- **DONE**

## Gallery Page, Minor Conversions:

- Click on "Show the Story" Button
  - Category: Button
  - Action: Show Gallery Story
  - Label: [Gallery Page Name]
  - Value: 1
- **DONE**

- Click on [More] or [Less] to show or hide the entire gallery page teaser
  - Category: Link
  - Action: See Gallery Page Teaser
  - Label: [Image Page Name]
  - Value: 1
- **DONE**

- Click on an image to see its image page
  - Category: Image
  - Action: See Image Page
  - Label: [Image Page Name]
  - Value: 1
- **DONE**

## Image Page, Minor Conversions:

- Click on "Explain the [color]"
  - Category: Button
  - Action: Explain the [dom, aux] color: [Blue, Green, Red, Yellow]
  - Label: [Image Title]
  - Value: 1
- **DONE**

- Click on "Hide Explanation"
  - Category: Button
  - Action: Hide Explanation, [dom, aux]: [Blue, Green, Red, Yellow]
  - Label: [Image Title]
  - Value: 1
- **DONE**

- Click on "Show the Whole Story"
  - Category: Button
  - Action: Show Image Story
  - Label: [Image Title]
  - Value: 1
- **DONE**

- Click on "Hide the Story"
  - Category: Button
  - Action: Hide Image Story
  - Label: [Image Title]
  - Value: 1
- **DONE**

## Major Conversions:

- Complete one of the quizzes
  - Category: Complete Quiz
  - Action: Complete Quiz Version
  - Label: [2XS, XS, S, M, L, XL, 2XL]
  - Value: 1
- **DONE**

- Sign up for the email list
  - Category: Join Email List
  - Action: Referring Page
  - Label: Capture [Referring Page] - if possible
  - Value: 1
- **DONE**
- **Note:**
  - Email signup page is on Groja.com
  - If they actually sign up, it sends an email

