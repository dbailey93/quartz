# Reoccurring issues on 31 shop 
## Servo drives
1. Occasionally the palletizer will fault out with a head translation error.  I'm unsure of what the initial cause of this is, but some thoughts:
	1. The Head seems to be pressed quite firmly against the table
		1. The Orange guards have been scraped clean of the paint on the tops where contact is made
2. The manual mode step-through will not complete certain steps at this point. Some examples:
	1. The curtain will not close when transitioning from the table to the loaded position
	2. The 'box aligner' rose before the head was clear and caused a crash
3. The PacDrive will not connect properly
	1. The S3 (Sercos III) will fail at maintaining a good connection.
	2. This will happen on start up as well as during production
	3. The S1 -> S3 connection loop was not properly made. I replaced the cable going from the final port on the Lexium (get number) that connects back to S3 on the PacDrive. Before this the connection loop was not communicating.
4. There is occasionally an IP conflict that happens on the second PacDrive (I believe this is for the lifting motion controls)
	1. The IP address that reads on the display is 10.129.3.104
	2. I get an email from Meraki on almost every start up of the machine that tells me there is an IP conflict with 190.201.100.100. The two associated MAC Addresses in conflict are:
		1. 00:04:17:07:AA:FC
		2. 00:04:17:07:AB:AA

![[Pasted image 20210730080205.png]]

### Needs
1. Better understanding on how to trouble shoot these issues
2. Some understanding of the communication layout in the palletizers
	1. Partly in related how the devices connect to the company network. Most of the devices are fairly exposed since the 10.129.x.x schema was used. Are we having most of our issues due to extra noise and traffic from the other networks?
3. Training on Schneider Motion Controls
4. Documentation on the Schneider Equipment
