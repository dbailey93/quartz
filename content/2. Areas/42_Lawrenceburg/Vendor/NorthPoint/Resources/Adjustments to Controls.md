**Casepack to hand pack**

**Goal**: To make the casepack <-> handpack transition a single button operation.

**Current State**: When going from case pack mode to hand pack mode requires the following steps and at least two people.
1. Have one person stop the flow of boxes at the top of carton line before the carton divider either with a pole or someone on a ladder
2. Another person will then have to go to the case conveyor panel to press the button to transition the divider
	1. While here also turning on the hand pack station conveyors
3. One person will then have to walk around the machine to the 1 -> 2 chanellizer and manually change that position
4. Finally one person will then walk back around the machine to the platform in front of the hand pack station to begin packing bottle in the cartons
---
**Future State**: The ideal scenario for this would be to have a single operator be able initiate the change from the platform where they handpack.

<u>**Key points to make this happen**</u>

- We would need a physical button at the handpack station to initiate this. 
	- If we want to keep the software based button on the conveyor HMI screen, this will need to be a momentary push button as to not confuse the states. There are options around this, but I believe it to be unnecessarily complicated in my opinion. 
	- Simple indications for an illuminated button would be:
		- Light On = Handpack
		- Light Off = Casepack
- We need a case stop and a presence indicating photo eye to prevent jam ups when we transition between the different states. Right now this is not feasible and I would consider the controlled divider to be non functional for the intended use case
	- The case stop would be a piston based box stop with a side gripping pad. The boxes will move in a slug manner, so you will not have spaces between the cases
	- The photo eye would be used for delaying the swing of the divider arm before the boxes have been cleared
- The channelizer will also need to change when pressing this button.
	- I believe this is possible as long as the ProFace HMI is connected to the conveyor PLC. This is something I will try while the machine is on site. It will just look for a change in state of the conveyor mode and move accordingly

**Sequence for Future**
\* Steps 2 and 3 would operate in tandem as they are independent processes

1. The operator presses the divider change button at the handpack platform
2. Case Divider
	1. The case stop initiates
	2. The photo eye will wait until there are no boxes present in front of it
	3. The divider arm will change position
	4. The case stop will release
3. 1 -> 2 Channelizer
	1. The conveyors for the handpack table will turn on
	2. the chanellizer will change position and send bottles to the hand pack station