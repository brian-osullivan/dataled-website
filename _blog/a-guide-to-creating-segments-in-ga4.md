---
_schema: default
layout: post
title: A Guide to Creating Segments in GA4
category: Analytics
description: >-
  In Google Analytics 4 (GA4), segments are subsets of your data that allow you
  to focus on specific groups of users, sessions, or events. With segments, you
  can analyze data at a deeper level.
author: brian
image: /images/segments-ga4.jpg
date: 2024-03-11T18:30:45Z
permalink:
---
Data is most useful when you learn something actionable from it. If you are trying to diagnose a drop in traffic to your site, you would drill into segments like traffic to the blog, shop, help center, etc., to see if all areas had a drop in traffic or just one.&nbsp;

Drilling into data to discover insights is something we spend a lot of time doing in GA. In Universal Analytics we used segments to help with deeper analysis. Segments still exist in GA4 but their functionality is limited versus Universal Analytics.&nbsp;

In this article, we will have a closer look at GA4 segments, their types, how they work, and how to create them.&nbsp;

First, the basics.&nbsp;

## What are segments in GA4?&nbsp;

In Google Analytics 4 (GA4), segments are subsets of your data that allow you to focus on specific groups of users, sessions, or events. With segments, you can analyze data at a deeper level and gain insights beyond the overall picture presented by the aggregate data. Examples include creating segments for users from a particular location, those who made a purchase, or those who spent a certain amount of time on your site.

There are three types of segments: user, session, and event segments. We will talk about each of them later in this article.&nbsp;

## Segments in UA vs. GA4

Segments exist in both Universal Analytics (UA) and GA. The purpose of segments in both platforms is fundamentally the same:

* **To isolate specific datasets:**&nbsp;For example, analyzing data for a specific user group (e.g., new users, mobile users, or users from a particular campaign), session (e.g., sessions with a purchase), or event (e.g., “sign up” event).
* **To compare data sets:**&nbsp;For example, comparing the total revenue earned from users in Ireland versus the revenue earned from users in England&nbsp;

### Differences between segments in GA4 vs. UA

However, there are some differences between the way segments work across both platforms. Compared to UA, segments are much more limited in GA4.&nbsp;

* **Availability:**&nbsp;Segments are readily available across all reports in UA, while in GA4, they are available only in Explore reports.&nbsp;
* **Reusability:**&nbsp;Saved segments in UA could be reused in the reports, whereas in GA4, they can only be used in the specific Explore report they are created in.
* **Creation Process:**&nbsp;In each report, UA offered a dedicated “Add Segment” section for creating and managing segments. In GA4, segments are created within the specific Explore report using prebuilt options or custom conditions.

