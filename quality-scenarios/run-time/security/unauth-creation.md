# Unauthorized user creating/modifying schedules

Containers in question:
- SIS adming Backend

Stimulus: Unauthorized user attempts to create or modify schedules.

Environment: SIS Admin Backend

Problem: Unauthorized access to schedule creation/modification functionality.

Solution:
- Log of all unauthorized access attempts.
- Log changes made to schedules, including user ID, timestamp,
and details of the changes.
- Implement alerting mechanism to notify administrators
of repeated unauthorized access attempts.
- After a certain number of anonymous failed attempts, 
rate limit further attempts from the same source or temporarily block access.