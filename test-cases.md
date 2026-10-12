# Task 2: Test Cases
## 1. Functional and Safety Test Cases
| Test Case ID | Requirement | Test Scenario | Test Steps | Expected Result | Priority |
|---|---|---|---|---|---|
| TC-01 | CR-03 | Unauthenticated operator | Send a command without login. | System rejects the command. | Critical |
| TC-02 | CR-03 | Unauthorized operator | Send a command without permission. | System rejects the command. | Critical |
| TC-03 | CR-03 | Authorized operator | Login and send a valid command. | System accepts and records the command. | High |
| TC-04 | CR-01 | Critical battery condition | Simulate a critical battery condition. | Robot enters Safe Mode within 3 seconds. | Critical |
| TC-05 | HR-02 | Obstacle or railway crossing | Simulate an obstacle or unsafe crossing. | Robot avoids the obstacle or waits for safe crossing conditions. | Critical |
| TC-06 | FR-06, FR-07 | Medicine delivery | Complete delivery at a verified destination. | Robot delivers medicine and returns to the warehouse. | High |
| TC-07 | CR-01, HR-04 | Unsafe chamber | Simulate unsafe temperature or an open chamber door. | System activates protection and prevents unsafe batch removal. | Critical |
| TC-08 | CR-02 | Twenty robots connect | Connect 20 robots at the same time. | System supports all 20 connected robots. | High |
| TC-09 | HR-03 | Communication link loss | Disconnect the link during operation. | Robot follows its approved safe response and records the event. | Critical |
| TC-10 | FR-01 | Robot startup | Switch on the robot. | Robot starts in IDLE state. | High |
## 2. Regression Test Cases
| Test Case ID | Change Request | Test | Expected Result |
|---|---|---|---|
| RT-01 | CR-01 | Repeat critical condition tests. | Safe Mode activates within 3 seconds. |
| RT-02 | CR-02 | Test delivery with 20 connected robots. | Delivery operations work correctly. |
| RT-03 | CR-02 | Disconnect one robot. | Other robots continue operating correctly. |
| RT-04 | CR-03 | Test valid and invalid operator permissions. | Only authenticated and authorized commands are accepted. |
| RT-05 | CR-03 | Check command and safety-event records. | Required records are saved correctly. |
## 3. Change Request Mapping
| Change Request | Description | Test Cases |
|---|---|---|
| CR-01 | Safe Mode within 3 seconds of a critical condition. | TC-04, TC-07, RT-01 |
| CR-02 | Support at least 20 simultaneously connected robots. | TC-08, RT-02, RT-03 |
| CR-03 | Require authentication and role authorization. | TC-01, TC-02, TC-03, RT-04 |
