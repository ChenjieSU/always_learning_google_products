# always_learning_google_products/google_analytics/03-google_analytics-for_beginners/part_2.md

Notes for Part 2 of the Advanced Google Analytics class at the Analytics Academy.

# Part 2. Setting up Data Collection and Configuration

## 2.1 Organize your Analytics account

Continuing to first study the transcript, then watch the video.

### 2.1.1 Video: Managing multiple accounts or properties (5:26)

- Simplest set up: a single organization, account, and property
  - Create three views for each property: Raw, Test, and Master

Accounts

- These are Google Analytics Accounts, NOT email accounts
  - To create a GA account: Analytics -> Admin
- Each GA account has a unique Account ID, contained in the tracking code
- An agency managing accounts for multiple companies:
  - Set up an Organization for each company
  - Create a separate GA account under each Organization
- To switch accounts:
  - Use the account selector (top left of the analytics page) OR
  - Access the Admin page

Properties

- Each account may contain multiple properties
- Each property is identified by a unique Propert ID, appended to the Account ID
- Access properties in the Admin window -> Property selection pull-down (middle of page near the top)
- Set up a property to organize a data set independently
  - Recommended: use different properties for website, a mobile app, or other device
- Cross-domain tracking: aka. "site linking"
  - Recognizes when a user navigates between related sites or subdomains in a single session
  - Enables tracking both in a single property
  - Must modify tags - this is easier when using Google Tag Manager
  - Google Analytics 360: can use "rollup reporting" to aggregate data into a new combined property
    - Example: combine website and mobile app data (in separate properties) into a third combined property
    - Note: the combined property does not inherit imported data, must set that up manually

User permissions

- Limitations:
  - Each GA account has a limited number of properties
  - Each property has a limited number of views
- Example: Can create a different view for each department
- Use the Admin page -> View pulldown to navigate between views
- Google Merchandise Store: medium-sized business
  - Single account, single property, three views

## 2.2 Set up advanced filters on views

Studying the transcript instead of watching the video.

### 2.2.1 Video: How to set up advanced filters on views (6:38)

- Filters: refine data
  - Example: track a specific subdomain or directory in separate views
- Two types: predefined and custom

Predefined Filters

- Predefined: simply need to select the ones you want to use
- Examples: Filter by ISP domain, IP addresses, subdirectories, hostname

Custom Filters

- Custom: include or exclude hits, format case of data, search and replace
- Include filters:
  - Example - to see mobile data separately: include-only for Device Category "mobile"
  - Example - to see data for a specific campaign: include-only data with the campaign name or type
- Exclude filters:
  - Example - exclude paid search (CPC) traffic
- Lowercase and Uppercase filters:
  - Allows normalizing data, such as URLs
  - Uppercase or lowercase filters: force values and combine rows that differ only by case
- Advanced filters:
  - Use regexes to remove, replace, or combine fields
  - Example: normalize search queries
  - Example: same page but url has different query parameters -> filter out query parameters
  - Example: different domain names but same page url (e.g., index.axd)
    - Use regex to add hostname
- Important factors:
  - Filters apply only after they are created (not retroactively)
  - It may take up to 24 hours for filters to apply
  - Sequence is important:
    - To adjust: Admin -> Filters (in View column, to the right) -> Assign Filter Order
      - Not seeing this in demo acct, and other accounts do not have any filters
  - Can share filters between views
    - Note: Changing a filter in one view changes it in all views
- Use the Test view to test a filter before using it in the master view

## 2.3 Create your own Custom Dimensions

Studying the transcript instead of watching the video.

### 2.3.1 Video: How to set up Custom Dimensions (6:10)

Overview

- Just like default dimensions but you decide the name and value(s)
- Use js tracking code on page:
  - Custom dimension captures page view, action, etc. and sends an additional parameter
- Example: custom dimension in URL to identify employees and apply a discount

Set up

- Process:
  - Admin -> Select Property -> Custom Definitions -> Custom Dimension -> New Custom Dimension
  - Name dimension, set scope to hit, product, session, or user
