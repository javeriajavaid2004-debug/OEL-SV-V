
# Change Request Analysis

## CR-01: Safe Mode Timing

The old requirement does not specify a response time.

The new requirement specifies 3 seconds.

**Testing:** Record the detection time and Safe Mode activation time.

**Expected Result:** Safe Mode activates within 3 seconds.

## CR-02: Simultaneous Robots

The old requirement does not specify the number of robots.

The new requirement specifies at least 20 robots.

**Testing:** Connect 20 robots at the same time.

**Expected Result:** The system supports all 20 connections.

## CR-03: Operator Authorisation

The old requirement checks authentication but does not clearly specify role authorisation.

The new requirement checks both authentication and role permissions.

**Testing:** Try commands using an unauthenticated operator, an unauthorised operator and an authorised operator.

**Expected Result:** Only the authorised operator's permitted command is accepted.

## Conclusion

These changes make the requirements clearer and easier to test.
