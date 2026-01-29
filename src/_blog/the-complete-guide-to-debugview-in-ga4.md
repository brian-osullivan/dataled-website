---
_schema: default
layout: post
title: The Complete Guide to DebugView in GA4
category: Analytics
description: >-
  DebugView is a feature within Google Analytics 4 (GA4) that allows you to
  monitor events and user properties in real-time as they’re collected from your
  website or app.
author: brian
image: /images/ga4-debug.jpg
date: 2024-03-13T11:31:19Z
permalink:
---
It takes time for data to show in your Google Analytics 4 (GA4) account — anywhere from 24-48 hours. When you set up GA4 or add a new event you’d like to verify it’s working correctly without waiting.

You can do this through **DebugView**, a built-in feature within GA4. We’ll discuss how in this article.&nbsp;&nbsp;

Specifically, we will talk about:&nbsp;

* What is DebugView?
* How to activate DebugView?
* How to understand the UI of the DebugView?
* Common issues with DebugView
* Any suitable alternatives?

## What is GA4 DebugView?

DebugView is a feature within Google Analytics 4 (GA4) that allows you to monitor events and user properties in real-time as they’re collected from your website or app.

You can get information about user interactions on your website, such as button clicks, page views, and purchases.&nbsp;

This real-time visibility helps you:

* Identify and fix tracking errors—quickly see if events are being captured correctly or if there are any missing data points.
* Verify data accuracy—ensure the information collected, like product details and prices, matches what’s on the website.&nbsp;
* Troubleshoot issues—gain insights into potential problems with your tags or tracking implementation, and consequently diagnose them efficiently.

You must enable debug mode to turn on and use DebugView.&nbsp;

## How to turn on DebugView?

To access DebugView, navigate to the **Admin** section within your GA4 property. Under the **Data display** column, scroll down to **DebugView** and click on it.&nbsp;

