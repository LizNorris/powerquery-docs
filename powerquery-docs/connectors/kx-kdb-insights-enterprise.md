# kdb Insights Enterprise Power Query Connector

!!!note

    The following connector article is provided by KX Systems Inc., the owner of this connector and a member of the Microsoft Power Query Connector Certification Program. 
    
    If you have questions regarding the content of this article or have changes you would like to see made to this article, visit the [KX](www.kx.com) website and use the support channels there.


The certified [_KX kdb Insights Enterprise_ Power Query Connector](https://learn.microsoft.com/en-us/power-query/connectors/) supports the Import data connectivity mode.

The connector enables Microsoft Power BI users to remotely connect, explore, query data, preview tables, and harness the power and performance of kdb Insights Enterprise analytics before importing datasets into Power BI for visualization.

## Summary

| Item	                         | Description   |
| ------------------------------ | ------------- |
| Release State                  | General Availability |
| Products                       | Power BI (Semantic models)<br/>Power BI (Dataflows)<br/>Power Apps (Dataflows)

| Authentication Types Supported | Database (Username/Password)<br/>OAuth

Function Reference Documentation | [KX kdb Insights Enterprise](https://code.kx.com/insights/enterprise/index.html)


## Prerequisites

Ensure the following prerequisities are met before proceeding:

1. kdb Insights Enterprise 1.11.0 or above is [installed](https://code.kx.com/insights/enterprise/getting-started/index.html) and running at least one database.

1. Permissions to query data on the running databases.


## Capabilities supported

- Import
    - Filtering
    - Aggregation
    - Group By


## Connect to kdb Insights Enterprise 

To make the connection, follow these steps:

1. Open Microsoft _Power BI Desktop_ or _Power BI Online_.

1. Open the Get Data screen:
    - For **Power BI Desktop**, click `Get Data -> More` from the **Home** tab in the upper ribbon.
    - For **Power BI Online**, in the Get Data experience, select the `Dataflow` category. Refer to [Creating a dataflow](https://learn.microsoft.com/en-us/power-bi/transform-model/dataflows/dataflows-create) for instructions.

1. Enter **KX kdb** into the search box.

1. Select **KX kdb Insights Enterprise**.

1. Click **Connect**.

1. Enter the URL for your _kdb Insights Enterprise_ deployment.

1. Click **OK**.

1. You are prompted to sign in if you have not signed in recently or have never signed in:

    - If you have not signed in recently or have never signed in click **Sign in**. The button is named **Sign in as a different user** if your login credentials have expired or are no longer valid.

        ![sign-in](images/powerbi-signin.png)

1. If your credentials are valid, the Connector popup displays that you are currently signed in and you can click the **Connect** button.

    ![signed-in](images/powerbi-signedin.png)


1. The **Navigator** dialog box displays all the running databases and tables for your chosen host on the left. Clicking on a table returns a preview of the selected data using the _kdb Insights Enterprise_ [getData REST API](https://code.kx.com/insights/api/database/query/get-data.html).

    ![navigator-preview](images/powerbi-preview.png)



## Navigator Options

The [parameters](https://code.kx.com/insights/1.11/enterprise/integrations/powerbi/powerbi-import.html#parameters) available on the Navigator allow you to leverage the power of kdb Insights Enterprise analytics to filter, group, and aggregate data by restricting the data being loaded and bringing you the performance of the _kdb Insights database_.


    | **Parameter** | **Details**                                                                      |
    | ------------- | -------------------------------------------------------------------------------- |
    | Start Time    | Applies to the partitioned column and will be ignored for non-partitioned tables |
    | End Time      | Applies to the partitioned column and will be ignored for non-partitioned tables |
    | Filter        | Filters out certain rows                                                         |
    | Aggregation   | Filters the columns and/or aggregates the rows being returned                    |
    | Group By      | Group the results of an aggregation based on specific columns                    |
