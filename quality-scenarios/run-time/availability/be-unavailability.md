# SIS Backend Unavailability

Containers:

- SIS Admin Backend
- SIS Backend

**Stimulus:**
A request to backend fails due to its temporary unavailability.

**Environment:**
Production or development.

**Problem:**
Requests are not processed.

**Solution:**
Add API gateway with fault tolerance and retry mechanism.
The said event will be logged and retried in under 1s.
