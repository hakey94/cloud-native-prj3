**Note:** For the screenshots, you can store all of your answer images in the `answer-img` directory.

## Verify the monitoring installation

See image follow path: Project_Starter_Files-Building_a_Metrics_Dashboard\solution-images\verify-pods.png
See image follow path: Project_Starter_Files-Building_a_Metrics_Dashboard\solution-images\verify-pod-services.png
See image follow path: Project_Starter_Files-Building_a_Metrics_Dashboard\solution-images\all-namespace.png

## Setup the Jaeger and Prometheus source
See image follow path: Project_Starter_Files-Building_a_Metrics_Dashboard\solution-images\grafana-dashboard.png

## Create a Basic Dashboard
See image follow path: Project_Starter_Files-Building_a_Metrics_Dashboard\solution-images\basic-dashboard.png

## Describe SLO/SLI
A Service-Level Indicator (SLI) is a specific/actual metric used to measure the performance of a service, while the Service-Level Objective (SLO) is a measurable goal set by the team to ensure a standard level of performance during a specified period of time.

The application had an uptime of 97.2% at running time point, and the average time taken to return a request was 100 ms.

## Creating SLI metrics.
these SLIs. 
- Network Uptime/Availability: 
    High uptime is essential for customer satisfaction and reliability. Customers expect services to be consistently available, and frequent downtime can lead to frustration, decreased trust, and potential loss of business. Ensuring high uptime is crucial for maintaining a positive user experience and operational integrity.

- Response Rate: 
    Response rate directly impacts customer satisfaction. Faster response times generally lead to higher satisfaction levels, as customers appreciate timely attention to their needs. It also helps in managing customer expectations and improving overall service efficiency 
- Memory used:
    it affects the performance, stability, scalability, and efficiency of applications and services
- CPU used:
    it impacts application performance, system stability, resource efficiency, scalability, and user experience
- Error Rate: 
    Error Rate is the percentage of acceptable errors within a given period. For example, a 1% error rate would result in an SLO at 99%, indicating that the customer is having a relatively error-free positive experience.

## Create a Dashboard to measure our SLIs
relate to: solution-images/sli-dashboard.png

## Tracing our Flask App
relate to: solution-images/flask-app.png
## Jaeger in Dashboards
relate to: solution-images/jaeger-tracing.png

## Report Error
*TODO:* Using the template below, write a trouble ticket for the developers, to explain the errors that you are seeing (400, 500, latency) and to let them know the file that is causing the issue also include a screenshot of the tracer span to demonstrate how we can user a tracer to locate errors easily.

**TROUBLE TICKET**

Name: Error in trial/app/app.py

Date: August 31, 2024 11:00:44

Subject: Cannot retrieve the number of jobs from provided URL

Affected Area: "./reference-app/trial/app/app.py", line 62, in trial-app

Severity: High

Description: JSONDecodeError: There's an issue around the way the request-response data is structured, cannot evaluate the length of the JSON output. It seems to be a problem with the jobs endpoint.


## Creating SLIs and SLOs
SLO: 99.9% uptime/month
SLIs:
    The application had an uptime of 99.98% last month
    99% of the requests in the previous month was served in < 199ms
    The average of 2xx/3xx responses from the application in the previous month is 98.3%
    The application error rate last month is 0.05%

## Building KPIs for our plan
- 10 error responses in the last 24 hours.
Successful requests/minute: this KPI indicates how well is performed our system.
Error requests/minute: this KPI is an analogous of this SLI.
Uptime - this KPI indicates if errors are comming from downtime or not.
- Average response time of < 2000ms in the last 24 hours.
Average response time: this KPI is an analogous of this SLI.
Uptime - this KPI will help us to determine if response time is affected by downtime of a service.

## Final Dashboard
relate to: solution-images/final-dashboard.png
- success requests/minute:
- error requests/minute
- Avg response time/minute
- Avg memory used/minute