![D:\Downloads\Segments UA.png](https://lh7-us.googleusercontent.com/DouRTmfcHyqvLPH6FfDDIHPxyBOeqhklrgXNKyJ3ScTLK8UYYaotcpPXLRKtyKp7S1HZjYOC2bPnap2TC7xNQrBS4mr51IZf_8dkhHAA0EDPM4f21_x0UR5geDJ5FUArD2vol7va9Q2gu4vjJEaEFLoRcjwXmqax){: width="624" height="252"}

## Creating Segments in GA4

Segments are created in the ‘Explore’ reports in GA4. You can find ‘Explore’ in the left panel of your GA4 dashboard.&nbsp;

![](https://lh7-us.googleusercontent.com/fovsvF10tRGRNk9rE-BHm7uXdP7xsRX0rzE4KRS06HFsMtzpgSzGk6ySvdpUWMSUsVvIQ2TuFfG8yqJW_5aV2qw0TWWmtiumuhk-VJuuW5zvaQWZYtXqUIpxmu4Mb8cbY4lhUMl23OWObRweNzVaDX3IvJoqfoJm){: width="165" height="547"}

<br>

Select any exploration report type to get started (I’m using Free form). Segments are in the Variables section. Select a timeframe and click on **\+** to start creating one.

![D:\Downloads\segments 1.png](https://lh7-us.googleusercontent.com/lCwJIG7PDPr9D9yb-VE75_PscJIHwKrj4EOe-tT-YZIRhVsMbgromRroQzSV3d1Bt5fmqw6csHnUd0f2uhlejHcdZkCQnEpnWdPDzrPfNFq1RlxX1rQDHdNZZbj7WULEwHIYF7LbG_qro5Zb4c66HQZY7w_jvj21){: width="624" height="363"}

You can **create a custom segment** or choose from the prebuilt segments, which you can find under **Use a reference**.&nbsp;

![D:\Downloads\custom segments.png](https://lh7-us.googleusercontent.com/wKlrV5IUkdAIKNxi37J0QZVBWntbkc_0mmzDhUSsN1ss5CqWnOzcxGf3fEa8S-6REpipIujBIrp7QLUHw_aJUT8bU9fK5fTnZBxZg-yG2hL3t1qazu5a1f65jcKpmmRuPK5EBj9st6SUFtQSMsrvZ-CgkFAxFVto){: width="624" height="339"}

First, let’s explore prebuilt segments.&nbsp;

### Creating Prebuilt Segments in GA4

There are three tabs in prebuilt segments: General, Templates, and Predictive.&nbsp;

In the **General** tab, some commonly used segments are given, such as purchasers, active users, etc. For example, if you are interested only in purchasers, click on **Purchasers**. The segment builder for purchasers will appear, with some fields pre-filled.&nbsp;

![](https://lh7-us.googleusercontent.com/Ae6KbVvNrkYEYOQj2WWCoDIQmto46dJCGyF4uy_aEowdERyNXQf32mSq-SSrz-RK836XImIsksaczl_vlRUOhYLaJG645UCcZ--WGPNRkfpsfb-Q9BvS6qPgEfO9PjxOzxOmmvcDYR30krlxfZSLVwDWY5Bbz9m0){: width="624" height="290"}

Similarly, if you want to know about your active users, click on **Recently active users**. Add a parameter to see how many users your segment matches in the **Summary** panel on the right.&nbsp;

![](https://lh7-us.googleusercontent.com/QiDIiduMpGMhvkmHMX32eN9XWvY0vucsDiBzCOuyLrCGrIFe0_uWmuN2KqQ4dTIkGqqtFvGK7pmdWLaMVs3JDiuyFUq8uRmpSVknuNQYtVaEC8b-ro5PvGOxSQ8mVMFbDdpivM7SH8yTryzR6w_VESm2i79w3E0Y){: width="624" height="287"}

Next is the **Templates** tab.&nbsp;

![](https://lh7-us.googleusercontent.com/vgiZCpf5dvy4GtHB6HG9LFHW6HKLnnl6N40Y85cQBSKazvqXxbIw6WxWgQdaYThMIeobN64y1Lj0s-AKGtllq0BxbIMaBilHcUExjjscXez2CJcE1HW5AbZ7s-KNZjvoq0MojtPOXdp8z2GquEKBvDq6vf26Be9z){: width="624" height="164"}

Here, you can segment your users based on demographics, technology, and acquisition channels. It also contains prebuilt segments relevant to the vertical you selected when you created your GA4 property.&nbsp;&nbsp;

Finally, in the **Predictive** tab, you can see prebuilt segments of users who are likely to convert—or churn. Most of these segments are aimed at sites that sell something. Even if you are an e-commerce site, they have prerequisites—a minimum number of 1,000 users must have triggered the condition in the previous 28 days. Since my website doesn’t allow users to purchase anything, I am not eligible to use this feature. <br>![](https://lh7-us.googleusercontent.com/eCYjZO_ydjput80wbNDFX8NM34rnH7E4d1pFIPJ2mVd7Hp-4MUWMtXwwJC_-Vg84OlRAgf0X8fHmUAPxGeITZyDxe61DBNFJceaNnHJd4EGiD5JVZHXmSCEKZAb3kjt9BaW_ij8mhc_g0J160JHDvDil_2KYxOR-){: width="624" height="319"}

Read more about the [<u>eligibility criteria for predictive metrics</u>](https://support.google.com/analytics/answer/9846734).&nbsp;

### Creating Custom Segments in GA4

Custom segments are found above pre-built segments.&nbsp;

![D:\Downloads\custom segments.png](https://lh7-us.googleusercontent.com/wKlrV5IUkdAIKNxi37J0QZVBWntbkc_0mmzDhUSsN1ss5CqWnOzcxGf3fEa8S-6REpipIujBIrp7QLUHw_aJUT8bU9fK5fTnZBxZg-yG2hL3t1qazu5a1f65jcKpmmRuPK5EBj9st6SUFtQSMsrvZ-CgkFAxFVto){: width="624" height="339"}

First, select the segment scope. Scope is the level of data you want to filter in a segment. In GA4, you can create custom segments for three types of scope: user, session, and event.&nbsp;

* **User segment:**&nbsp;Includes all events associated with users who meet specific criteria (e.g., users who purchased in the last 30 days).
* **Session segment:**&nbsp;Includes all events associated with sessions that match the set criteria (e.g., sessions with a specific source/medium).
* **Event segment:**&nbsp;Includes only specific events that meet your criteria (e.g., “add\_to\_cart” events).&nbsp;

Let’s create a **User segment.** After clicking on the **scope,** the segment builder window will appear.&nbsp;

![D:\Downloads\segment builder.png](https://lh7-us.googleusercontent.com/tozIe6tyvCFiioeWmcSFeaTqUf_KfEkcln5Sot8lG2vv0IPb_kK2rvKg-sXv8F1Knsrijw5GdbwQg9bkPp01A2AKxzIZ-xMhMMKEJqSLv_pyL7QJgTa1BLYRKD-Squ7EpN6a5ydRThz1nrMo4DTMigznl_j0oEoJ){: width="624" height="296"}

1. **Name your segment.** Give it a name that is easy to identify. I’m using “US users.”&nbsp;
2. **Define your segment criteria**. Include users (or sessions or events in case of session and event segments, respectively) when certain criteria are met.&nbsp;
3. **Add new condition:** Click on “Add new condition” to specify the criteria for your segment. &nbsp;**&nbsp;**&nbsp;First, select the Event or Dimension you will use to define your segment, I’m using the Country dimension. ** ** &nbsp;Next click “**\+ Add filter”** to narrow down your event — I entered the United States here.&nbsp;**&nbsp;**&nbsp;

![](https://lh7-us.googleusercontent.com/BrtpGnXu-u_L9XTZTJzvxCSKu-fj0F7uSZHZSGk34xeGWm6rSMxfE5MaZvv1C0mpcLd4qpyx_LO4SL7piJDQ2vXXh8zi2zQl6MPpb2Olm01OzJyXsCFenaHtpw0QfSur6rlgSAHHdmPI7eqoRuIarHQ1eGvsoQ12){: width="462" height="410"}

![](https://lh7-us.googleusercontent.com/tNiYRQIEFLwBUF6zuCNCKynLAt4eMIPtU_Nk_rEhvgbqPgqR-HV8LW-jjpNG-NBFIAdkCYqg0k-yxPDZuUCFi7DbE9g20gHyjx0s26T5xtzCcEFxSXqQAYIKnTnhSxUB9s5AjwIFVFwXqW1SMkyf7rJEjh3j72Ub){: width="624" height="284"}

Depending upon your dimension, you can select a comparison operator (e.g., equals, greater than) and enter the desired value.&nbsp;

1. **AND/OR:** You can add multiple conditions using AND/OR logic to create more complex segments. For example, for “Users from the US who have purchased,” you will add country AND *purchase* from the list of events and dimensions.&nbsp;
2. **Conditon’s scope:** The user icon beside the delete button is called a condition’s scope, and it determines how broadly or narrowly the conditions are applied.

![](https://lh7-us.googleusercontent.com/uyYgHLHpu0PFFchxWwPaYtrpe7Dutqf8nHMlDU3mU7Yv2N8o95AkBXozFky6We7ublv5kR6B9Rm1KDZ_7_jU5RH1gUZu8p14E0YeEJ1er08rdf3QZ_FsLqrzJCjtt1jtt8c6zM_lN8rOp-oMv_8Pj0M4vI5bYOrh){: width="306" height="214"}

For user segments, you can select:

* **Across all sessions:** conditions must be met during the lifetime of the user. For example, if you have added two conditions (*begin\_checkout*, *purchase*), then both events can have happened at any time, irrespective of whether the conditions were met in the same session or not.&nbsp;
* **Within the same session:** all conditions must be met within the same session. Only those users that had the *begin\_checkout* and *purchase* event in the same session would be in the segment.&nbsp;
* **Within the same event:** all conditions must be met within the same event. Because you are limited to one event with this scope you can’t combine multiple events, only events and parameters. For example, you could specify to isolate users that have the *begin\_checkout* event and are from *France*.&nbsp;

For session segments, there are two scopes: ‘**Within the same event’** and ‘**Within the same session’.** For event segments, there is one scope: ‘**Within the same event’**.&nbsp;

1. **Adding a sequence:** You can add a sequence to your segments here. We will talk more about this later.&nbsp;
2. **Adding exclusions:** You can further refine your segment by excluding irrelevant data. This can be helpful when you want to focus on a specific subset within a broader segment. For example, you might create a segment for “All users who purchased” and then exclude “users who purchased a specific product on sale” or “all users who purchased” and then exclude “purchasers from a specific location” to analyze regular purchase behavior.
3. **Summary:** The summary panel shows you how many users match your segment.
4. **Build an audience:** Based on the segment you created, you can build an audience that you can use later in GA4 or your Google Ads campaigns. &nbsp;**&nbsp;**&nbsp;
5. **Save and apply.** The segment is now ready to be used.&nbsp;

Once the segment is saved, it will move to the **Segments** section in the report, found under **Variables.**&nbsp;

![D:\Downloads\segment comparison.png](https://lh7-us.googleusercontent.com/YlPvxO9VS00Qr5txy8AA7wtDiioEfXtC0AX3qSvWUe6RGUTGipo-nquluR_aHtSGUnMdvK6RQ-ibYSWOMII8sofmw5WlXEFfka8Nnc1dN7ZITaM_AMjPeCrv8JcmhQXU_FZhbyE7eWng6CeUbcy_KjJJQdACYYR6){: width="624" height="347"}

I made 2 segments, one for users from the UK and another for users from the US. Drag segments to the **Segment Comparison** tab and the result can be seen in the table on the right.&nbsp;

## Adding a Sequence

If you want to analyze your user’s journey, you can create a sequence in segments. Sequences show the path that a user takes in the course of an action. For example, you can define a sequence of events (e.g., view product page, add to cart, purchase) and identify users who completed this specific sequence of events within a session.&nbsp;

&nbsp;

## An alternative&nbsp; to Segments in GA4: Comparisons

While segments in GA4 allow you to isolate and compare data, they are limited. You can only access them in the Explore reports and can’t reuse them.

This is where GA4 Comparisons step in as an alternative approach for analyzing and comparing different subsets of your website or app’s data directly within reports.

![](https://lh7-us.googleusercontent.com/0DfNDbXXxxAkwKtBvY1Ic6hKWmJR9T7L2hMaRRkQm19laIqauEUq9qkCiu0DSm1HaCOGBQz4X7TABSUrmYrnhPCppYRgbCacKIlmDCwU9RlXFC-QD1zI4FJyoBk3on7jhmdCGFo2Sdf1gwn1tvLxbrlHxuOLLn2i){: width="624" height="232"}

#### *Functionality*

GA4 Comparisons allow you to compare data for different segments&nbsp;**within the same report**. This means you can view side-by-side comparisons of key metrics (e.g., sessions, conversions, revenue) for different user groups, sessions, or events.

#### *Benefits*

Like segments, comparisons allow you to drill into a subset of data or compare two subsets.&nbsp;

Unlike segments, comparisons can be added to standard reports. They can’t be saved but you can reuse them across multiple reports until you exit the segment.&nbsp;

### How Do GA4 Comparisons Work?

1. **Access:**&nbsp;Within most standard GA4 reports, you’ll find the “Edit comparison” option at the top of the report. When you click on the icon below, the comparisons window will open, allowing you to add up to 4 comparisons.&nbsp;

![D:\Downloads\comparison.png](https://lh7-us.googleusercontent.com/9eAqSqiPYeTm9GnNGE2mbPYHi5jU0XkOzQbpPc2wtyJ0G161nL7C0ZyIk-wNJO-PnGtq27GI9CzcJgr7ctXfR2VHF9he79xBExOObhjMQZSgPjcKiDGB6AjFPaLRdrFhnrDnwayHVkE14Hxj47vh8JXfTlDMv7Lm){: width="538" height="231"}

1. **Selection:**&nbsp;Choose the data set you want to compare. I am comparing users from the US versus Canada and the UK visiting one of my websites in the last 28 days.&nbsp;

![](https://lh7-us.googleusercontent.com/I4hPo9VsRXlliQKQsM2HpP0SMp7Ol6D5GZtN3Cy9GKwGbRCjBeWfEKvA5rDAsoyKsbQhPRwmUJ8nqBp1o3M3nGLFE2l8A6nXCgpxeNQ03cJppkeLzGJaQHxUEAg6dAmkaJY9s4zE-godTAmEhW7Cvs0){: width="624" height="232"}

1. **Analysis:**&nbsp;The report will display your chosen data set alongside the original data.&nbsp;

## Segments in GA4: A Recap

Segments help users isolate, compare, and analyze data at a deeper level. Found in the Explore reports, segments offer website (or app) owners to:&nbsp;

* **Isolate specific data sets:**&nbsp;Focus on user groups, sessions, or events that meet defined criteria.
* **Compare data sets:**&nbsp;Visually compare key metrics for different parameters or events.

However, there are a few limitations of segments. You can create them only in the Explore report, and you cannot reuse them. Additionally, you can create only up to 10 segments per exploration. Plus, not more than four segments can be applied to an individual exploration technique at one time.

A better alternative in these cases would be using comparisons, which offer a lot of the same functionality but are available in the standard reports.

&nbsp;