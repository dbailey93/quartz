# Auto Labeling Fixes

## Scope
The Auto Labeling fixes that are implemented are to adjust how the time stamp is matched with the APS developed labeling service and the Kolinahr Labeler in Lawrenceburg (and eventually Elmira). 

**The Problem:** When pallets are coupled from the palletizer -> shuttle car -> load center, the order of the coupled pallets will change their order due to load/unload position. This will cause the pallets to get a pallet number that does not correspond with the sequence of creation.

*This only happens between pallets on the same shop as the pallets from differing shops will contain their own numbering set*

---
**Some comments on the current state:**
- This has not been ran since roughly April or May of 2021, so we do not have any recent data
- There was initially some confusion about whether this system has ever been ran or even works at all
	- We have ran the auto labeling system since start up
	- It was created and tested by Alejandro Rojas from EMS
	- It works from previous runs except in the situation where the order is changed
- Every pallet that arrives at the labeler (as long as the tracking was not lost due to different issues) will contain unique information about the pallet that will be able to properly keep them in order of creation time
- The information that arrives with the pallets at the labeler contains:
	- Source line number
	- Timestamp
	- unique message ID for the pallets



### Current State: 
The pallet information and pallet number is generated at the exit of the Palletizer (31, 32, 33, or 34). This is then passed along the process in the four possible paths below:
<br></br>
![[Pasted image 20220209082058.png]]
<p style="text-align:center;">Figure 1. Pallet Paths</p>
<br></br>
The pallets that leave the palletizer are coupled (two at a time) onto the shuttle cars. 


Pallet **1** will always have an earlier timestamp than pallet **2**. When these pallets swap as shown below, the pallet number will apply to the first pallet to arrive regardless of the timestamp. This is due to the fact that the labeler has no knowledge of what the timestamps are until the pallets arrive.


<br></br>
![[Pasted image 20220209083930.png]]
<p style="text-align:center;">Figure 2. Pallet Load Order</p>
<br></br>

Given the paths that were shown in *Figure 1*, there is a chance depending on which path is taken that the pallets that arrive at the labeler will be in the original order of **1** first and **2** second. In this scenario, everything works as it should. In the scenario where the pallets arrive at the labeler with **2** first and **1** second, the labeler will pull the first pallet number for the pallet in the order that they arrived.

```ad-note
title: Example
color: 255,0,0
- Two pallets move from 34 shop.
- Pallet **2** arrives before pallet **1**.
- Pallet **2** will get pallet number 256 and then pallet **1** will get pallet number 257.

The time stamps will print correctly on these, but the pallet numbers will show out of order.
```



---

### Future State
The idea to fix this is to use the data that is created at the palletizer to create a string ID that gets sent to a data base. By loading these into a database, we can increment the pallet numbers as they are created versus at the time of arrival to the labeler. 

There are a couple of ways that we can complete this. 
1. Creating a tag that is a concatenated string that contains the date and time stamp of the pallet created. 
2. Another is using the unique pallet ID that is already created at the exit of the palletizer.

**Option #1**

Pros | Cons
---|---
The ground work has already been started on this, so it may be the easiest to implement | This may not be the most robust method for preventing issues in the future
It is a method that APSEng is already somewhat familiar with | It is essentially doing extra work on top of an already existing system

**Option #2**

Pros | Cons
---|---
This is used already on the machines and was created by the engineers that are actually familiar with the original code of the machines | Will require some additional support
Should allow us to do more of the tracking and numbering of the pallets at a lower level than we are currently doing | Cost associated with the support -- $8400 




Things that will need to be done in order to complete this:
> Things in bold are done by David Bailey. Things not in bold will be done by either APS Eng or other
- [ ] Turn on the auto-labeling system to observe current state
- [x] **Create historian tags for palletizer**
- [x] **Create historian tags for labeler**
- [ ] Create database for tags to populate in
- [ ] **Test run of matching tags**
- [x] Create API to match the pallet data between palletizer and labeler
- [ ] Do API call to windows label service when pallet arrives at labeler
- [ ] Write matching code for the current web based label making site used in plants
- [ ] **Test run of matching tags with API call**


