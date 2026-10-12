
# SACDCS Change Log

## Project Information
- Project: Smart Autonomous Cold-Chain Delivery & Control System
- Baseline Version: 1.0
- Updated Version: 1.1
- Status: Modified

## CR-01: Safe Mode

**Requirement ID:** HR-01

**Status:** Modified

**Old Requirement:**
The robot shall enter Safe Mode when a critical battery or thermal condition is detected.

**New Requirement:**
The robot shall enter Safe Mode within 3 seconds when chamber or battery temperature exceeds the approved critical threshold, or battery capacity falls below the approved emergency level.

**Reason:**
The new requirement defines the triggering conditions and the maximum response time.

## CR-02: Robot Connections

**Requirement ID:** NFR-02

**Status:** Modified

**Old Requirement:**
The system shall support communication with multiple robots simultaneously.

**New Requirement:**
The system shall support at least 20 simultaneously connected robots.

**Reason:**
The new requirement gives an exact number of robots that can be tested.

## CR-03: Operator Authorisation

**Requirement ID:** FR-03

**Status:** Modified

**Old Requirement:**
Only authenticated operators shall be permitted to issue robot commands.

**New Requirement:**
The system shall require authenticated and role-authorised operators before accepting any robot command.

**Reason:**
The new requirement checks both operator identity and command permissions.

## Version History

| Version | Description |
|---|---|
| 1.0 | Original approved requirements |
| 1.1 | CR-01, CR-02 and CR-03 modified |
