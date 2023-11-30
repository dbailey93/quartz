Action Register for Auto Labeler


Regardless of which option we go with on the pallet identifier, the following items will need to be done by the following groups:

<u>Controls</u>
- Have identifier in historian on both the originating palletizer and the labeler
	- this is a total of 5 tags
- Populate the tags in historian
- Run the test on the pallets with the labeler turned on
- Run a test on the manual load and entry of pallets done by fork truck drivers

<u>APS Engineering</u>
- Create database for the tags to have them assigned a pallet number by the order that they are created
- Write the code for the API call when the pallet arrives at the labeler to match with the pallet in the table
- Any other code work that needs to be done to integrate this with the existing label program that is in use.
