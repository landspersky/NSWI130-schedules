# Consistency of schedules during concurrent updates

Containers in question:
- SIS Admin Backend
- Schedule Database

**Stimulus:**
Multiple authorized users attempt to modify the same schedule at the same time.

**Environment:**
Production or development environments with concurrent access.

**Problem:**
Conflicting updates may lead to inconsistent or lost schedule data.

**Solution:**
- Implement optimistic concurrency control or locking mechanisms to prevent lost updates.
- Notify users if a schedule has been modified by someone else before their changes are saved.
- Log all conflicting update attempts for audit and troubleshooting purposes.
- Provide clear error messages and guidance to users when conflicts occur.
