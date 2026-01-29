---
layout: post
title: "Bounce rate in GA4"
category: Analytics
description: Why bounce rate has been deprioritized in GA4.
image: /images/google-analytics.jpg
permalink: /blog/ga4-bounce-rate/
---

If you’ve started using GA4 you might be wondering where bounce rate has gone. It was a metric that was pretty central in previous Google Analytics versions and seems non-existent in GA4.

It’s actually still there, but it’s hidden. Why? The GA team has decided to depriortize bounce rate as a metric in favour of other metrics.

I’ll explain why later but first let’s talk about what bounce rate is and how you can actually find it in GA4.

## Why bounce rate?

Most sites only convert a small percentage of users, usually between 2 and 4%.

Measuring the quality of your traffic can be difficult when so few people convert. A couple of conversions either way can skew things a lot. It would be good to have a metric that measures the quality of visits to your site.

Enter bounce rate. The idea is that you use it as a proxy for traffic quality. High bounce rate = bad traffic, low bounce rate = good traffic.

But the way bounce rate was measured in GA prior to GA4 meant it didn’t always correlate with “session quality”.

## How bounce rate is calculated

To understand how well bounce rate can measure your traffic quality, let’s talk about how it’s calculated.

### How bounce rate is calculated in Universal Analytics

Older versions of GA, like Universal Analytics, recorded a bounce when a user visits only one page in a session. Pages that bounce and exit pages also record 0 ‘time on page’.

There are two problems with this approach:

1. There are plenty of use cases where visiting one page on a website can still be a successful session. Reading a blog post, looking up directions or a contact us page, and reading a help article are all good examples.
2. It doesn’t tell you anything about the quality of an individual page. Blog posts can have high bounce rates and 0 ‘time on page’ even if someone spends 15 minutes reading the entire article.

Given this, I think single-page sessions are are a flawed way to measure ‘session quality’.

### How bounce rate is calculated in GA4

GA4 records a bounce if a user:

a) leaves the site after less than 10 seconds and

b) they have only viewed one page and

c) they haven’t converted

It’s more complicated but it’s definitely better. If a user reads a full blog post or help article it’s no longer considered a bounce.

Universal Analytics used the time difference between pageviews to measure ‘time on page’.

_UA ‘time on page’ for pageview 1 = time of pageview 2 - time of pageview 1_

That was a flawed approach because ‘time on page’ was always 0 for exit pages. It had to be, because there was no pageview afterward.

GA4 takes a different approach. It’s always recording how long a users tab is active for. It uses that calculation to measure on-page engagement. It’s a lot more accurate.

### Where to find bounce rate in GA4

Bounce rate isn’t available by default in any of the standard reports. You can customize the standard reports to see it or create an Exploration report and add it there.

Bounce rate makes the most sense as a way to measure landing pages, so now I’m going to show you how to add it to that report.

1. Navigate to Reports &gt; Life cycle &gt; Engagement &gt; Landing page
2. Click the pencil icon in the top right (you’ll need to be an admin to see this icon)
3. Click ‘Metrics’ and then ‘Add metric’.
4. Scroll until you see ‘Bounce rate’ and click it (it’s under the Session heading).
5. Click ‘Apply’ to add it to your report.
6. If you want to keep it you’ll need to click Save &gt; Save to current report. (This changes the report for all users.)

## How to measure “session quality” in GA4?

If bounce rate has been improved in GA4, why isn’t it in any of the reports? I think that’s a good question.

Rightly or wrongly the GA team wanted to focus on engagement instead — you’ll see lots of engagement metrics in GA4.

They measure pretty much the same thing so it’s not really a big deal in my opinion. And like we just saw, you always have the option of customizing your reports to add bounce rate.

Let’s take a look at a couple of the engagement metrics.

### Measure “session quality” with engagement Rate

‘Engagement Rate’ is the inverse of ‘bounce rate’. It’s the percentage of all sessions that didn’t bounce.

_100% - Bounce rate = Engagement Rate_

You can see ‘engagement rate’ in the Traffic and User acquisition reports in the Acquisition section.&nbsp;

### Use avg engagement time to measure “page quality”

If Universal Analytics did a poor job of measuring page quality, it’s an area where GA4 shines.

It measures how long a user's tab is active. Which is good indication if they are engaging with the page.

You can find avg engagement time in the Pages and screens and Landing page reports in the Engagement section.

## “Session quality” metrics are better in GA4

Whether you use the default engagement metrics or customise your reports for bounce rate isn’t all that important IMO. The key point for me, is that GA4 gives you a much better picture of traffic and session quality.

The GA4 team have done that by recognising the issues with the previous metrics and fixing them.
