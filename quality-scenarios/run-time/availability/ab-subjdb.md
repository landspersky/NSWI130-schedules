# SIS AB versus Subject database

Containers in question:
    - SIS Admin Backend
    - Subject database

Backend is unable to read/write data about a subject.

Solution of Subject database outage:
    - Retry five times, after that return error to UI.
        - If this happened often, inform sysadmin?
    - Inform (log - NENI KONTEJNER)

