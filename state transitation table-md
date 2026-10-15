# Delivery Robot – State Transition Verification

| Current State | Event / Condition | Next State | Requirement | Valid? | Verification Evidence |
|---|---|---|---|---|---|
| ST-01 IDLE | PowerOn and checks pass | ST-01 IDLE | FR-01 | Yes | TC-01 |
| ST-01 IDLE | Valid DeliveryRequest | ST-02 NAVIGATING | FR-01 | Yes | TC-01 |
| ST-01 IDLE | Direct delivery request without destination verification | No delivery; remain ST-01 | FR-05 | No – Invalid transition | Negative transition test |
| ST-02 NAVIGATING | ObstacleDetected | ST-03 AVOIDING_OBSTACLE | FR-04 | Yes | TC-04 |
| ST-03 AVOIDING_OBSTACLE | ObstacleCleared and route verified | ST-02 NAVIGATING | FR-04 | Yes | TC-05 |
| ST-02 NAVIGATING | DestinationReached and delivery conditions safe | ST-04 DELIVERING | FR-05 | Yes | TC-06 |
| ST-04 DELIVERING | DeliveryCompleted | ST-05 RETURNING | FR-05 | Yes | Handover test |
| ST-02 NAVIGATING | CriticalBattery and safe return confirmed | ST-05 RETURNING | FR-06 | Conditional | TC-07 |
| ST-03 AVOIDING_OBSTACLE | CriticalBattery and safe return confirmed | ST-05 RETURNING | FR-06 | Conditional | Battery fault test |
| ST-04 DELIVERING | CriticalBattery or CriticalTemperature | ST-06 SAFE_MODE | FR-06 / NFR-01 | Yes | TC-07 |
| ST-05 RETURNING | WarehouseReached | ST-01 IDLE | FR-01 | Yes | Return test |
| ST-01 IDLE | CriticalTemperature or critical fault | ST-06 SAFE_MODE | NFR-01 | Yes | Fault injection |
| ST-02 NAVIGATING | CriticalTemperature | ST-06 SAFE_MODE | NFR-01 | Yes | TC-07 |
| ST-03 AVOIDING_OBSTACLE | CriticalTemperature | ST-06 SAFE_MODE | NFR-01 | Yes | TC-07 |
| ST-05 RETURNING | CriticalTemperature | ST-06 SAFE_MODE | NFR-01 | Yes | TC-07 |
| ST-02 NAVIGATING | LinkTimeout | ST-07 LINK_LOST | NFR-04 | Yes | TC-11 |
| ST-03 AVOIDING_OBSTACLE | LinkTimeout | ST-07 LINK_LOST | NFR-04 | Yes | TC-11 |
| ST-04 DELIVERING | LinkTimeout | ST-07 LINK_LOST; suspend unsafe handling | NFR-04 | Conditional | TC-11 |
| ST-05 RETURNING | LinkTimeout | ST-07 LINK_LOST | NFR-04 | Yes | TC-11 |
| ST-07 LINK_LOST | LinkRestored and integrity checks pass | Approved recovery state | NFR-04 | Conditional | Reconnection test |
| ST-06 SAFE_MODE | FaultCleared and authorised recovery passes | Approved safe recovery state | NFR-01 | Conditional | Recovery test |
| Any active state | CrossingUnsafe before entry | Remain before crossing or enter safe stopping condition | HR-02 | Yes | TC-13 |
