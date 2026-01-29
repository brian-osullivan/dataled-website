---
layout: post
title: "User engagement in GA4"
category: Analytics
description: Engagement can be a useful leading metric if your site has low traffic.
image: /images/laptop.jpg
permalink: /blog/user-engagement-in-ga4/
---

## Why measure engagement?

Most sites don’t get many conversions — so figuring out performance from conversion rate alone can be tough. Engagement can be a useful leading metric if your site has this issue.

The problem is that no one can agree on what ‘good’ engagement is. And engagement has traditionally been difficult to measure.

## Engagement in Universal Analytics was flawed

Universal Analytics (UA) used a very crude way to measure user engagement: the time difference between when pageviews were sent to the GA servers.

Here are some examples of how UA calculated metrics like time on page, time on site, and bounce rate:

**Example 1: time on page**

A user comes to your site and has 2 pageviews.

The ‘time on page’ for the first page was the time difference between when the 2 pageviews happened — not terrible.

The ‘time on page’ for the second page is 0, there’s no tracking hit after it — not great.

![](/images/1.png)

**Example 2: bounce rate**

A user might come from Google, spend 15 minutes reading your blog post, bookmark the page to return to it and leave the site. A useful visit but still marked as a bounce in UA as there’s only one pageview tracking hit.

\{Illustration\}

## GA4 has a new way to measure engagement

As we just saw, Universal Analytics used the time difference between pageviews to measure engagement.

GA4 has a clever new way of measuring how long people view your pages for.

It measures how long a user actively looks at a tab (or an app). So to measure engagement in GA4, tabs need to be in focus and actively looked at it.

It’s a simple change but it’s a much more effective way to measure how people actually engage with your website.

Bounce rate has also being updated as a part of this change. Any session that doesn’t have a user_engagement event is session with a bounce.

## The user_engagement event in GA4

The user_engagement event in GA4 is sent when a user’s session meets the criteria for being engaged.

There are three ways a session can get marked as being engaged:

1. The user sees 2 or more pages
2. The user spends 10 or more seconds on the site
3. The user completes a conversion

If any of these 3 things happen, you’ll see a user_engagment event in GA4 for that session.

Sessions with the user_engagement event are engaged sessions. Sessions without it, are bounces.

## Engagement in GA4 is better

GA4 removes metrics like ‘avg time on page’ and replaces them with updated engagement metrics.

Let’s run through some of these new metrics:

**Avg engagement time and Avg engagement time per session:** these metrics are both similar. They measure how long, on average, the browser tab was active. The difference is that ‘Avg engagement time’ is per user and ‘Avg engagement time per session’ is obviously per session.

**Engaged sessions/Engaged sessions per user:** As mentioned above, for a session to be classed as ‘engaged’ one of three things needs to happen. i) the user stays on the site for more than 10 seconds, ii) the user sees 2 or more pages, or iii) the user completes a conversion. Engaged sessions per user is calculated by dividing the engaged sessions by users.

**Engagement Rate/Bounce rate** (new and improved): Any session that isn’t classed as ‘engaged’ is a bounce. So the % of sessions with a bounce plus the % of engaged sessions should total 100%. Bounce rate takes a bit of a back seat in GA4, it’s not available by default but you can customize reports to see it.

**Engagement is something the GA4 team got right**

GA4 has been met with a pretty mixed reaction but I think engagement is one of the things that the team has really got right.

In retrospect, engagement metrics in Universal Analytics were pretty terrible.

GA4 uses some clever ways to measure engagement and get a much better understanding of what users do on a site. That should help us optimize our traffic and site.&nbsp;
