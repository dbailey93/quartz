# Shakopee

### **Shakopee Obsolescence Project in Tandem with Radwell:**

> I plan to do a walkthrough of the plant to identify where all of the electrical panels are located. I have a drawing of the plant and a general idea of the locations, but not enough exactness to be able to give an accurate account to Radwell.

- I was able to get all known panels identified for marking on the AutoCAD drawing for Radwell.
- Need to rewrite charter to appease Kyle Ferguson

### **Pallet outfeed conveyor controls investigation:**

> I will be working with Jesse Nystrom (or will have him loan me his laptop) to connect to the outfeed conveyors. These are all on a PLC 5 which requires RSLogix 5. I do not posses a copy or license for the software unfortunately, so I will need to borrow what you have on site.
> From the findings I hope to be able to provide some suggestion in preventing this in the future.
> Jesse Nystrom has provided a printout of the program for review, but connecting locally to watch the I/O is the way that this needs to be done to verify all connections are properly functioning.

- Safety Photo Eyes were added on 8/22. These stop the chain conveyor from operating.
    - There was another incident overnight on 8/23
    - Suggested fix is to add the pneumatic bladders to this as well as to stop the outfeed strapper conveyor

### **Case Palletizer Programs and potential process improvement opportunities:**

> These palletizers are also on PLC 5s so I cannot view them at the moment.
> Same as the pallet outfeed, I have received the printout of the programs so I can at least do a preliminary review before connecting locally.

- During the visit to Shakopee I was unable to watch the palletizers in operation, so there will need to be a future observation for a total understanding.
- I am currently looking into layer counting HMI/visual options to use on the PLC 5 System
- Options:
    - computer using AdvancedHMI software ($)
    - Possible use of ProFace HMIs from old LAW casepackers ($)
    - Digital 7 Segment LED Display ($)
### Repack Area Counts
> Michael Beaver asked me to help with getting a PLC online to relay case counts over to APS. This should be a small project and won’t take priority over the other items on this list.

- The existing PLC was not compatible with the network setup that was requested. Jesse Nystom gave me an extra Micro1400 PLC that I was able to get programmed and on the network. He will be providing the sensor from the flap conditioner to supply counts to this.
- This will also be the PLC used for the future shop back up lights used to alarm that specific shops are dumping.
# Lawrenceburg
### Carton Shop APS/Machine Connections
> Malcolm has initiated the a project on getting APS and the carton machines on the network finally. I have been asked by Malcolm to help support some of this

### EMS Case Rotation
> The Case Rotation projected is now slated to happen on September 18-19

* I will be on site for this to help support the project.
* Lawrenceburg is providing the mechanical support for this
* 33 shop is the priority but a request to EMS to provide an additional day of programmer support to copy the changes to the other three shops
### Cold End Spray Support
>31 Shop Cold End Spray issues have been causing a lot of down time. I have been asked to help support/investigate electrical problems

* I was called in early to the plant to help with the most recent issues on 8/24
* So far nothing indicates any sort of controls issues
* The heat in the area is excessive and a solution needs to be made for this
	* There are already some vortex coolers on the sprayer cabinet, but the mixer cabinet needs to be cooler as well
# Other
### Electrical Downtime Dashboard
* Dashboard tracking the electrical downtime data from MPulse/APS
* Plan to have something to review by end of next week (9/1)

### Transformer PM Information
* Standardized PM plan for all transformers across all plants
* Work with Chris/Kelly to get this put into MPulse
* Chris provided a recommended schedule already

---
## **Shakopee**

**Shakopee Obsolescence Project in Tandem with Radwell:**

AFE has not been approved by Kyle Fergusson due to the following:
- Who will be the long term owner of this project following the delivery of the results from Radwell (Purchasing, duh)
- The previous store room audit did not go very far from purchasing and there were no project follow ups after the fact, so Kyle has low confidence in the success of this without more commitment from that team.

**Pallet outfeed conveyor controls investigation: (8/30)**

- After following an additional incident on 8/23, the strapper outfeed was requested to be added to the logic.
- Following the meeting with Drake/Kevin, Jesse reclarified what was done. He has not added the strapper outfeed to the logic.
	- Jesse claims there is an existing photo eye on the strapper that solves this problem.
	- Currently getting clarification on how this works to verify that it is viable for the safety requirements

**Case Palletizer Programs and potential process improvement opportunities:**

These palletizers are also on PLC 5s so I cannot view them at the moment. Same as the pallet outfeed, I have received the printout of the programs so I can at least do a preliminary review before connecting locally.

- During the visit to Shakopee I was unable to watch the palletizers in operation, so there will need to be a future observation for a total understanding.
- I am currently looking into layer counting HMI/visual options to use on the PLC 5 System
- Options:
    - computer using AdvancedHMI software ($)
    - Possible use of ProFace HMIs from old LAW casepackers ($)
    - Digital 7 Segment LED Display ($)

**Repack Area Counts**

- Next steps:
    - beacon lights/alarms purchased - Will get with Jesse
    - Kepware data handling configured – waiting on IT for access (delay until 9/5 due to availability and hurricane)

## **Lawrenceburg**

**Carton Shop APS/Machine Connections (?/?)**
No Update as of 8/25

**EMS Case Rotation (9/19)**
The Case Rotation projected is now slated to happen on September 18-19

- I will be on site for this to help support the project.
- Lawrenceburg is providing the mechanical support for this
- 33 shop is the priority but a request to EMS to provide an additional day of programmer support to copy the changes to the other three shops

#### The project manager for this from EMS has left the company, it is now assigned to Lorena Cavasin 8/29

**Cold End Spray Support (8/25)**
Issue:
> Cold end spray was either not spraying any liquid at all or the concentration of the liquid was not at the proper mixture

Cause:
> Heat was much too high in the area around the lehr (surfaces ~160F and ambient around 100-115F) and causing the cold end lubricant to thicken and not mix properly within the dosing system.
> Additional problem was with electrical panel for dosing system being ~170F+. This is far too hot for consistent operation.

Meeting held on 8/25 to discuss root causes and ways to mitigate.
notable actions form the meeting:
- Electrical Panel to be cooled by means of Vortex cooler and KaoWool if available
- The poly/luball barrels need to be stored in a cooler place
	- not next to lehr
- In the meantime, the barrels will be wrapped with a cooling blanket
	- ordered by Brent 8/25
- Other items ordered:
	- Platform for barrel to stand on
	- dolly to transport barrels
	- new spray nozzles from Henrryetta to trial
		- Has a more conical spray pattern

**Other**

**Electrical Downtime Dashboard (9/1)**

- Dashboard tracking the electrical downtime data from MPulse/APS
- Plan to have something to review by end of next week (9/1)

- Data from APS added to power BI dashboard, but the filtered parameters are not showing all data. Will be getting it addressed 8/31

**Transformer PM Information (8/30)**

- [ ] Standardized PM plan for all transformers across all plants
- [x] Work with Chris/Kelly to get this put into MPulse
	- [x] All PMs suggested by Chris have been added to MPulse under "1ANCHOR"
- [x] Chris provided a recommended schedule already
- [x] Annual 3rd party needs to follow same process and be performed by same company
- [ ] A matrix is being made to show current state of all plants
	- [ ] Need to verify what plants have been doing individually outside of 3rd party annuals
