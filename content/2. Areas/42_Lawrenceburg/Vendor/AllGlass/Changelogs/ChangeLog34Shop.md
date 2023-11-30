# Change Log - 34 Shop
#changelog

### Date: [[2022-02-10]]
Routine: 14_Zone_2_Divider_Output, 
Rung: 
- [ ] Adjustments
	- [x] Motor(s):  M12971, M12941, M12841
	- [ ] Photo Eye(s): 
	- [ ] Timer(s): 
	- [ ] Other: 
- [x] New Logic

**Description:**
Added a timer based on M12971 stopping. When M12971 is stopped for 3 seconds or longer, then M12941 and M12841 will both stop.
**Reason for change:**
This was added to help prevent overfeeding the mass flow before the second single filer when running flasks.

---


### Date: [[2022-03-04]]
Routine: _11_Zone2_Squeezer_To_MX4_Output
Rung: 3
- [x] Adjustments
	- [ ] Motor(s): 
	- [ ] Photo Eye(s): 
	- [ ] Timer(s): 
	- [x] Other: 
- [ ] New Logic

**Description:** Added a temp bypass for the lack of a squeezer motor

**Reason for change:** need to have alternate route due to the bypass conveyor also having issues


---