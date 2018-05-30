# always_learning_google_products/google_analytics/03-advanced_google_analytics/part_3.md

Notes for Part 3 of the Advanced Google Analytics class at the Analytics Academy.

# Part 3. Advanced Analysis Tools and Techniques

## 3.1 Segment data for insight

Continuing to first study the transcript, then watch the video.

### 3.1.1 Video: Introduction to segmentation (5:30)

- Segmentation: allows viewing a subset of data in a report
  - A differently-colored line represents each segment in the graph
- User segments: can span multiple sessions in a date range (max. 90 days)
  - Can segment by date range demographics: age range, gender
- Session segments: behavior within a single session
- Can add multiple segments to a single report
- Can compare users who purchased to those that didn't
- Can build segments using dimensions, metrics, dates, and sequences of actions
- Audience Overview and other reports: the default is the All Users segment
  - Click Add Segment to add a segment - see Click through the guide below
- Type 1 - Default or System segments:
  - Examples: Tablet traffic, New Users, Returning Users
  - Applied to every report until you remove it or exit Google Analytics
- Can display up to four segments at a time
- Actions drop-down:
  - Copy: to copy and edit segment
  - Build audience: for remarketing (covered later)
- Type 2 - Custom segments: deined by admins
  - See the "Click through the guide" below
  - Can specify multiple filters, example: age 25-34 + language "es"
  - Can specify sequences - mix of pageviews and events
- Click on Share segments to import and share segments
  - Does not share any of the data
- Segments are applied after sampling

### 3.1.2 Click through the guide

Audience -> Overview report:

- Use Custom Segments to analyze subsets of data
- Process:
  - Click on Add Segment near top of report
  - Click on New Segment button (red)
  - Enter Segment Name
  - Click on Conditions (under Advanced on the left side of the report)
- Filter settings in the segment creator (short video)
  - Include or exclude data, based on session or user
    - User: want to look at all sessions for users who land on the page, regardless of how many sessions they did it
    - User filter: choose when want to look at users who complete an action, regardless of the session
    - Sessions: includes only the sesssions in which the user landed on the page
- Process (cont'd):
  - Set filters: Users [or Session] and Include [or Exclude]
  - Set Dimension Selector: "Landing Page"
  - Set Operator Selector: contains [or exactly matches or starts with or ends with or matches regex or is one of or...]
  - Enter a value in the Input Field: "android" to identify any users who land on a page with "*android*" in the URL
  - Summary Preview: what percentage of users first landed on an Android page
  - Save
  - View custom segment
  - Ensure correct date range is selected
  - Note increase in pageviews metric
  - In left nav, Geo -> Location
  - Note increase in new users

### 3.1.3 Complete the activity: 3/3 - 100% (first try)

## 3.2 Analyze data by channel

Studying the transcript instead of watching the video.

### 3.2.1 Click through the guide

- Using the Channels Report for Analysis:
  - Acquisition -> All Traffic -> Channels
- Channels report table - shows data segmented by channel: Direct, Display, Email, Organic Search, Social, etc.
  - Display channel: AdWords or DoubleClick campaigns, served on the Google Display Network
  - Paid Search channel: Advertising in Google Search
- Conversions menu drop-down: in heading of the Channels report table - shows goals
  - Select Goal 1: Purchase Completed
- Set date range and check the compare to previous period checkbox
- Apply android segment created in previous lesson
- Remove All Users segment (down arrow in box -> Remove)
- Compare conversion columns - Purchase Completed
- Sort channels by Conversion rate (click on column header)
- Sort channels by New Users (click on column header)
- Click into Referral channel and note referral sources - note which ones are performing the best

### 3.2.2 Video: Using Multi-Channel Funnel reports for analysis (4:24)

Attribution Modeling

- Set of rules determining how to credit conversions
- By default: "last click" attribution model - only the last one before the conversion counts

Multi-Channel Funnel (MCF) reports

- Reports showing what role prior marketing efforts have played
  - Learn what efforts should be credited with an "assisted conversion"
  - Can see how long it took to go from initial interest to purchase
  - Includes interactions with paid and organic search, referral sites, affiliates, social, email
- Conversions -> Multi-Channel Funnel reports -> Overview report
  - Total conversions, and which were click-assisted, impression-assisted, or rich media-assisted
- Conversions -> Multi-Channel Funnel reports -> Assisted Conversions report
  - Higher numbers -> more the channel helped with the conversion
- Conversions -> Multi-Channel Funnel reports -> Top Conversions Paths report
  - Shows channel combinations that led to conversion
- Conversions -> Multi-Channel Funnel reports -> Time Lag report
  - Time in days from initial interest to conversion
- Conversions -> Multi-Channel Funnel reports -> Path Length report
  - Average number of interactions it took to convert
- All show which channels are contributing to the conversion rate

### 3.2.3 Complete the activity: 3/3 - 100% (first try)

Note: For question 2, Analytics displayed a warning about looking at a filtered view.
I ignored this warning and was able to choose the correct answer regardless.

## 3.3 Analyze data by audience

### 3.3.1 Click through the guide (no video for this section)

Using Activity, Cohorts, and Benchmarking for Audience Analysis

- Active Users report: Audience -> Active Users
  - Number of unique users who initiated sessions in the last 1, 7, 14, or 30 days
  - Sudden, short-term drops: may be due to bad press or social content
  - Long-term drops: possible issues with site code or marketing efforts
- Cohort Analysis report: Audience -> Cohort Analysis
  - Examine groups of users and their behavior
  - Report options - drop-downs in header:
    - Cohort Type - Acquisition Date: cohorts grouped by when they stared their first session
    - Cohort Size - Group by day, week, or month
    - Metric - User Retention (default), Goal Completions, Pageviews, Revenue, Session Duration, etc.
    - Date Range - Last 7, 14, 21, or 30 days
  - Example - compare revenue across cohorts:
    - Size: by week
    - Metric: Revenue per User
    - Date Range: Last 9 weeks
  - Review report: builds a table showing avg. revenue per user
    - Top row: avg. revenue per user for all users
    - Analyze cohorts: other rows, avg. revenue per user for each cohort
    - Heatmap: darker blue -> higher numbers, lighter blue -> lower numbers
  - Apply android landing page segment
  - Compare segments to analyze marketing campaign efforts
- Benchmarking report: Audience -> Benchmarking
  - Compare your data with aggregated, anonymized data from other companies
  - Audience -> Benchmarking -> Channels
    - Toolbar: dropdowns to select industry vertical, region, and session size
    - Example: All Shopping, US -> All Regions, 5000-9999
    - Green up arrows -> better than average, Red down arrows -> not that great
    - Heatmap: darker cells -> larger differences
  - Audience -> Benchmarking -> Location
    - Compare to industry numbers for selected location
  - Audience -> Benchmarking -> Devices
    - Look at separate numbers for desktop, mobile, and tablet traffic
    - Details toggle: icon in upper left corner of data table header
    - Heatmap toggle: icon in upper left next to details toggle

### 3.3.2 Complete the activity:



## 3.4 Analyze data with Custom Reports

### 3.4.1 Click through the guide (no video for this section)



## 3.5 Assessment 3:

