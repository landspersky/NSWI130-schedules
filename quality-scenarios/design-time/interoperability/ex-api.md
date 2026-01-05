# External UI vs SIS backend

Containers in question:
- External UI
- API Gateway 
- SIS Backend

Source of Stimulus:
External UI

Stimulus: External UI makes API request

Environment: SIS Backend - production.

Response:
API Gateway authenticates, authorizes, and logs the request.
SIS Backend processes the request and returns schedule data according to access rights.
The response conforms to the API specification.

Measure:
\>= 99.9% of valid requests are successfully processed.
100% of responses conform to the API schema.
100% of requests are logged by the API Gateway.