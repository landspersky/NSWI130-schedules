# SIS Backend Unavailability

Containers:

- SIS Admin Backend
- SIS Backend

**Stimulus:**
BE is temporarily unavailable due to heavy load or other problem.

**Environment:**
Production or development.

**Problem:**
Requests are not processed due to unavailability.

**Solution:**
Add API gateway with fault tolerance and retry mechanism.
