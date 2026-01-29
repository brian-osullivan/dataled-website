---
_schema: default
layout: post
title: A Guide to Creating Custom Channel Groups in GA4
category: Analytics
description: >-
  GA4 channel groupings categorize your website (or app) traffic based on its
  source (website or platform) and medium (type of marketing or communication).
author: brian
image: /images/chess-ga4-channel-groups.jpg
date: 2024-03-29T19:32:10Z
permalink:
---
Channel groupings in GA4 sort traffic by type. You don’t see individual websites or campaigns, but just the mediums they belong to. For example, the “Organic Search” channel groups organic traffic from search engines like Google, Bing, and DuckDuckGo.

If you don’t like how Google has bucketed your traffic, you can create custom groups. When I worked at a company that had a lot of organic traffic we split it into three groups: i) homepage organic traffic ii) blog organic traffic and iii) rest of site organic.

Our reasoning was the homepage organic was largely organic brand traffic. We outsourced our blog so wanted to measure that separately. Our internal SEO team was responsible for the traffic to the rest of the site. Custom groups allowed us to match our internal definitions of traffic as well as report and track them better.

In this article, I’ll take you through the default channel group and how to create your own channel groups.

First, let’s define some commonly used terms:

* **Channel group:** This is a category that combines website traffic sources with a shared “medium.” It’s essentially the type of traffic.
* **Source:** This is the specific website (or platform) that sent you traffic Examples include “google” (organic search), “facebook.com” (organic social), “buzzfeed.com” (referral).
* **Medium:** This is the type of traffic that brings users to your site. Medium and channel are often identical. But, they can be different.

## What is the difference between channel grouping and medium?

Mediums are inflexible and don’t change over time. Channel groupings are flexible and can be edited in the admin section of your account.

Medium is either set by Google automatically (organic, referral, organic social, etc) or is set by you putting UTM tracking in your URLs. Once the medium is set, it doesn’t change. Channels are set by flexible rules in the admin section that can be edited later.

## Types of GA4 Channel Groupings

GA4 offers two ways to categorize your website traffic sources:

* Default channel groups
* Custom channel groupings

### Default Channel Groups

These come pre-defined by Google and classify your traffic into familiar buckets like Organic Search, Direct, and Email. They provide a quick snapshot of your overall traffic mix.

You can find default channel groups in Reports under Acquisition, both in User acquisition and Traffic acquisition reports.

