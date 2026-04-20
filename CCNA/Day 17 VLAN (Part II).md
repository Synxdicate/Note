# Trunk Ports
แก้ปัญหา router มี interface ไม่พอที่จะเชื่อม VLAN

trunk port = tagged ports
access port = untagged ports

**Trunking Protocol**:
1. ISL
2. 802.1Q
![[Pasted image 20260419125921.png]]
มี 2 field หลัก ๆ
- Tag Protocol Identifier (TPID) - 16 bits set เป็น `0x8100` เป็น 802.1Q
- Tag Control Information (TCI) - 12 bits
	- PCP(Priority Code Point) - 3 bits ใช้เป็น CoS
	- DEI(Drop ...) - 1 bit
	- VID(VLAN ID) - 12 bits VLAN ที่ 0 กับ 4095 โดนจองใช้ไม่ได้
![[Pasted image 20260419130545.png]]
VLAN range (1-4094):
- 1-1005: normal VLAN
- 1006-4094: extend VLAN
อันเก่าบางตัวใช้ extended VLAN ไม่ได้

native VLAN