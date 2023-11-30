# Stack Light State Meaning
---
## Needs Operator's Attention

### Solid Red Light
- Machine is stopped by either E-Stop, manually stopped, or cycle stopped
*Need to add a relay to account for the E-Stop condition*

### Blinking Red Light
- Machine is stopped due to conditional factors and would require human intervention
	- Down bottle
	- Case Jam
	- Shear Eye
	- Inverter Faults

---
## Normal Conditions

### Solid Green Light
- Machine is running normally and in operation

### Blinking Green Light
- Machine is running normally, but it is not in active operation due to other factors that are not directly caused by the case packing system
	- Waiting on ware
	- Waiting on cases
	- Cases backed up at Flap Closer (Machine after the second inspection station)
```ad-tip
color: 255,0,0
While a blinking green light may not immediately need attention, it is usually a sign of an issue at a location either before or after the casepacker.
**Be sure to investigate the area if this starts to flash**
```
