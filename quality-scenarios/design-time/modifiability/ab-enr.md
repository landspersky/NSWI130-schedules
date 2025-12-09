# SIS AB versus Enrollments module

Containers concerned:
    - Správce rozvrhových lístků
    - Správce notifikací o rozvrhu

Stimulus: Enrollment module makes an API change

Environment: Admin Backend

Problem: Non-centralized access to Enrollment module in AB

Fix: Create new container for unified communication with Enrollment module

Response: Developer makes small changes in new container which fixes communication across the board.

Measure: 1 man-day fix