![D:\Downloads\debugview access g14.png](https://lh7-us.googleusercontent.com/rH64zvNaUVA8SVg5jGxo0F3VUj3Q2o6RVVWYdK-T1Qt3DN_mYZBhDCLFDpJIaSTUvOzTGjtKXYBQ363tGXLLQxozQhomeFutMIoVtvE48n6VZYOV_tc_7TQJp2eKWlz_gSF8zA90UOedgYqZ6yXVN0QBkj4azHqa)

If there is no data like in the below screenshot, it means debug mode is not enabled.&nbsp;

![](https://lh7-us.googleusercontent.com/N4JQ9na4ecO7lkxVohE_dKZ7kIaKSJlFiYIT8jWxKQTpl_FkBRlLS-ttylXitBErZmeN7aRDqMwWXKj9w03tttKPLDJskgWH2Fbi0ijAUGmbmkiDXP8H4cKC8VjBI96-9c-c-PXZopK4aRBbbdFLg0uYgfuyCr4N)

There are several methods to activate debug mode:

* Tag Assistant
* GTM Preview Mode
* Third-Party Platforms

**1\. Tag Assistant**

Visit [<u>https://tagassistant.google.com/</u>](https://tagassistant.google.com/) and follow the on-screen instructions to enable debug mode for your device. This is the easiest method—add your domain and click **Connect**, and a window will appear.&nbsp;

Now, go back to DebugView, and you will see data flowing.&nbsp;

![](https://lh7-us.googleusercontent.com/bR1gUFtsZUiy7BFFz02uYAfsaeeDzmk9ckpGzMHs2ViZUdM52cDdi11ny9fJ26LuHmsefpsr6WDXzDt1x8kBQiGvYOQdm92Qq9hLy6d4IghZpK2vHehOs8pG3PPjhSh9gyNARPpk9NfpDrdISysEC543T85eQYpF)

**2\. GTM Preview Mode**

Another method is to use Google Tag Manager (GTM). Go to [<u>https://tagmanager.google.com</u>](https://tagmanager.google.com), and you will see **Preview** just beside **Submit.** Click on **Preview and follow the instructions.** After the domain is connected, a window will appear confirming it’s working.

![](https://lh7-us.googleusercontent.com/NbFTw4fdX16URM2VgHDVy0IT0DXHck0nOhjBTZ6AbY_VRfZMrQmIfGqiZg9Te0HggpekLTHpDUHN26Mc4cPlE8Kl6LxrfqXkzUCjtvvYLOxyFVFOfeYCFYgvvaEzQ28lNrr3w48-F6LzszyiEPL2mstlRRPiK3rx)

Some sites struggle with arbitrary parameters added to the URL. If you cannot see any activity in the DebugView, you can try unchecking ‘*Include debug signal in the URL.’*&nbsp;&nbsp;

![D:\Downloads\ga4 gtm.png](https://lh7-us.googleusercontent.com/jqu9i0xuvf9E0gtCVKc77u9O-LWqveQLN4VhmzzOpEdLAKdUNGIIkOh98b9tZTUzBZFPXahObIDjB530AM75oQy5LNP_gYXp0gtWuK4lxiFOu7AAfEVafsQLQxDGzEJT3r214yFCn9mijWV5CI4xnVhct9a0hrk-)

**3\. Third-Party Platforms**

There are lots of **GA4 Debugger** extensions that you can download from the Chrome Web Store: [https://chromewebstore.google.com/search/ga4%20debug]()

Similarly, for Firebase projects, you can use the **Firebase Developer Tools** extension. Navigate to the **Analytics** tab and enable debug mode for your project.

## Understanding the DebugView Interface

The DebugView interface comprises of the following 5 elements:

* Device Selector
* Minutes stream
* Seconds stream
* Top Events
* User Properties

![D:\Downloads\GA4 UI.png](https://lh7-us.googleusercontent.com/8xcE0qJjCnkCsgfqpMagUsDEMnfZfiQOimpeG36gCmHhUnssxYu5k-JPNxK6izSg-d7sjr189lL2ELWDSqh0GqCHSNLqmQ8T3EKNW1PrDmCQZd0OC292yru-BxnqDQM5dJFxdgtjT-JYbT9ZysOAKXFfz1A14EyT)

**1\. Device selector**

This dropdown menu allows you to switch between different devices that have triggered debug mode. This is only relevant if you’re testing across multiple devices.

**2\. Minutes stream**

This section is a historical record, showcasing event data archived in 5-minute intervals for the past 30 minutes. Each circle shows the activity recorded in a minute, while the number inside the circle shows the count of events in that minute. For example, in the 8:41 minute, 4 events took place above.&nbsp;

If you click on any circle, it will populate the details of events in the Second stream.&nbsp;

**3\. Seconds stream**

This column acts as a live feed where actual debugging happens. The Seconds stream displays events logged within the past 60 seconds, allowing you to analyze events at a more granular level. It shows events happening in real-time and will allow you to debug.

If you click on any event, it will show the Parameters and User properties tabs. Under the Parameters tab, you will see a granular view of the parameters captured with that event (page\_view in the example below). Under the User properties, you will see any user attributes being sent with the event.

![D:\Downloads\events details ga4.png](https://lh7-us.googleusercontent.com/rIsTEHDAaEgM-43JLFNkjYdemdzUakGGjYs4glOllaI9eLy9yByB3ApcG9d7g8X_Y1QQqGYtustmBa9Zc2EKFM8B3zN_N_JEnqf8WgbAJ1eEZTe2LeUAn1u0dogUNZQsTKs_5WCoCpv9r-zMYmLRritz1p-vvKGg)

You’ll see different types of parameters:

* Some that don’t get shown in the UI (batch\_page\_id/batch\_ordering\_id: group and sort events sent from the page)
* Automatically collected parameters that do get shown in the UI (page\_title: the title of the page)
* Custom parameters that you’ve set yourself (none in this screenshot!)

The number appearing against each parameter shows the number of values for that parameter — all of the parameters in the above screenshot have just 1 value.

If you click the chevron you can see the values for the parameter.

![](https://lh7-us.googleusercontent.com/GggLGAbSXdI70sbayV56DkJTvExdC-pLSlgP0NzdIcCfoczJl80ffz5TIwrrYEOdeeg1rBwp8PnNf3O2RLSG0_D68aNLOsWu2FGubWI_YAkJqoY52FT9iUb1zLTMpO42r1w3VDkzv2mNNf1gMQiK5Fg)

**4\. Top Events**

This panel displays the most frequently logged events within the past 30 minutes. If you click on any event it will show all of the parameters and user properties grouped by that event in the seconds stream.&nbsp;

![](https://lh7-us.googleusercontent.com/bh_0LIPH3AHvd8OjqD4gUbcuvD8qbYaACvSVAuy27M3Eq67-gxXgducyPBGceGrK8P-vvUIZnQcKfCONJPMuGjxFHUhDCoI2OAZuO9-GwZxOKpgzSXTWdcG0wPbFqHc_sEALz0jKilqOg_gIPfKybqM)

**5\. User Properties active now**

The title is self-explanatory, this shows all of the active user properties. User properties are attributes that describe a user, like user\_id. Like parameters, they can be collected automatically or be custom-set by you.

## Known Issues with DebugView

While DebugView is a valuable tool, it has some limitations:

**1\. It can lag**&nbsp;

If DebugView appears sluggish or unresponsive, clear your browser history or use an incognito window. This can often resolve temporary glitches. Note, however, that sometimes, even clearing the cache or using an incognito window won’t work for delays. All you can do is wait for some time and try again in a few minutes.&nbsp;

**2\. Missing custom item parameters**

Custom item parameters are e-commerce-specific parameters that allow you to add more details about products. For example, you might add a custom item parameter to mark products as in or out of stock. Custom item parameters do not display within DebugView — it’s a long-standing bug.

**3\. Number display bug**

Numbers can get displayed incorrectly. You might see prices appear 10^6 larger. So, 48.72 becomes “48720000”. This is just a visual bug; the data is still collected accurately. The larger number is how prices are stored in the Google backend.

&nbsp;Similarly, in the Device selector portion, you may see 0 written against ‘Debug device’ even though you will find your device in the dropdown. This is also a visual bug and doesn’t indicate any problem in your tags or tracking.&nbsp;

## Alternatives to DebugView

If you’re finding DebugView too laggy or buggy, try these alternatives:

**1\. GTM Preview Mode**

You should be able to do most of your testing using GTM. I do the majority of my debugging in GTM and only use DebugView occasionally to see if data is showing up in GA4.

![D:\Downloads\GTM preview.png](https://lh7-us.googleusercontent.com/tFt0dGr-OeErXeVrgelAKhCG3wnle-Ywdv31bqU601qbH1ffhs4syhrWYt9dZkdNBfVUFNfI5FZrA5RMTuIhe9nL5RjI1jQR5ZvbalXvW9a1P9zxhtb7CH8s4wZU5fPqjidOfmuuLpHA2HrTWM69qEA1cOafcEMj)

**2\. Developer Console**

The browser developer console is a great way to debug your installation. Other tools use the same data but wrap it in a nicer UI — sometimes it’s better to go straight to the source!&nbsp;

Open the [<u>Developers tools on Chrome</u>](https://support.google.com/campaignmanager/answer/2828688) by right-clicking and hitting ‘Inspect’. Navigate to the ‘Network Tab.’ Search ‘Collect’ and refresh your page. In the ‘Payload’ tab, you will see the data that your browser is actually sending to Google.&nbsp;

![D:\Downloads\developer tools.png](https://lh7-us.googleusercontent.com/YOEYSKBz9RggRz3AYZnwEpCV3JqLFCXadg6QUk6kTTvn7lLf58gBNwSDO4OZp4c_mkZ87bD_aJcmDHmAl71QoUui0ctIk81AXcp0KqoTT-4lePE8i42qNl-7MbeZC-VMcaa5qiDQldYcpFW--kNx94p81Y5PAsx1)

## DebugView in GA4: Wrapping it up

DebugView in GA4&nbsp; helps you see if your tags and tracking are working correctly. It’s not perfect but it’s a useful tool to help you troubleshoot your setup.

If you’re finding it laggy or buggy you can use GTM or the developer console instead.

&nbsp;