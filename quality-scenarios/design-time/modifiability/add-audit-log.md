# Adding Audit Log Container

Containers concerned:

- Ulozeni/historizace predmetu
- Ulozeni/historizace rozvrhovych listku

Source of Stimulus: Teacher, who has governance over a course, made a mistake when editing the course.

Stimulus: Administrator notices and needs to investigate who did it and what exactly happened.
Inform other staff that, for example, they should double check the data they are submitting.

Environment: Admin Backend

Response:

- System cannot provide audit trail - no logging mechanism exists
- Administrator cannot determine who made the change or what the previous values were
- Developer adds Logger container to enable audit trail for future incidents and implements it into appropriate components.

Measure: 2 man-day

---

Architectural problem: No mechanism to log who performed which operations and when. Cannot track modifications to courses or timetables.

Design fix: Create Logger container with loggerDB. Manager components (course_manager, ticket_manager) emit audit events after successful operations.
