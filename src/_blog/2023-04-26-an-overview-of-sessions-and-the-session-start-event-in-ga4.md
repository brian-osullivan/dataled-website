---
layout: post
title: "An Overview of Sessions and the session_start event in GA4"
category: Analytics
description: Sessions are a ‘messy’ metric, so GA4 focuses more on users and events.
image: /images/ga-analytics.jpg
permalink: /blog/sessions-and-session-start-in-ga4/
---

Sessions have always been a core part of GA. But they are a ‘messy’ metric so GA4 focuses more on users and events.

What do I mean by ‘messy’? The way a session is defined is subjective. And the rules used to define sessions can cause weird behaviors in reports.

For that reason, I’d encourage you to lean more on users and events over sessions in your own reporting.

GA4 has a different definition of a session vs Universal Analytics. Let’s get into that definition first, and then talk about the problems it creates.

## How GA4 calculates sessions

In GA4 a session starts when a user opens your site or app. It ends after 30 minutes of inactivity. That’s it, it’s pretty simple.

## How Universal Analytics calculates sessions

Sessions could end in 3 different ways in Universal Analytics:

1. After 30 minutes of inactivity — this is the same as GA4

2. At midnight any existing sessions ended and new ones were created — this doesn’t happen in GA4.

3. If a user’s traffic source changed mid-session the existing session ended and a new one was created. This also doesn’t happen in GA4.

## Why do sessions in GA4 not match with Universal Analytics?

There are a few common reasons why sessions don’t match in Universal Analytics and GA4.

1. The first and most obvious reason is that the way sessions are defined is different. It’s easier to end a session in Universal Analytics (30 minutes of inactivity, a new day, a new traffic source) so you get more sessions vs GA4.

2. Another common reason that session counts differ is that you have a lot more filtering options in Universal Analytics properties.

The filtering in GA4 is pretty limited. It automatically removes bots. You can choose to filter out internal IPs and that’s it.

With Universal Analytics you had powerful filtering at the view level to remove and manipulate data. You could drastically change and reduce the data coming into GA. Filtering out bots was also optional.

1. Lastly, Google states that sessions in GA4 are estimated. So you can’t expect them to be 100% accurate.

## What is the session_start event in GA4?

The session_start event is created automatically in GA4 every time a session starts. A unique ID (ga_session_id) is created for every session at the same time.

A session ends after 30 minutes of inactivity. There is no time limit on a session so in theory they can keep on running and running if there isn’t a 30-minute period of inactivity.

## Why do the session_start and session events in GA4 not match?&nbsp;

There are two reasons why the session_start and session events differ in GA4.

1. Firstly, these are different metrics, and some small differences are expected. For example, a count of sessions for your site last Monday includes all the sessions that happened on Monday. But some of the sessions on Monday might have started on Sunday. So, a user who started their session at 23.55 on Sunday and finished at 00.30 would have a session on Monday but no session_start.

2. Secondly, GA4 calculates the number of sessions that occur on your site or app by [estimating the number of unique session IDs](https://support.google.com/analytics/answer/9191807?hl=en). So this metric isn’t always accurate.

So it’s not expected that sessions and session_starts will be equal — most sites will see higher counts of sessions.

## Why are there sessions with no session_start event in GA4?

This happens for one of the same reasons these metrics don’t match.

A session_start can only happen in one day but sessions can span multiple days. If a user starts a session before midnight and concludes it after midnight, the second day will show a session without a session_start.

## Sessions without pageviews in GA4 - (not set) landing pages

Another quirk of GA4 sessions is that it’s more common to get sessions without any pageviews vs Universal Analytics.

Sessions without any pageviews are the reason you see (not set) in your landing page report.

The culprit here is the way GA4 measures engagement. Most GA4 accounts are automatically measuring things like scroll depth and file downloads.

Here is why this happens. A user leaves a tab without any activity for 30 minutes and then returns to it. They scroll the page but don’t open any new pages. They then leave the site.

A new session gets created as 30 minutes have elapsed since the user last interacted with the site. There is no pageview. But scrolling the page does create a scroll event.

So we get engagement events and a new session but no pageviews. As a result, we’ll see (not set) in our Landing pages report.

## Sessions are a messy metric

As I said at the start of this article, sessions are a messy metric. They’re defined in subjective ways and can lead to odd-looking data in reports like sessions without a session_start and sessions without pageviews. These issues are normal but I would still consider users and events to be more reliable metrics to report on compared to sessions.
