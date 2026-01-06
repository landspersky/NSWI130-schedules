# SIS AB versus Notifications

Containers in question:
    - SIS admin backend
    - Notifikacni sluzba

Source of Stimulus: A notification event occurs.

Stimulus: SIS admin backend requests for a notification to be sent.

Problem: Notification service is busy (full queue). All notifications must be delivered somehow sometime (QoS)

Response: Have an internal output-facing queue, when notification service is available again, send.

Measure: Downtime depending on the availability of the notification service 

---

Architecture design fix: not needed

