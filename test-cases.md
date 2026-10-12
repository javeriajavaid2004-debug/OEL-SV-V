# SACDCS Test Cases
## TC-01: Unauthenticated Command
**Requirement:** FR-03  
**Risk:** Critical
**Steps:**
1. Do not log in.
2. Send a robot command.
3. Check the robot status and event log.
**Expected Result:** The command is rejected and logged.
## TC-02: Unauthorised Operator
**Requirement:** FR-03  
**Risk:** Critical
**Steps:**
1. Log in as an operator without the required permission.
2. Send a restricted command.
3. Check the result.
**Expected Result:** The command is rejected.
## TC-03: Valid Delivery Command
**Requirement:** FR-02, FR-03, FR-10
**Steps:**
1. Log in as an authorised operator.
2. Send a valid delivery request.
3. Check the robot state.
4. Check the event log.
**Expected Result:** The command is accepted, navigation starts and the event is logged.
## TC-04: Critical Battery
**Requirement:** HR-01  
**Change Request:** CR-01
**Steps:**
1. Simulate a critical battery condition.
2. Record the detection time.
3. Record the Safe Mode activation time.
**Expected Result:** Safe Mode activates within 3 seconds.
## TC-05: Obstacle and Railway Crossing
**Requirement:** FR-04, HR-02
**Steps:**
1. Detect an obstacle.
2. Check that navigation stops.
3. Simulate a closed railway barrier or an approaching train.
**Expected Result:** The robot handles the obstacle and does not enter an unsafe railway crossing.
## TC-06: Delivery and Return
**Requirement:** FR-06, FR-07
**Steps:**
1. Move the robot to the destination.
2. Complete delivery.
3. Check the return journey.
**Expected Result:** The robot delivers the package and returns to the warehouse.
## TC-07: Chamber Conditions
**Requirement:** FR-08, FR-09, HR-04
**Steps:**
1. Simulate an incorrect temperature.
2. Start correction.
3. Check sensor readings.
4. Attempt batch removal during protection.
**Expected Result:** The chamber verifies the temperature and blocks unsafe batch removal.
## TC-08: Twenty Robots
**Requirement:** NFR-02  
**Change Request:** CR-02
**Steps:**
1. Connect 20 robots simultaneously.
2. Check their connections and status messages.
**Expected Result:** All 20 connections are supported.
## TC-09: Communication Loss
**Requirement:** HR-03, FR-10
**Steps:**
1. Disconnect the communication link.
2. Observe the robot response.
3. Check the event log.
**Expected Result:** The approved safe response starts and the event is recorded.
## TC-10: Robot Startup
**Requirement:** FR-01
**Steps:**
1. Switch on the robot.
2. Check its initial state.
**Expected Result:** The robot enters IDLE.
## Regression Testing
| Change Request | Tests to Repeat |
|---|---|
| CR-01 | TC-04, TC-09 |
| CR-02 | TC-08, TC-03, TC-09 |
| CR-03 | TC-01, TC-02, TC-03 |
