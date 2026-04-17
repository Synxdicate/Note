# Static Routing
**default gateway = default route**
default route เป็น least specific
จะส่ง packet ไปนอก network ต้องส่งไปที่ default gateway 
`0.0.0.0/0` = `0.0.0.0 - 255.255.255.255`
**two-way reachability**
router ไม่จำเป็นต้อง route เท่าหมด แค่ส่ง packet ไปให้ router อีกตัว ง่าย ๆ ก็คือ ทำหน้าที่ของตัวเอง ไม่เป็นต้องทำทั้งหมด ก็คือแค่ทำ next-hop

![[p11.2.1.png]]


![[p11.2.2.png]]
<center>ตัวอย่างการทำ default route</center>


## commands
`ip route [ip-address] [netmask] [next-hop]`
`ip route [ip-address] [netmask] [exit-int]` directly connect
`ip route [ip-address] [netmask] [exit-int] [next-hop]`
`ip route 0.0.0.0 0.0.0.0 [next-hop]` 

`show running-config | include ip route`
เพิ่มเติม
`exit-int` ใช้ Proxy-ARP

จากที่ลองทำแลปแล้วต้อง route ทั้งสองข้างอย่างที่ว่า two-way reachability

ใน SW layer 2 จะไม่เปลี่ยนเลข MAC