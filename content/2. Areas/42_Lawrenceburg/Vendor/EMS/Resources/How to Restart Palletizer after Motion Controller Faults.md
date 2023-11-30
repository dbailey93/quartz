# How to Restart Palletizer after Motion Controller Faults
### Quick steps to recover
1. If the Head will not move on the  palletizer, check the electrical cabinet for the status on the Schneider PacDrive Modules
	1. If the Motion Controllers are operating correctly, they should look like this:
	![[allGoodState.jpg|500]]
2. If the "State" Light is red (and is the only light that is red), the drive is likely has some sort of fault. 
	1. First step would be to remove the 24v power supply off the top of the controller
	![[PacDrive24v.jpg|300]]
	3. Remove the 24v off of the Lexium drive
	![[lexium24v.jpg|300]]
	3. Remove the green Ethernet cable from the front of the PacDrive
	![[PacDriveEthernet.png|300]]
	4. Wait 5-10 seconds and plug the 24v power back in to both.
	5. Once the devices boot up, plug the Ethernet cable back in
	6. If all lights go to green, try to reset from the HMI
3. If the "S3" Light is red, there is some sort of communication issue going to the field devices
	1. Power down the entire machine (Main Disconnect on the electrical panel) for about 10 minutes.