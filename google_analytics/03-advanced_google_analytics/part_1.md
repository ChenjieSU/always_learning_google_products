# always_learning_google_products/google_analytics/03-advanced_google_analytics/part_1.md

Notes for Part 1 of the Advanced Google Analytics class at the Analytics Academy.

# Part 1. Data Collection and Processing

## 1.1 Google Analytics data collection

Getting the impression it's easier to study the transcript than the video.

### 1.1.1 Video: How Google Analytics collects data (5:39)

- Teachers: Justin Cutroni and Krista Seiden - analytics advocates.

Website data collection:

- Tracking code: tracks each user interaction on the site: page loads, button clicks, etc.
- Analytics tracks this by dropping a cookie in user's browser for the site
  - Browsers store cookies independently for each site
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
    - If this user identifier already exists in the cookies for the site, then they are a returning user
    - Else, if no cookie was stored there, then they are a new user

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
  1. Determines whether user is new or returning
  1. Categorizes hits into sessions
  1. Combines data from the tracking code with other data

**Step 1:** New vs. Returning Users

- User loads page -> Google generates random ID for user's cookie
  - Browsers store different cookies for different sites
  - If there is already a cookie containing an ID for the site, the user is returning, else they are new
- Limitations:
  - Technique can be thwarted if user disallows or clears cookies
  - Different devices are interpreted as different users, unless User ID feature is turned on (covered later)

**Step 2:** Defining sessions

- Sessions begin when users first visit the site
- Sessions end after 30 minutes pass without any hits
- Examples:
  1. User loads page and leaves immediately: single pageview hit for a single session
  1. Pageview hit -> watches video (event hit): 1 pageview and 1 event hit in a single session
  1. Pageview hit -> distracted for 30+ mins -> watches video: two separate sessions, one hit each (in same browser tab)
- 30 minutes is the default, and can be changed
  - How to change the default: https://support.google.com/analytics/answer/2795871?hl=en
- Organizing data by session allows calculating session-based metrics, such as:
  - Number of sessions, pages per session, average session duration, and bounce rate

**Step 3:** Other sources

- Joining Google Analytics data with other sources
- Measurement protocol: send data from a web-connected device, e.g., POS system, kiosks
  - To collect non-Google data, must manually add it to the URL string
  - Measurement protocol details: see Analytics Developer documentation
- Analytics can link to data from AdWords, AdSense, and Google Search Console
  - Allows collecting clicks, impressions, cost data

## 1.3 Applying configuration settings

It seems a bit easier to study the transcript than to watch the video.

### 1.3.1 Video: Transforming data using configuration rules (5:12)

**Step 4:** Apply configuration rules

- Setting up data configuration rules allows control over how data is processed
- Allows filtering and grouping data, setting goals, creating custom dimensions and metrics, and importing data

Data Filters

- Ways to filter a view:
  - Exclude specific data
  - Include specific data
  - Modify data (search and replace)
- Enables aligning data with business needs
- Filters are **rules** applied to data during processing
  - if "filter type" is true, filter is applied, else it is not
- Reasons to apply filters:
  - To transform data: e.g., include data only froma specific country, or exclude internal traffic
  - To help meet specific measurement objectives

Goals

- Types of goals:
  - Most common:
    - Destination or Pageview goals: user views a specific page
    - Event goals: user performs an action defined as an event
  - Not as common:
    - Duration goals: based on session length
    - "Pages or Screens per Session" goals: user views a set number of pages in a session
- User can meet multiple goals per session, but they count as only one conversion
- Conversions and transactions are credited to the last campaign, search, or ad

Channel and Content Groupings

- Channel groupings: organize data into custom channels
- Content groupings: aggregate metrics in reports based on site organization

Custom Dimensions and Metrics

- Can create custom dimensions and metrics
- Custom dimensions: (discussed later)
  - Can be used as secondary dimensions in standard reports
  - Can be used as primary dimensions in custom reports
  - Can be used as a segment
- Custom metrics: can be collected for a standard or custom dimension
- Data import: upload data from external sources, e.g., text file from offline CMS or CRM system

Data Import

- Combine offline data with hit data
- Add context and insight by including business-specific data collected independently
- Must set up configuration rules before gathering data (they cannot be applied retroactively)

## 1.4 Storing data and generating reports

Studying the transcript rather than watching the video.

