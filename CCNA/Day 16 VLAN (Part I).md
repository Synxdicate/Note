# VLAN
เริ่มต้นที่ LAN/Broadcast Domain

Broadcast domain - group devices that will recieve `FFFF.FFFF.FFFF`
![[p16.1.png]]
> รูปนี้ขาด broadcast domains อะไรบ้าง

ทำไมต้องทำ VLAN?
1. performance
2. security
กันเรื่องใช้ Broadcast Domain เปลือง

inter-VLAN routing

router ไม่ส่งข้าม VLAN แม้อยู่ใน subnet เดียวกัน

VLANS-`1` = default
VLANS-`1002-1005` = old technologies

ถ้า assign VLAN ที่ยังไม่มี ตัว switch จะสร้าง VLAN มาให้
## command
`switchport mode access`
`switchport access vlan [num]`
`show vlan brief`