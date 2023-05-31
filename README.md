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
- Uptime: The percentage of time that a service is available.
- Error rate: The percentage of requests that result in an error.
- Utilization: The percentage of resources utility.
- Latency: The time it takes for a request to travel from the client to the server and back.
- Bandwidth: The amount of data that can be transferred between the client and the server per second.

## Create a Dashboard to measure our SLIs
### Uptime
![Uptime](https://github.com/mmalzahrani/Project_Files-Building_a_Metrics_Dashboard/assets/27856878/c8345433-31bd-479d-b330-d69e9d8ddf7a)

### Error Rate
![Error_rate](https://github.com/mmalzahrani/Project_Files-Building_a_Metrics_Dashboard/assets/27856878/30fa881d-7a82-4f08-b15e-97a56458655e)

### Utilization
![Utilization](https://github.com/mmalzahrani/Project_Files-Building_a_Metrics_Dashboard/assets/27856878/7e099cdf-908d-4234-8dad-66936407b2a7)

### Latency
![Latency](https://github.com/mmalzahrani/Project_Files-Building_a_Metrics_Dashboard/assets/27856878/ce034130-44f4-4120-a5b9-8f31b14403c9)

### Bandwidth
![Bandwidth](https://github.com/mmalzahrani/Project_Files-Building_a_Metrics_Dashboard/assets/27856878/f92cc161-5689-494d-a02a-9b4c655a0b4c)


## Tracing our Flask App
![Jaeger_tracing_span_Error](https://github.com/mmalzahrani/Project_Files-Building_a_Metrics_Dashboard/assets/27856878/3f6c3760-554e-4808-b0a9-5071bb24c8b7)


Python span endpoint code
```python 
# Tracer error
@app.route('/errortrace')
@by_endpoint_counter
def errortrace():
    with tracer.start_span('errortrace'):
        return "Bad Request", 400
```

## Jaeger in Dashboards
![Jaeger_Dashboard](https://github.com/mmalzahrani/Project_Files-Building_a_Metrics_Dashboard/assets/27856878/d70464f6-66e6-44b6-8f5d-00ccceba533e)


## Report Error

TROUBLE TICKET

Name: 400 BAD REQUEST on /errortrace backend app

Date: Tue, 30 May 2023 17:31:29 GMT

Subject: API endpoint BAD REQUEST

Affected Area: Backend app

Severity: High

Description: The calls in backend get Bad requests


## Creating SLIs and SLOs
- SLI: The average response time for page requests will be less than 1 second.
- SLO: The service will be available 98.9% of the time.
- SLI: The number of requests that take more than 100 milliseconds to load will be less than 1% of the total number of requests in a month.
- SLO: The website will be available for at least 99.9% of the time in a month.
- SLI: The number of 5xx, 4xx errors per day will be less than 10.
- SLO: The number of page requests per second will be greater than 1000.
- SLI: The number of errors returned by a web service will be less than 0.1% of the total number of requests in a month.
- SLO: The average latency for a page load will be less than 100 milliseconds.


## Building KPIs for our plan
- The number of minutes of downtime per month.
- The number of 500 errors per month.
- The number of errors returned by a web service per month.

## Final Dashboard
![Final_Dashboard](https://github.com/mmalzahrani/Project_Files-Building_a_Metrics_Dashboard/assets/27856878/db2571a7-b362-4434-960f-52a9a4665e14)

- Uptime: The percentage of time that a service is available.
- Error rate: The percentage of requests that result in an error.
- 40x 50x Error: The number of 5xx, 4xx errors
- Tracing ALL: The time it takes for a request to travel from the client to the server and back.

