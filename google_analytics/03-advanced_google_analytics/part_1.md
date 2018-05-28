# always_learning_google_products/google_analytics/03-google_analytics-for_beginners/part_1.md

Notes for Part 1 of the Advanced Google Analytics class at the Analytics Academy.

# Part 1. Data Collection and Processing

## 1.1 Google Analytics data collection

Getting the impression it's easier to study the transcript than the video.

### 1.1.1 Video: How Google Analytics collects data

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

### 1.2.1 Video: Categorizing data into users and sessions

## 1.3 Applying configuration settings

### 1.3.1 Video: Transforming data using configuration rules

## 1.4 Storing data and generating reports

### 1.4.1 Video: Storing data to generate reports quickly

## 1.5 Creating a measurement plan

### 1.5.1 How to create a measurement plan


## 1.6 Assessment 1:

