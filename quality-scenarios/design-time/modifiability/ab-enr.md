# SIS AB versus Enrollments module

Containers concerned:
    - Správce rozvrhových lístků
    - Správce notifikací o rozvrhu

Source of Stimulus: Maintainers of Enrollment Module want to make a change to their API

Stimulus: adding new functionality or changing response formats.

Environment: Admin Backend

Response:
- Quickly get the system back to working state
- Developer makes small changes in a centralized container which fixes communication across the board.
- System down for maximum of *measure* duration

Measure: 1 man-day fix

---

Architectural problem: Non-centralized access to Enrollment module in AB. The design makes it difficult to quickly and efficiently adapt our system to the changes in the external module.

Design fix: Create new container for unified communication with Enrollment module.


