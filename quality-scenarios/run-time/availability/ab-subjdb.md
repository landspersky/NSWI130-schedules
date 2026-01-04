# SIS AB versus Subject database

Containers in question:
    - SIS Admin Backend
    - Subject database

Source of Stimulus: User requests to view their schedule

Stimulus: Subject database outage - backend is unable to read/write data about a subject. 

Environment: Admin Backend

Response:
- Retry five times, after that return error to UI.
    - If this is happening too many times, alert admin
- Log all unsuccessful attempts with useful information

Measure: max 5s downtime if retry is successful

---

Architectural problem: No mechanism in the AB to be able to log events.

Design fix: Create logger container



