
# Requirements Traceability Matrix

| Requirement ID | State / Transition | Operation ID | Constraint ID | Test Case ID | Risk |
|---|---|---|---|---|---|
| FR-01 | ST-01: IDLE | OP-01 | C-01 | TC-10 | High |
| FR-02 | IDLE to NAVIGATING | OP-02 | C-01 | TC-03 | High |
| FR-03 | Command validation | OP-03 | C-08 | TC-01, TC-02 | Critical |
| FR-04 | NAVIGATING to AVOIDING_OBSTACLE | OP-04 | C-02 | TC-05 | Critical |
| FR-05 | AVOIDING_OBSTACLE to NAVIGATING | OP-05 | C-02 | TC-05 | High |
| FR-06 | NAVIGATING to DELIVERING | OP-06 | C-03 | TC-06 | Critical |
| FR-07 | DELIVERING to RETURNING | OP-07 | C-04 | TC-06 | Critical |
| FR-08 | Chamber monitoring | OP-08 | C-06 | TC-07 | Critical |
| FR-09 | Chamber correction | OP-09 | C-06 | TC-07 | Critical |
| FR-10 | Event logging | OP-12 | C-09 | TC-03, TC-09 | High |
| HR-01 | SAFE_MODE | OP-10 | C-05 | TC-04 | Critical |
| NFR-02 | 20 connected robots | OP-11 | C-10 | TC-08 | High |
| HR-02 | Railway crossing | OP-04 | C-07 | TC-05 | Critical |
| HR-03 | LINK_LOST | OP-11 | C-10 | TC-09 | Critical |
| HR-04 | Chamber protection | OP-09 | C-06 | TC-07 | Critical |