![D:\Downloads\Default groups.png](https://lh7-us.googleusercontent.com/cZdzrBYHr19Ki7gNEYwCbYJrjkwO8FUf5WcrV67UTT4ycE6Ybx08ZvFmrqAsLDs93tfScJxfTZHW1v-DNAC9qpWn-Xzue_Sln3uZClYW4CLZPjHoCueb9fXyseD8gLxGWZ4bvBGDLn_yGer-cNoOe9yTdqen2Fqn){: width="624" height="469"}

**Note:** You might notice the numbers in these reports don’t match up. That isn’t related to channel groupings. It’s got to do with how they attribute traffic. The User acquisition report shows the channel users found your site when they visited it for the first-ever time — first-click attribution. The traffic acquisition report shows the channel users visited your site from on their most recent visit — last-click attribution.

![D:\Downloads\First user primary channel group.png](https://lh7-us.googleusercontent.com/4PvoBzx7su-9GhRyRSm2ecEjUT5v2pnN0rwcrbSfSvi6FcNokEOOiiU-uJWFiUFIsqBFw3kqsJJ1N3Kb20C-WskV-ljnzvp5fkV92lZzaY6PSGfFmYf63NfeyO5GnlBuNEM3xCgX4OEQghzyLxKKawahmeyTdJ-f){: width="624" height="293"}

![D:\Downloads\Session primary channel group.png](https://lh7-us.googleusercontent.com/eQKQHd7YjyipNG0HlTbZLzBa7eXv5N9Sx6hgA_SMU_75XqEAyweWlamkq2lU_yoi5TuEiKW7InD_Isk7JkHYf7sqtZXLNIuwfPeciBgsV9CjuxrX_iu0fHDZkHqaqRADWqxU0EygdNtFRx_FQtSOQ3A7kkKopkWF){: width="624" height="135"}

*The channel grouping might look different in these reports but it’s the same. It’s the attribution method that’s different.*

In each report, you will see some common default channels:

![](https://lh7-us.googleusercontent.com/nuf4s4sujY18ivb2CoiGXV_CyhsRSsJzxUrrhQ_7bj3OV4_1HhKGZT0B0xQbgy21qJFIZi5Ih13LAAcJgl0XifL-W3WdAfo86eE0i3GIYxU9A0EOLxV18VkiucYNe4de_JRdmszNgtHPh3JA1Le1LP_z6BZvHbCD){: width="624" height="656"}

&nbsp;

* **Organic Search:** This group captures traffic originating from unpaid search engine results. The source will vary depending on the specific search engine (e.g., “google, “bing”).
* **Direct:** Traffic that arrives directly on your website by typing in the URL or using bookmarks.
* **Referral:** This group includes users who clicked on a link from another website to reach yours. The source here would be the referring website.
* **Paid Search:** This group includes traffic coming from paid advertising campaigns on search engines.
* **Organic Social:** This group captures traffic from social media platforms where users click on non-paid links to your website. The source would be the specific social media platform (e.g., “facebook.com,” “quora.com,” etc.).
* **Unassigned:** This group contains traffic where GA4 couldn’t definitively categorize the source or medium.
* **Email:** This group captures traffic originating from email marketing campaigns.
* **Display:** This group includes traffic from display advertising placements across websites and apps.
* **Organic Shopping:** This group captures traffic from organic product listings on shopping platforms like Amazon or eBay.

There are more, such as audio, SMS, etc.

### Custom Channel Groups

The default channel groups might not make sense to you or match your internal definitions of traffic. Luckily, you can modify them and create new custom channel groups.

Let’s use email as an example. A software company I worked with wanted to split their email channel in two: i) product emails sent from their app and ii) marketing emails sent from their email marketing software.

Different teams worked on both sets of emails and they had different goals so they wanted to separate them. Here’s how to do it:

**1\. Access Channel Groups:** Navigate to the Admin section of your GA4 property. Under the “Data Display” column, click on “Channel Groups.”

![D:\Downloads\Channel group.png](https://lh7-us.googleusercontent.com/Gt15v36AF1bRIbT7sWj5jrygqXZ3eZJQXDQXrK-1jXY9Ba_PzBIscO2ZMBoUFR0AMILatrvkIgXR2zTR9TCJPEEGO4KkbSaBq1w1tWpkEyakVCKoQWKoILsH2SDjVcWwItBEG2xwOoRBt4MYjX-MsWygscy6mvaD){: width="624" height="464"}

1. **Create a New Group:** You can either start from scratch or create a copy of the default group. It’s quicker and easier to copy the default group

![D:\Downloads\Create new.png](https://lh7-us.googleusercontent.com/ZMkPdFYoNN2mz4a9doiL7Wquo6lmNaX3a-fayq08l65w97RJJjxS0wxJCly69qLiqYvKXqu1TsJbSqTampqwojsQD-K9rDYeZertg1FUg3281b53d8x05yYS9XvUVRxyd0yztwxpgrNhOjF3tP7d7aJ7luJytg3y){: width="624" height="221"}

1. **Edit or Add Channels**

* You’ll see a list of existing channels within the group.
* To edit a channel, click on it and modify the conditions.
* To add a new channel, click “Add new channel” and give it a name. I’ve named my channel “Marketing Emails”).

![](https://lh7-us.googleusercontent.com/gpVFpKllgAKdTgd1tVs75QJCbxxFUHBJacvHOHTMRZysnIIaM4w0XfnHtu1oT91oOFX7FP3W320P_ns4Dv4Xf9dylvf387-aergib1Tnk1gflrCgf1idIDyMq_vBNIWbLNjdrNyu2IWlD_NH1HR7ldg){: width="624" height="256"}

1. **Define Channel Conditions**

* Click “Add condition group” to define the criteria for assigning traffic to this channel. You can combine multiple conditions using AND/OR logic.
* Select the dimensions (e.g., source, medium, campaign name) and their corresponding values to determine which traffic falls into this channel.
* Marketing emails in my example all have their medium tagged as ‘email’ and contain the term ‘mkt’ in their campaign name.

![](https://lh7-us.googleusercontent.com/X0W3BDoxZ9e_OPKLen57mBuOAEqSIr69quMLhG2iBLY4Bo99ulFIwgf3MQEOjfEtf27WS0U8mBL_xqP7hk0KbrkqcqSt2voXHEjdcuSmRkg79UhovJQw3wFIMhGpXplFq1JU8Sv-iNdUbZQXeWpTai0){: width="624" height="447"}

1. **Save and Reorder**

* Click “Save channel” after defining the conditions.
* You can reorder the channels within the group by clicking “Reorder” and dragging them to your desired position. The order determines which channel definition takes priority when classifying traffic.
* After I created another channel group for system emails I reordered my list and put both ‘Marketing Emails’ and ‘Product Emails’ above ‘Email’.
* If ‘Email’ stayed higher I would never see values for Marketing Emails and Product Emails in the reports. The more general ‘Email’ would take priority by being higher.
* I didn’t want to delete ‘Email’ in case some email traffic didn’t fit into ‘Marketing Emails’ or ‘Product Emails’.

&nbsp;

![](https://lh7-us.googleusercontent.com/8_yaaKOKipFvn22ZHgcqNEdzwhYQaT1LfpIF3zeeipgOuGUgpct3sYRrs1rHDnqKw0BVY1QsD7agKeU77O8dYuA-w5eabTabA01c9W7CeIoqQeTOYlFNd7MsJC9a1ZRh4-lciSgYMnqQaRwjqrbFCb4){: width="624" height="180"}

**Order in channels is important.** I mentioned this above but it’s worth repeating. When a user visits your website, Google tries to map the source of the visitor to a channel group in the order you have set. So, if Email is your first channel, and the user falls in the Email category, the other rules are not evaluated for that visit. Even if they fall into other categories. Whichever channel is matched first will be applied to your traffic.

&nbsp;

## How to See Custom Channel Groups in the Reports

There are two ways to see your custom channel groups in the reports.

1. Setting your default (primary) channel group

You can set your custom channel as “primary” in Channel groups. Now your reports will all default to that channel group.

![](https://lh7-us.googleusercontent.com/oH4-MX8-4AAyLMnw5B3ghBFTqPVX-QNUwnHaP3133EfevmMSxxIsQ2LJ2oVgQGjixpBnEV1G-b4aFHPXXIrBFKJRhURk14dARuXxoHsuQsYV-XUwNwtuEtYMxBfaM_u-XwGpnqaFlht6g4pK37MVVnx7wtO2PRRL){: width="624" height="189"}

1. Changing channel groups in reports

Alternatively, navigate to either User acquisition or Traffic acquisition, and add your custom channel. Click on the primary dimension drop-down:

![](https://lh7-us.googleusercontent.com/w0BEIllAYMjp543MnzMpXNJlInuu7xdZDgP5Xv5wHO2a5SRuHARSaj35Ed_OclpBSUs0Gyy4A4pb2Cz02xwz3LtOKXJ8T4fI3lmS6utb0kPFap3HxyqOHVc0971eqkakGC2AHiPCh2Jef5cImkRb4OU){: width="624" height="439"}

Select your custom channel grouping from the list:

![](https://lh7-us.googleusercontent.com/osaIefYS3ohWvG8Vg3RbcOJj0o6VgKqgFQaGz95d0nd3KsqVgINA5akhRnunhhn1eQYkvDaXwOz3WC4MFEHR6z-z6U4GA50bbsohb-9S_Z_U-DeTN4uXI4nMwIq2VlxcnFLrsLY6NAjkUchnNEiukUQ){: width="624" height="497"}

&nbsp;

## Channel Groups in GA4 - Behaviour and Limitations

Unlike a lot of other data in GA, channel groups are not permanent and they work on historic data. You can make a grouping today and it works on past data. You can edit that grouping tomorrow and it too will apply to past data.

Channel groups have some limitations:

1. Unlike Universal Analytics, you cannot use landing pages as a source in conditions in GA4. Landing page was a useful way to split up Organic traffic so it’s a loss to not have them in GA4.
2. Standard properties can only have 3 groups. The default group and a maximum of 2 more.
3. You can create only 25 channels within each group.

&nbsp;

## Conclusion

Channel groupings in GA4 help you categorize your website traffic in a way that makes the most sense to you. They’re easy to create and modify. If the default channel grouping doesn’t work for you, you can set your custom group as the default.

&nbsp;