
### 2023-03-15

##### Cemlink 6
![Pasted image 20230315100743.png](Pasted%20image%2020230315100743.png)

``````ad-note
Input bit 33 correlates to Unit_3 Furnace Online. This is likely a watchdog bit that feeds from the connected TK3 PLC. TK3 PLC IP address is

![Pasted image 20230315101619.png](Pasted%20image%2020230315101619.png)
``````
---
##### Meraki

The PLC is communicating with our network at half duplex rates:
![Pasted image 20230315101327.png](Pasted%20image%2020230315101327.png)

This is forced on in the Meraki dashboard:
![Pasted image 20230315101757.png](Pasted%20image%2020230315101757.png)

There is also an alarm indicating high CRC Errors on this port
![Pasted image 20230315101843.png](Pasted%20image%2020230315101843.png)