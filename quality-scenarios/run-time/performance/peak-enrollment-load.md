# SIS Backend Performance During Enrollment Period

Containers concerned:

- SIS backend
- Adresář rozvrhových lístků
- Adresář předmětů
- Databáze rozvrhů
- Databáze předmětů

Stimulus: Thousands of students simultaneously searching for courses and viewing
timetables during enrollment period

Environment: Production environment during peak enrollment (start of
"zápis season")

Problem: SIS backend must handle expected load during enrollment period

Response: System maintains response times under 2 seconds for course searches
and timetable queries

Measure:

- Let's say we wish for: 95th percentile response time < 2s for read operations
- System handles hundreds of concurrent requests without degradation
- No failed requests due to timeouts or resource exhaustion

Solution approach:

- Read-only backend is horizontally scalable (as per architectural decision)
- Database read replicas for courseDB and scheduleDB
- Caching layer for frequently accessed course and timetable data
- Connection pooling
