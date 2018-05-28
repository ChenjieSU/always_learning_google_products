# always_learning_google_products/google_analytics/03-google_analytics-for_beginners/part_1.md

Notes for Part 1 of the Advanced Google Analytics class at the Analytics Academy.

# Part 1. Data Collection and Processing

## 1.1 Google Analytics data collection

Getting the impression it's easier to study the transcript than the video.

### 1.1.1 Video: How Google Analytics collects data (5:39)

- Teachers: Justin Cutroni and Krista Seiden - analytics advocates.

Website data collection:

- Tracking code: tracks each user interaction on the site: page loads, button clicks, etc.
- Analytics tracks this by dropping a cookie in user's browser for the site
- Note: using the same tracking code on different sites causes Analytics to count the sessions separately
  - Cross-domain tracking: tracking users on multiple sites - covered later

Anatomy of a "hit:"

- Each user interaction on the site is a "hit" sent to Google Analytics
- Each hit is a URL string sent to google with several parameters set, for example:
  - User's language
  - Page being viewed
  - Resolution of user's screen
  - Analytics ID from the tag
  - Randomly-generated user identifier, allows identifying new and returning users
- Most common hit types are:
  - "pageview" - user loads page with tracking code
  - "event" - user interacts with a particular element, e.g., a button
    - additional data: event action, category, label, value
    - allows categorization of user interactions
  - "transaction" - aka. "ecommerce" hit, passes data about purchases, transaction IDs, SKUs, etc.
- Other hit types:
  - "social hits" - likes, shares, tweets
  - "page timing hits" - allow timing how long it takes the site to load css, js, images, etc.
- Other parameters sent with hit data:
  - IP address, server log files, ad-serving data
  - Allows understanding: user's location, browser and os specifics, age, gender, and referring source/medium
- All parameters become dimensions in Analytics reports

## 1.2 Categorizing into users and sessions

Starting to think it's easier to study the transcript than watch the video, and keep having to stop it to take notes.

### 1.2.1 Video: Categorizing data into users and sessions (6:06)

- How Google Analytics processes data:
  - Determines whether user is new or returning
  - Categorizes hits into sessions
  - Combines data from the tracking code with other data

New vs. Returning Users

- User loads page -> Google generates random ID for user's cookie
  - If there is an existing ID, user is returning, else they are new
  - This is not explained very well...
- Limitations:
  - Technique can be thwarted if user disallows or clears cookies
  - Different devices are interpreted as different users, unless User ID feature is turned on (covered later)

Defining sessions

- Sessions begin when users first visit the site
- Sessions end after 30 minutes pass without any hits
- Examples:
  1. User loads page and leaves immediately: single pageview hit for a single session
  1. Pageview hit -> watches video (event hit): 1 pageview and 1 event hit in a single session
  1. Pageview hit -> distracted for 30+ mins -> watches video: two separate sessions, one hit each (in same browser tab)
- 30 minutes is the default, and can be changed
  - How to change the default: https://support.google.com/analytics/answer/2795871?hl=en

Joining Google Analytics data with other sources

-

## 1.3 Applying configuration settings

### 1.3.1 Video: Transforming data using configuration rules (5:12)

## 1.4 Storing data and generating reports

### 1.4.1 Video: Storing data to generate reports quickly (5:44)

## 1.5 Creating a measurement plan

### 1.5.1 Video: How to create a measurement plan (3:00)


## 1.6 Assessment 1:

