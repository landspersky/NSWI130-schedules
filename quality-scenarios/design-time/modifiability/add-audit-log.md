# Adding Audit Log Container

Containers concerned:

- Správce předmětů
- Správce rozvrhových lístků
- Uložení/Historizace rozvrhových lístků
- Uložení/Historizace předmětů

Stimulus: Compliance requirements demand complete audit trail of all course and
timetable modifications (who changed what and when)

Environment: Development - adding new audit log container and database

Problem: System currently stores "deleted" revisions but lacks comprehensive
audit logging. Need to add audit log container to track all important operations
throughout the system.

Fix: Developer:

1. Creates new container "Logger" with database "loggerDB"
2. Manager components (course_manager, ticket_manager) send audit events after
   successful important operations

Response: Audit logging added by modifying only manager components to emit
events. Controllers, frontends, and read-path remain untouched.

Measure:

- Few changes required: only manager components modified
- No breaking changes to existing functionality
