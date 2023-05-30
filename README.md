**Note:** For the screenshots, you can store all of your answer images in the `answer-img` directory.

## Verify the monitoring installation
![All-pods-svcs](https://github.com/mmalzahrani/Project_Files-Building_a_Metrics_Dashboard/assets/27856878/909cec2b-4bea-4f77-9691-24be07196c31)


## Setup the Jaeger and Prometheus source
![Grafana_homepage](https://github.com/mmalzahrani/Project_Files-Building_a_Metrics_Dashboard/assets/27856878/2ddb4697-6862-4f48-ab76-6f24d9e77283)


![Grafana_Data_Sources](https://github.com/mmalzahrani/Project_Files-Building_a_Metrics_Dashboard/assets/27856878/761b2b0d-8295-47c3-9663-3e3aeeaf4c27)


## Create a Basic Dashboard
![Grafana_Dashboard_Prometheus](https://github.com/mmalzahrani/Project_Files-Building_a_Metrics_Dashboard/assets/27856878/eb71cf0e-7b4f-4454-b52e-08de1385d156)


## Describe SLO/SLI
Service level objectives (SLO):
Targets for service reliability. They define the acceptable levels of performance, availability, and other metrics for a service. SLOs are typically expressed as a percentage or a number of errors per unit of time.

Service level indicators (SLI):
Metrics that measure how close a service is to meeting its SLOs. SLIs are typically quantitative metrics, such as uptime, response time, or error rate.


## Creating SLI metrics.
Uptime: The percentage of time that a service is available.
Error rate: The percentage of requests that result in an error.
Utilization: The percentage of resources utility.
Latency: The time it takes for a request to travel from the client to the server and back.
Bandwidth: The amount of data that can be transferred between the client and the server per second.

## Create a Dashboard to measure our SLIs
*TODO:* Create a dashboard to measure the uptime of the frontend and backend services We will also want to measure to measure 40x and 50x errors. Create a dashboard that show these values over a 24 hour period and take a screenshot.

## Tracing our Flask App
*TODO:*  We will create a Jaeger span to measure the processes on the backend. Once you fill in the span, provide a screenshot of it here. Also provide a (screenshot) sample Python file containing a trace and span code used to perform Jaeger traces on the backend service.

## Jaeger in Dashboards
*TODO:* Now that the trace is running, let's add the metric to our current Grafana dashboard. Once this is completed, provide a screenshot of it here.

## Report Error
*TODO:* Using the template below, write a trouble ticket for the developers, to explain the errors that you are seeing (400, 500, latency) and to let them know the file that is causing the issue also include a screenshot of the tracer span to demonstrate how we can user a tracer to locate errors easily.

TROUBLE TICKET

Name:

Date:

Subject:

Affected Area:

Severity:

Description:


## Creating SLIs and SLOs
*TODO:* We want to create an SLO guaranteeing that our application has a 99.95% uptime per month. Name four SLIs that you would use to measure the success of this SLO.

## Building KPIs for our plan
*TODO*: Now that we have our SLIs and SLOs, create a list of 2-3 KPIs to accurately measure these metrics as well as a description of why those KPIs were chosen. We will make a dashboard for this, but first write them down here.

## Final Dashboard
*TODO*: Create a Dashboard containing graphs that capture all the metrics of your KPIs and adequately representing your SLIs and SLOs. Include a screenshot of the dashboard here, and write a text description of what graphs are represented in the dashboard.  
