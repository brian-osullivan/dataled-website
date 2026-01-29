---
_schema: default
layout: post
title: All GA4 limits 2026
category: Analytics
description:
author: brian
image: marketing.jpg
date: 2026-01-15T17:50:37Z
permalink:
---
## **ACCOUNT & PROPERTY STRUCTURE LIMITS**

**Accounts & Properties**

* Maximum 100 Google Analytics accounts per user
* Maximum 2,000 properties per account
* Maximum 50 data streams per property (max 30 app data streams)

**Sources:** [Google Analytics hierarchy](https://support.google.com/analytics/answer/9303323?hl=en)

---

## **EVENT COLLECTION LIMITS**

**Standard GA4:**

* Unlimited distinctly named events for web streams
* 500 distinctly named events per app user (app streams)
* 2,000 distinct sessions per user per day
* 10,000 conversions per user per day
* 100,000 events per user per day
* Event name length: 40 characters
* Event parameters per event: 25
* Item-scoped parameters per event: 27 custom (in addition to prescribed parameters)
* Event parameter name length: 40 characters
* Event parameter value length: 100 characters (exceptions: page\_title 300, page\_referrer 420, page\_location 1,000)
* User properties: 25 per property
* User property name length: 24 characters
* User property value length: 36 characters
* User-ID value length: 256 characters

**GA4 360:**

* 2,000 distinctly named events per app user
* Event parameters per event: 100
* User properties: 100 per property
* Event parameter value length: 500 characters (except page\_location: 1,000)

**Sources:** [Event collection limits](https://support.google.com/analytics/answer/9267744?hl=en), [GA4 360 limits](https://support.google.com/analytics/answer/11202874?hl=en)

---

## **CONFIGURATION LIMITS**

**Standard GA4:**

* Audiences: 100
* Saved comparisons: 50
* Saved segments: 50
* Key events (conversions): 30
* Custom insights: 50
* User-scoped custom dimensions: 25
* Event-scoped custom dimensions: 50
* Item-scoped custom dimensions: 10
* Event-scoped custom metrics: 50
* Explorations: 200 created per user, 500 shared per property
* Ads links: 400
* Calculated metrics: 5

**GA4 360:**

* Audiences: 400
* Saved comparisons: 200
* Saved segments: 200
* Key events: 50
* User-scoped custom dimensions: 25 (same as standard)
* Event-scoped custom dimensions: 125
* Item-scoped custom dimensions: 25
* Event-scoped custom metrics: 125
* Explorations: 200 created per user, 1,000 shared per property
* Calculated metrics: 50

**Sources:** [Configuration limits](https://support.google.com/analytics/answer/12229528?hl=en), [GA4 360 limits](https://support.google.com/analytics/answer/11202874?hl=en)

---

## **DATA RETENTION & EXPORT LIMITS**

**Standard GA4:**

* Data retention: Up to 14 months (options: 2 or 14 months)
* Data export: 100,000 rows for reports and explorations; 10M cells for unsampled explorations
* BigQuery export (daily): 1 million events
* BigQuery export (streaming): unlimited
* Data import manual uploads: 120 uploads per day per property
* Data import storage limit: 10 GB per property

**GA4 360:**

* Data retention: Up to 50 months (options: 2, 14, 26, 38, 50 months)
* BigQuery export (daily): Billions of events
* Data import storage limit: 1 TB per property

**Sources:** [Configuration limits](https://support.google.com/analytics/answer/12229528?hl=en), [GA4 360 limits](https://support.google.com/analytics/answer/11202874?hl=en)

---

## **SAMPLING & REPORTING LIMITS**

**Standard GA4:**

* Explore sampling limit: 10 million events per query
* Ad-hoc query limit: 10 million events per query (beyond this = sampling)
* Standard reports row limit: ~2 million rows
* Explore reports row limit: ~2 million rows
* High-cardinality threshold: &gt;500 unique values per dimension per day

**GA4 360:**

* Explore sampling limit: 1 billion events per query
* Unsampled explorations: 20,000 daily tokens, 5,000 tokens max per query
* Automatic expanded datasets with 2 million row limit

**Workarounds:**

* Export to BigQuery for unsampled data
* Reduce date ranges
* Use fewer segments and lower-cardinality dimensions
* Limit high-cardinality dimensions in reports

**Sources:** [Mauro Romanella](https://www.mauroromanella.com/ga4-data-quality-sampling-thresholding-and-cardinality-explained/), [InfoTrust](https://infotrust.com/articles/google-analytics-4-reports-sampling-cardinality-thresholding/), [In Marketing We Trust](https://inmarketingwetrust.com.au/data-sampling-in-google-analytics-4/)

---

## **API LIMITS & QUOTAS**

**Standard GA4 (updated limits as of late 2023):**

* Tokens per property per day: 200,000
* Tokens per property per hour: 40,000
* Tokens per project per property per hour: 10,000
* Concurrent requests per property: 10
* Potentially thresholded requests per hour: 120
* Most requests consume &lt;10 tokens

**GA4 360:**

* Tokens per property per day: 2 million
* Other quotas significantly higher

**Previous/Legacy Limits (enforced Nov 2022):**

* Tokens per property per day: 25,000
* Tokens per property per hour: 5,000
* Tokens per project per property per hour: 1,250
* Concurrent requests per property: 10

**General API Limits:**

* 50,000 requests per project per day
* 10 queries per second per IP address

**Workarounds:**

* Use BigQuery connector instead of native GA4 connector
* Use Extract Data connector (limited to 100MB)
* Use third-party connectors (Supermetrics, Whatagraph, etc.)
* Share reports with fewer people
* Reduce number of charts/widgets per page
* Set data source refresh to maximum 12 hours

**Sources:** [Google Developers - Data API limits](https://developers.google.com/analytics/devguides/reporting/data/v1/quotas), [Supermetrics](https://supermetrics.com/blog/google-analytics-4-api-quota), [Data Bloo](https://www.databloo.com/blog/ga4-quota-limits/), [EasyInsights](https://easyinsights.ai/blog/how-to-overcome-the-limitations-of-the-google-analytics-4-api-quotas-with-easyinsights/)

---

## **DATA THRESHOLDING**

**When Applied:**

* Reports using Google Signals data
* Demographic dimensions (age, gender)
* Interest category dimensions
* When user count falls below threshold (~30-50 users/events)

**Workarounds:**

* Increase reporting period
* Turn off Google Signals in reporting settings
* Use device-based reporting identity instead of blended/observed
* Export to BigQuery

**Sources:** [Mauro Romanella](https://www.mauroromanella.com/ga4-data-quality-sampling-thresholding-and-cardinality-explained/), [In Marketing We Trust](https://inmarketingwetrust.com.au/data-sampling-in-google-analytics-4/)

---

## **CARDINALITY ("OTHER" ROW)**

**Limits:**

* High-cardinality dimensions: &gt;500 unique values per day
* Standard reports row limit: ~2 million rows
* When limit exceeded, excess data grouped into "(other)" row

**Workarounds:**

* Use Explorations instead of standard reports (not subject to "other" row)
* Limit collection of high-cardinality values
* Export to BigQuery
* Upgrade to GA4 360 (automatic expanded datasets)

**Sources:** [Mauro Romanella](https://www.mauroromanella.com/ga4-data-quality-sampling-thresholding-and-cardinality-explained/), [InfoTrust](https://infotrust.com/articles/google-analytics-4-reports-sampling-cardinality-thresholding/)

---

## **GOOGLE ADS & INTEGRATION LIMITS**

**Standard GA4:**

* Google Ads Manager audience lists: 100
* Display & Video 360 audience lists: 100
* Search Ads 360 audience lists: 100

**GA4 360:**

* Google Ads Manager audience lists: 400
* Display & Video 360 audience lists: 400
* Search Ads 360 audience lists: 400

**Source:** [Cardinal Path](https://www.cardinalpath.com/blog/key-differences-between-the-360-and-free-versions-of-ga4)

---

## **KEY LIMITATIONS TO NOTE**

1. **No scheduled email reports** (must use BigQuery/Looker Studio)
2. **No session-scoped custom dimensions** (only event and user scopes)
3. **No product-scoped dimensions** (only user, event, item scopes)
4. **Limited GDPR compliance** in some EU countries
5. **No offline conversion tracking** natively
6. **Cannot grant access to individual data streams** (only property level)
7. **Subproperties and roll-up properties** only available in GA4 360

**Sources:** [Factors.ai](https://www.factors.ai/blog/a-non-exhaustive-list-of-limitations-with-ga4-2022), [Ruler Analytics](https://www.ruleranalytics.com/blog/analytics/limitations-google-analytics/), [RudderStack](https://www.rudderstack.com/learn/GA4/benefits-and-limitations-of-google-analytics-4-ga4/)

---

## **UNIVERSAL WORKAROUND: BIGQUERY INTEGRATION**

BigQuery integration solves most GA4 limitations:

* ✅ Bypasses sampling limits
* ✅ Eliminates cardinality limits
* ✅ No data thresholding
* ✅ Access to raw, unsampled data
* ✅ Custom queries for complex analysis
* ✅ Long-term data storage beyond 14/50 months

**Note:** Free BigQuery tier includes 10GB storage and 1TB query processing per month.