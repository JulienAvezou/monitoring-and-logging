# monitoring-and-logging

You are only as secure as your weakest link -> its important to get visibility upfront

AWS provides CloudTrail and CloudWatch

CloudTrail: enables continuous monitoring and auditing of API calls
-> can store logs in S3 or CloudWatch (for visuals and alerts configuration via metrics)

1. Enable CloudTrail to collect auditing data
-> enabled by default in AWS, for 90 days
-> can use the Event History to find/filter for events
-> all auth events are logged in N.Virginia AWS region

<img width="1352" alt="Capture d’écran 2024-06-13 à 16 08 00" src="https://github.com/JulienAvezou/monitoring-and-logging/assets/62488871/54341067-c9a2-4301-88b5-9b8d465f904d">

   
However Events Management is limited
To create an ongoing record of activity to capture info across all regions -> create a trail
   
2. Configure CloudTrail to forward the events
Can see trail logs in CloudWatch log groups and filter them using queries

<img width="1101" alt="Capture d’écran 2024-06-13 à 17 04 32" src="https://github.com/JulienAvezou/monitoring-and-logging/assets/62488871/524799a6-5a8b-4174-8409-4fbb6322040e">
<img width="1351" alt="Capture d’écran 2024-06-13 à 16 59 23" src="https://github.com/JulienAvezou/monitoring-and-logging/assets/62488871/922c0db6-e7f0-4e57-afc9-421f884742a2">
<img width="1280" alt="Capture d’écran 2024-06-13 à 16 54 46" src="https://github.com/JulienAvezou/monitoring-and-logging/assets/62488871/7718bcac-3466-4fdf-bd0b-ab4b1a563980">


4. Configure alarms with CloudWatch
- define which metrics you want to monitor
- can confgure SNS topic to receive email notification
- can also configure automatic actions to trigger if alarm goes off
- can create custom metrics -> metric filter
- use event history after alarm triggers for debugging and investigations

<img width="1228" alt="Capture d’écran 2024-06-13 à 17 15 47" src="https://github.com/JulienAvezou/monitoring-and-logging/assets/62488871/47aaaed2-6800-4de9-890d-83d54d5589ba">
<img width="1131" alt="Capture d’écran 2024-06-13 à 17 38 00" src="https://github.com/JulienAvezou/monitoring-and-logging/assets/62488871/23f2483d-d9f9-4cbc-a9ea-0602d17af08a">
<img width="1105" alt="Capture d’écran 2024-06-13 à 17 41 51" src="https://github.com/JulienAvezou/monitoring-and-logging/assets/62488871/b81ee2be-cc09-451f-a55e-a02a56de0a94">
<img width="1059" alt="Capture d’écran 2024-06-13 à 17 54 53" src="https://github.com/JulienAvezou/monitoring-and-logging/assets/62488871/21279001-7689-449c-8f7c-593a2dfe24b5">
<img width="1158" alt="Capture d’écran 2024-06-13 à 17 58 35" src="https://github.com/JulienAvezou/monitoring-and-logging/assets/62488871/f25f1d0b-f87f-43da-a490-b56c22b86725">
<img width="1137" alt="Capture d’écran 2024-06-13 à 18 03 21" src="https://github.com/JulienAvezou/monitoring-and-logging/assets/62488871/609fc711-1c4d-4faa-a4e9-217ff2b949a3">
<img width="1129" alt="Capture d’écran 2024-06-13 à 18 06 45" src="https://github.com/JulienAvezou/monitoring-and-logging/assets/62488871/2ad065de-fdb0-48a0-8a41-4bffb4ad1851">
<img width="1092" alt="Capture d’écran 2024-06-13 à 18 07 07" src="https://github.com/JulienAvezou/monitoring-and-logging/assets/62488871/12784644-234a-439f-9af5-7ef2493e95fa">
<img width="1242" alt="Capture d’écran 2024-06-13 à 17 15 03" src="https://github.com/JulienAvezou/monitoring-and-logging/assets/62488871/ad5c6525-140a-4673-a8f7-78139d89a186">


4. Configure specific alarms for billing costs
-> AWS Budgets
<img width="1014" alt="Capture d’écran 2024-06-13 à 18 15 03" src="https://github.com/JulienAvezou/monitoring-and-logging/assets/62488871/a35d9574-e519-41ce-a521-495dc2b21aa5">