- Add Custom Dimension
  - Dimensions can only be paired with others when they are in the same scope
  - Active checkbox: active by default, but can un-check to de-activate it at any time
  - First time: given js for the site - copy the js then click Done
  - Taken to overview page listing all custom dimensions - each has an ID (slot number, read-only)
  - Add js tracking code to site - Google Tag Manager can help with this
  - Custom Metric - parameter of index-value pairs
  - Code uses userStatus js var to determine whether user came from employee-only link vs. entering normal retail site
    - Attaches custom dimension ("dimension1") to pageview hit
    - Sent to google, processed into data for the custom dimension and appropriate reports

Using Custom Dimensions in your reports

- Use Custom Dimensions as:
  - Secondary dimensions in reports
  - Primary dimensions in custom reports (discussed later)
- Example - see which products are most popular:
  - Ecommerce -> Conversions -> Product Performance -> secondary dimension: User Category
- Limitations:
  - Cannot be applied retroactively
  - Standard Analytics: up to 20 Custom Dimensions
  - Analytics 360: up to 200 Custom Dimensions

### 2.3.2 Complete the activity: 3/3 - 100%

## 2.4 Create your own Custom Metrics

Studying the transcript instead of watching the video.
Will probably watch the video later, before taking the assessment, to review the material.

### 2.4.1 Video: How to set up Custom Metrics (5:36)

- Examples: number of ads loaded on page, bandwidth page used when loaded
- Collected using js on a page, sent as an additional parameter on the hit
- Example: want to know which marketing channels are working the best
- Process:
  - Admin -> Select Property -> Custom Definitions -> Custom Metrics -> New Metric
  - Name metric, set scope to hit or product
    - Hit: causes metric to increment with each pageview
    - Product: causes metric to increment by cost assigned to product
  - Format: integer, decimal, or time
  - Specify minimum or maximum to exclude very small or very large values from reports
  - Active checkbox: active by default, but can un-check to de-activate it at any time
  - First time: given js for the site - copy the js then click Done
  - Taken to overview page listing all custom dimensions - each has an ID (slot number, read-only)
  - Add js tracking code to website
  - Custom Metric - parameter of index-value pairs
  - Hit causes Analytics to increment the value of the metric
- Concerns:
  - How do you want metrics to appear in reports?
  - How do you want metrics to work with session-level dimensions such as source/medium?
- Google Tag Manager makes managing the js tags easier

## 2.5 Understand user behavior with Event Tracking

Enjoying studying the transcript instead of watching the video.
Will watch the video when reviewing the material later.

### 2.5.1 Video: How to set up event tracking (5:00)

- Use event tracking to learn if and how users are engaging with the site
- Example: track clicks on the global nav bar
- Implementation: add js to the elements you want to track
- Need to set it up for each element individually
- Parameters to define in the js:
  - Category: for organizing disparate events - examples: videos, social, etc.
  - Action: what the user did - examples: play (video), like (post)
  - Label: optional, for further description - example: name of video, title of post
  - Value: optional, numerical value - example: time to load video, how much an event is worth
- These are passed to Analytics with each hit
- Example: to monitor the "Android" link under "Brands"
  - Category: Navigation
  - Action: Brands
  - Label: Android
- Total Events: total number of interactions with the element
- Unique Events: number of unique users who have interacted with the element
- Event reports: under Behavior
  - Top events: organized by category by default
    - Click into Category to see Actions
    - Click into an Action to see the Labels
  - Use links just above table to select the "Primary Dimension:" for the report:
    - Event Category, Event Action, or Event Label
- Suggestion: monitor elements that take user away from site
  - Example: chat button monitored and implemented by a third party
    - Category: Outbound links, Action: Live Chat, Label: Home (or other page title)
    - Learn which pages give users trouble
- Suggestion: to increase engagement, monitor navigation actions and how users interact with content

### 2.5.2 Complete the activity: 3/3 - 100%

## 2.6 More useful configurations

No video for this section.

Instead: "Select from the pulldown menu below to learn about more settings that may interest you:"

### 2.6.1 Demographics and Interests reports


### 2.6.2 Internal Site Search


### 2.6.3 Calculated Metrics


### 2.6.4 Channel Groupings


### 2.6.5 Content Grouping


### 2.6.6 Enhanced Ecommerce


### 2.6.7 User ID


### 2.6.8 Data Import


## 2.7 Assessment 2:

