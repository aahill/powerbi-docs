<properties
   pageTitle="Share reports with coworkers"
   description="Learn how to share Power BI reports, and filtered reports, with coworkers in your organization."
   services="powerbi"
   documentationCenter=""
   authors="maggiesMSFT"
   manager="erikre"
   backup="ajayan"
   editor=""
   tags=""
   featuredVideoId="0tUwn8DHo3s"
   qualityFocus="complete"
   qualityDate="06/22/2016"/>

<tags
   ms.service="powerbi"
   ms.devlang="NA"
   ms.topic="article"
   ms.tgt_pltfrm="NA"
   ms.workload="powerbi"
   ms.date="08/31/2017"
   ms.author="maggies"/>

# Share reports with coworkers

*Sharing* is a good way to give a few people access to your dashboards and reports. Power BI offers [several ways to collaborate and distribute your reports](powerbi-service-how-should-i-share-my-dashboard.md), and sharing is just one.

With sharing, you and your recipients need a [Power BI Pro license](powerbi-free-vs-pro.md). Suggestions? The Power BI team is always interested in your feedback, so go to the [Power BI Community site](https://community.powerbi.com/).

You can share a report with coworkers in the same email domain as you, from your own My Workspace or from an app workspace. When you share a report, those you share it with can view it and interact with it, but can't edit it. They see the same data that you see in the report, unless [row-level security (RLS)](powerbi-admin-rls.md) is applied. 

## Share a Power BI report

1. [Share a dashboard](powerbi-service-share-unshare-dashboard.md) with tiles that link to the report you want to share. 

    Even if you only want to share the report, you need to share a dashboard that links to the report first. The people you share the dashboard with now have permission to see the underlying report. You don't need to send them mail when you share the dashboard.

2. Copy the report page URL and send it to your coworkers. 

    When they select the link, Power BI opens a read-only version of the report.

## Share a filtered version of a report
What if you want to share a filtered version of a report? Maybe a report that only shows data for a specific city or salesperson or year. You do this by creating a custom URL.

1.   Open the report in [Editing view](powerbi-service-go-from-reading-view-to-editing-view.md), apply the filter, and save the report.

     In this example we're filtering the [Retail Analysis sample](powerbi-sample-tutorial-connect-to-the-samples.md) to show only values where **Territory** equals **NC**.

     ![Report filter pane](media/powerbi-service-share-report/power-bi-filter-report2.png)

2.  Add the following to the end of the report page URL:

    ?filter=*tablename*/*fieldname* eq *value*

     The field must be of type **string** and neither *tablename* or *fieldname* can contain spaces.

    In our example, the name of the table is **Store**, the name of the field is **Territory**, and the value we want to filter on is **NC**:

     ?filter=Store/Territory eq NC

    ![Filtered report URL](media/powerbi-service-share-report/power-bi-filter-url3.png)

    Your browser adds special characters to represent slashes and spaces, so you end up with:

    app.powerbi.com/groups/me/reports/010ae9ad-a9ab-4904-a7a1-10a61f70f2f5/ReportSection2?filter=Store%252FTerritory%20eq%20NC

3.  Send this URL to your coworkers. 

    When they select the link, Power BI opens a read-only version of the filtered report.

## Next steps

- Have feedback? Go to the [Power BI Community site](https://community.powerbi.com/) with your suggestions.
- [How should I collaborate on and share dashboards and reports?](powerbi-service-how-should-i-share-my-dashboard.md)
- [Share a dashboard](powerbi-service-share-unshare-dashboard.md)
- More questions? [Try the Power BI Community](http://community.powerbi.com/).