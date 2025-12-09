# SIS AB versus Notifications

Containers in question:
    - SIS admin backend
    - Notifikacni sluzba

Problem: Notification service is busy (full queue)
All notifications must be deliviered somehow sometime (QoS)

Solution: Have an internal output-facing queue, when notification service
is available, send.

