---
_schema: default
layout: post
title: Referral Traffic GA4
category:
description: How to create a custom report to see referral traffic.
author: brian
image: /images/website.jpg
date:
permalink: /blog/referral-traffic-ga4/
---
The referrals report is missing from GA4. Unlike many other missing GA4 reports it’s not hiding behind a primary dimension dropdown — if you want to see your referral traffic you’ll need to create a custom report.

But the good news is that recreating the referral report from Universal Analytics is quick and easy.

## Quick recap: what are referrals

Referral traffic comes from links on other sites that are not search engines or ads.

So anybody who backlinks to your site will show up as a referral, providing people actually click on the link.

You might want to see your referrals to:

* See who’s linking to your site — good for SEO.
* Which external links are sending quality traffic — these might be good sites to create a formal partnership with.

## How to recreate the Referrals report in GA4

1. Navigate to Reports &gt; Acquisition &gt; Traffic Acquisition.
2. Click the pencil icon to customize the report in the top right corner

*Note: If you don’t see the pencil icon you don’t have permission to customize reports. You’ll need to ask an Admin to upgrade your access level.*

1. Click ‘Dimensions’ when the’ Customize report’ menu loads.
2. Click the three dots next to ‘Source’ and hit ‘Set as default’ and click ‘Apply’ to save the change.
3. Back in the ‘Customize report’ menu click to add a filter.
4. Select ‘Session medium’ from the drop-down and hit the ‘referral’ checkbox. Click the ‘Apply’ button to save.
5. You now have a list of all your referral traffic. Click the blue ‘Save’ button and select ‘Save as new report’. Give it a name like ‘Referral traffic’.

### Adding your new referral report to the reports menu

Your new referral report is created but it won’t show up anywhere, it’s floating in the ether for now. Let’s add it to the Acquisition section in GA4.

1. Click the library link at the bottom of the reports menu.

*Again, if you don’t see this link you don’t have the right permissions. Ask an admin for an upgrade.*

1. Find the ‘Life cycle’ collection (make sure it’s the published one) and click ‘Edit collection’.
2. Search for your referral report and drag it over to the Acquisition section.
3. Click ‘Save’ &gt; ‘Save changes to current collection’ and you’re done. Your referrals report is now available from the main Acquisition menu.