### 1.4.1 Video: Storing data to generate reports quickly (5:44)

- Process:
  1. Data gathered, configuration settings applied
  1. Data transformed into dimensions
  1. Metrics are associated with these dimensions
  1. Each dimension is stored in its own aggregate database table
- Reports: all based on a single dimension and its corresponding metrics
  - Most reports use rows for dimensions and columns for the associated metric data
- Goals and Enhanced Ecommerce: have their own metrics
- Metrics: calculated using either:
  - Aggregate values: e.g., total sessions, total users, pageviews
  - Specific dimensions: e.g., sessions or new users per country
- Calculating key metrics:
  - Time on page: [timestamp of next page load] - [timestamp of hit for current page]
  - Pages per session: average of unique pageview hits
  - Average session duration: average length of time between first hit and either last hit or session timeout
  - Bounce rate: users who have only one interaction (page view)
- Scope of dimensions and metrics - determined during processing:
  - hit-level
  - session-level
  - user-level
- For pairing, dimensions must be in the same scope
- Must define scope (in a pull-down) for custom dimensions and metrics
- Data is combined into aggregate data tables and processed daily
- This enables quick display of standard reports
- Use of secondary dimensions and custom reports can cause Analytics to:
  - Check for the required aggregate table
  - Possibly fall back to processing raw data and creating the report from scratch
  - Analytics may have to process only a sample rather than all data
- Sampling depends on type of user:
  - Standard Analytics users: sampling occurs at property level (before view-level filters are applied)
  - Analytics 360 customers: sampling occurs at view level so view-level filters don't affect the sample size
- Once data has been filtered, values lost cannot be recovered
- The Google Analytics Core Reporting API can also access Analytics Data
  - Allows importing data into third-party reporting tools

## 1.5 Creating a measurement plan

It's official: studying the transcript is easier than watching the video.

### 1.5.1 Video: How to create a measurement plan (3:00)

- Must define business objectives and how to measure them
  - This determines what data needs to be collected
- Macro conversions: key actions representing broader goals, e.g., a purchase
- Micro conversions: smaller goals supporting the key objectives, e.g., signing up for email
  - Micro conversions nudge users closer to a macro conversion
- Micro and macro conversion examples:
  - E-commerce - micro: newsletter subscription, macro: purchase
  - Lead generation - micro: follow on social media, macro: fill out contact form
  - Content publishing - micro: click into an article, marco: reading a certain number of articles
  - Online information and support - micro: rate an article, macro: completing a flow and solving an issue
- Put all micro and macro conversion into a measurement plan
  - Measurement plan: aligns business objectives with Analytics configuration settings
  - Business objectives
  - Strategies for attaining objectives
  - Tactics to support the strategies
  - Each tactic has one or more key performance indicators (KPIs) for measuring micro and macro conversions
- Macro conversions: often measure tactics
- Micro conversions: metrics used to understand user behavior
- Must identify these conversions before creating a measurement plan
- Measurement plan: aligns business objectives with Analytics configuration settings
- Must create a measurement plan to know how to set up and configure Analytics

Business Objective
- Strategy 1
  - Tactic 1
    - KPI (conversions)
  - Tactic 2
    - KPI (conversions)
- Strategy 2
  - Tactic 1
    - KPI (conversions)
  - Tactic 2
    - KPI (conversions)

### 1.5.2 Interactive Google Merchandise Store Measurement Plan

Business Objective: Sell Google Merchandise
- Strategy: Advertising plan making it easier for customers to make purchases
  - Tactic: Increase referrals to Android merchandise pages
    - KPI: Increase referrals - and resulting increase in customer awareness
    - KPI: Increase new users - and resulting increase in customer awareness
    - KPI: Increase pageviews - and resulting increase in customer awareness
  - Tactic: Increase revenue from Android merchandise products
    - KPI: Increase conversion rate - and resulting increase in revenue
    - KPI: Increase total transactions - and resulting increase in revenue
    - KPI: Increase total revenue - and resulting increase in revenue

Not yet covered?
- Segments (Dimensions) - use the following:
  - Customer Demographics - understand who is visiting pages selling Android merchandise
  - Traffic Sources - understand where the visitors are coming from
  - Device Type - optimize which devices store should optimize for
  - User Category - distinguish purchases by employees from purchases by external customers

## 1.6 Assessment 1: 15/15 - 100%

