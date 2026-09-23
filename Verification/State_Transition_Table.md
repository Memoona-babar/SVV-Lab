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
