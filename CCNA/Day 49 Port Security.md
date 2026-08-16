```
int [interface]
switchport port-security
exit
show int [interface] switchport
```

Secure-up = port sec and interface enable

ErrDisable Recovery
```
show errdisable recovery

errdisable recovery cause psesure-violation

errdisable recovery interval 180
```

Violation Modes
- shutdown
- Restrict - เกิด sec violation count เพิ่ม กับ unauthorized traffic โดน discard
- Protect - sec violation count = 0

```
switchport port-security
switchport port-security mac-address [mac]
switchport port-security violation [mode]
```

Secure MAC address aging
- aging time ถ้า = 0 mins ไม่มี age out
- aging type
	- absolute
	- inactivity
- SecureStatic Address Aging
```
switchport port-security aging time [minutes]
switchport port-security aging type {absolute | inactivity}
```

sticky secure mac address
```
switchport port-security
switchport port-security mac-address sticky
```


```
show mac address-table secure
```

![[Pasted image 20260815154705.png]]