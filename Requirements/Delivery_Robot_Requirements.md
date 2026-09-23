# Autonomous Delivery Robot – Requirements

| Req. ID | Requirement |
|--------|-------------|
| R1 | The robot shall remain in IDLE state when no delivery request is available. |
| R2 | The robot shall start navigating toward the destination when a valid delivery request is received. |
| R3 | The robot shall continuously monitor its surroundings while navigating. |
| R4 | The robot shall enter AVOIDING_OBSTACLE state when an obstacle is detected during navigation. |
| R5 | The robot shall resume navigation toward the destination after the obstacle has been successfully avoided. |
| R6 | The robot shall start the delivery process only after reaching the destination. |
| R7 | The robot shall return to the warehouse after successfully delivering the package. |
| R8 | The robot shall return to the warehouse when its battery level becomes critically low during navigation. |
| R9 | The robot shall become IDLE after reaching the warehouse. |
| R10 | The robot shall not enter DELIVERING directly from IDLE or AVOIDING_OBSTACLE states. |
