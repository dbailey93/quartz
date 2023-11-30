
### Date: [[2022-05-23]]
Routine: Stacker - S000_STA_OUT
Rung: 1
- [x] Adjustments
	- [x] Motor(s): Infeed_Conv_1411
	- [ ] Photo Eye(s): 
	- [ ] Timer(s): 
	- [ ] Other: 
- [x] New Logic

**Description:**
![[Pasted image 20220523084524.png]]
**Reason for change:**

Added new bit:
InfeedBottleStop

This was to send a zero speed command to the Allglass reference bit

---


### Date: [[2023-03-08]]
Routine: 
Rung: 
- [x] Adjustments ✅ 2023-03-14
	- [ ] Motor(s): 
	- [ ] Photo Eye(s): 
	- [ ] Timer(s): 
	- [x] Other: ✅ 2023-03-14
- [ ] New Logic

**Description:** Changed Head Rotation: Movement per Encoder Revolution value from 3600 to 3500

**Reason for change:** After the main head rotation shaft broke, the encoder seemed to have failed as well. The newly installed encoder would not allow the head to rotate correctly to 180 degrees, stopping at ~130 degrees instead
![[Pasted image 20230314124706.png]]


---