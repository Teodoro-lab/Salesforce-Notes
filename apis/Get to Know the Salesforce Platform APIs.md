# Get to Know the Salesforce Platform APIs

**REST API**, **SOAP API**, **Bulk API**, and **Streaming API**. Together they make up the *Salesforce data APIs*.

These four APIs apply broadly across the spectrum of core Salesforce data.



## REST API

- Can execute *CRUD* on records, *search or query* your data, *retrieve object metadata*, and access *information about limits* in your org. 

    

- It is exceptional for writing mobile and web apps because of its **RESTful approach**. 

    

- Supports *XML* and *JSON* formats.



## SOAP API

- It uses a *Web Services Description Language (WSDL)* file to rigorously define the parameters for accessing data through the API.

    

- Because SOAP API uses the WSDL file as a formal contract between the API and consumer, it’s great for **writing server-to-server integrations**.

    

- It Only supports *XML*.



## Bulk API

- Bulk API is a specialized RESTful API for loading and *querying lots of data at once*.

    

- **< 50,000** records.

    

- It is **asynchronous**, meaning that you can submit a request and come back later for the results(this is the recommended approach).

    

-  There are **two versions** of Bulk API (*1.0* and *2.0*).

    

- Bulk API is great for performing tasks that involve lots of records, such as **loading data into your org** for the first time.



## Streaming API

- Streaming API is a specialized *API for setting up notifications* that trigger when changes are made to your data.

    

-  It uses a publish-subscribe model in which **users can subscribe to channels that broadcast certain types of data changes**.

    

- The pub/sub model reduces the number of API requests by eliminating the need for polling. Streaming API is great for writing apps that would otherwise need to frequently poll for changes.



## API Access and Authentication

- To access the salesforce API's you need one of these orgs:
    - Enterprise Edition
    - Unlimited Edition 
    - Developer Edition 
    - Performance Edition
    - Professional Edition

> Make sure that you have the “API Enabled” permission, and you’re ready to start integrating.

*All API calls require authentication*, , except for the SOAP API **login()** call. 

You can either use one of the supported OAuth flows or authenticate with a session ID retrieved from the SOAP API **login()** call. 



## API Limits

- Salesforce limits the number of API calls per org to ensure the health of the instance.  There are **three types of API limits**: 

    - *timeout limits:*  <u>Restrict the length of time a single call is allowed to run.</u>

    - *concurrent request limits:*  <u>Cap the number of long-running calls that are running at one time.</u> (Concurrent limits vary by org type).

    - *total request allocations:* <u>Cap the number of calls made within a rolling 24-hour period.</u> (Total limits vary by org edition and license type, including any add-on licenses you purchase.)

        

- You have several ways to check your **remaining API calls**:

    - The API Usage box on the System Overview page. (From Setup, enter System Overview in the Quick Find box, then select **System Overview**.)
    - Information returned in the Sforce-Limit-Info response header for REST APIs.
    - Information returned in the response body (in <type>API REQUESTS</type>) for SOAP APIs.
    - The [/limits](https://developer.salesforce.com/docs/atlas.en-us.224.0.api_rest.meta/api_rest/resources_limits.htm) call in the REST API.
    - The API Request Limit per Month [usage-based entitlement](https://help.salesforce.com/articleView?id=users_understanding_tenant_usage_entitlements.htm&language=en_US), which shows you your org’s API calls aggregated over 30 days.

    You can also set up notifications for when your org exceeds a number of API calls that you designate. To do so, from Setup, enter API Usage Notifications in the Quick Find box, then select **API Usage Notifications**.



## Which API Do I Use?

Check when to use each of them [in trailhead !!!](https://trailhead.salesforce.com/es-MX/content/learn/modules/api_basics/api_basics_rest)

| API Name           | Protocol            | Data Format       | Communication                                     |
| :----------------- | :------------------ | :---------------- | :------------------------------------------------ |
| REST API           | REST                | JSON, XML         | Synchronous                                       |
| SOAP API           | SOAP (WSDL)         | XML               | Synchronous                                       |
| Connect REST API   | REST                | JSON, XML         | Synchronous (photos are processed asynchronously) |
| User Interface API | REST                | JSON              | Synchronous                                       |
| Analytics REST API | REST                | JSON, XML         | Synchronous                                       |
| Bulk API           | REST                | CSV, JSON, XML    | Asynchronous                                      |
| Metadata API       | SOAP (WSDL)         | XML               | Asynchronous                                      |
| Streaming API      | Bayeux              | JSON              | Asynchronous (stream of data)                     |
| Apex REST API      | REST                | JSON, XML, Custom | Synchronous                                       |
| Apex SOAP API      | SOAP (WSDL)         | XML               | Synchronous                                       |
| Tooling API        | REST or SOAP (WSDL) | JSON, XML, Custom | Synchronous                                       |