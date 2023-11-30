# All Glass Lane Divider
## What they do:
The lane dividers will divide the bottles from one lane of single line to two seperate lanes of single line. This is used to send bottles to either MX4 or to either lane for the bulk palletizer.

## How they work:
These are driven off of solenoid valves and air cylinders. The decisions for how the lane divider determines when to move is based of a collection of photo eyes. Two which are inside the divider cabinet at the exit of the transfer arm that count and detect jams and one each on the individual lanes that the divider feeds to that will indicate a back up.

## Logic
### Clamp
* Transitioning from left or right lane
* B38241 (left lane photo eye) is blocked + 1500ms timer
* B38261 (right lane photo eye) is blocked + 1500ms timer
* Both B38241 and B38261 are blocked + 1000ms timer
### To Move Left
* B38261 (right lane photo eye) is blocked
* Channel Count is complete while in right lane position
* 