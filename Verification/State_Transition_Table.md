# Autonomous Delivery Robot – State Transition Table

| Current State | Event / Condition | Next State |
|---|---|---|
| IDLE | Delivery Request Received | NAVIGATING |
| NAVIGATING | Obstacle Detected | AVOIDING_OBSTACLE |
| AVOIDING_OBSTACLE | Obstacle Avoided | NAVIGATING |
| NAVIGATING | Destination Reached | DELIVERING |
| DELIVERING | Delivery Successful | RETURNING |
| NAVIGATING | Critical Battery | RETURNING |
| RETURNING | Warehouse Reached | IDLE |

## Verification Activity

### Check 1 – Invalid Transition

IDLE → DELIVERING

This transition is invalid because the robot must first receive a delivery request and navigate to the destination.

Violated Requirements: R6, R10


### Check 2 – Missing Transition

If there is no transition from AVOIDING_OBSTACLE to NAVIGATING, the robot cannot continue its delivery journey after avoiding an obstacle.

Required transition:

AVOIDING_OBSTACLE → NAVIGATING


### Check 3 – Obstacle During Delivery

AVOIDING_OBSTACLE → DELIVERING

This transition is invalid.

The robot must first return to NAVIGATING and then reach the destination before entering DELIVERING.
