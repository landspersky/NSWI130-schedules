# Unauthorized user creating/modifying schedules

Containers in question:
- API Gateway
- SIS admin Backend

Source of Stimulus: Unauthorized or anonymous user.

Stimulus: Unauthorized user attempts to create or modify schedules.

Environment: SIS Admin Backend - production environment.

Problem: Unauthorized access to schedule creation/modification endpoints.

Response:
- The system rejects the request HTTP 401/403.
- All unauthorized attempts are logged (user ID if available, source, timestamp, endpoint).
- Repeated unauthorized attempts trigger administrator alerts.
- After exceeding a defined threshold, the source is rate-limited or temporarily blocked.
- All authorized schedule changes are fully audited (who, when, what changed).

Measure:
- 100% of changes are logged.
- Alerts are sent within 1 minute of more than 10 unauthorized attempts.
- Rate limiting/blocking is enforced after 20 failed attempts within 10 minutes.