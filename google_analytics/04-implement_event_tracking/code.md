# always_learning_google_products/google_analytics/04-implement_event_tracking/code.md

# Generic Code

On a single-line:

```
ga('send', 'event', [eventCategory], [eventAction], [eventLabel], [eventValue], [fieldsObject]);
```

Alternative syntax, possibly more resilient and flexible:

```
ga('send', {
  hitType: 'event',
  eventCategory: 'Videos',
  eventAction: 'play',
  eventLabel: 'Fall Campaign'
});
```

# References

- General info about events: https://support.google.com/analytics/answer/1033068?hl=en
- How to set up Event Tracking: https://support.google.com/analytics/answer/7165642?hl=en
- Page with important links: https://support.google.com/analytics/answer/1136960?hl=en
- Code to use, and how to use it: https://developers.google.com/analytics/devguides/collection/analyticsjs/events
- Common setup mistakes: https://support.google.com/analytics/answer/1009683?hl=en
- Troubleshooting: https://support.google.com/analytics/troubleshooter/7400465

