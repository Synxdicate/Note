# Ethernet LAN Switching (Part 1)

Ethernet Frame
![[p5.1.png]]
1. **Preamble** - (7 bytes), ไว้ sync clock
2. **SFD** ( Start Frame Delimeter ) - (1 bytes) , ระบุจุดสิ้นสุด Preamble/ จุดเริ่มต้น frame
3. **Destination** (6 bytes) เก็บเลข MAC ปลายทาง
4. **Source** - (6 bytes) เก็บเลข MAC ต้นทาง 
5. **Type/Length** - (2 bytes) type of packet encapsulate
	1. ถ้าเป็น 1500 หรือน้อยกว่า = Length ข้อมูล
	2. ถ้าเป็น 1536 หรือมากกว่า = Type protocol
6. FCS ( Frame Check Sequence ) - (4 bytes) เป็น CRC algorithm -> Cyclic Redundancy Check
ทั้งหมด 26 bytes (ไม่รวม Packet)

pattern
`10101011` pattern SFD
type
`0x86dd` IPv6
`0x0800` IPv4

## MAC
**physical address** 6 bytes อีกชื่อเรียก "burn-in address (BIA)"
> มีอยู่ใน `show interfaces [int]`

ครึ่งแรก (24 bits) ระบุบริษัทที่จด OUI
ครึ่งหลัง (24 bits) unique อุปกรณ์

FORWARD (Know Unicast frame) = อันนี้รู้ว่าต้องส่งไปที่ interface ไหน
FLOOD (Unknow Unicast frame) = ไม่รู้จัก เลยส่งไปหาทุก interface เพราะว่าไม่รู้เลข MAC นี้

	MAC address table ไว้เก็บ Source MAC จาก frame ที่ส่งไปมา

# Part 2
minimum size Ethernet frame = 64 bytes (payload + head + tail)
header+tail = 18
**minimum payload**  = 46 bytes 
ถ้า payload น้อยกว่า 46 bytes จะเพิ่ม padding จนเต็ม 46 bytes

## ARP
address resolution protocol
ใช้หาเลข MAC(L2) จาก IP address(L3)
- **ARP request** - broadcast 
- **ARP reply** - unicast
`FFFF.FFFF.FFFF` เลข MAC ไว้ broadcast
**command**
`arp -a`
`show arp`
`show mac address-cable`
`clear mac address-cable dynamic` เคลียทั้งหมด
`clear mac address-cable dynamic [เลข mac]`
`clear mac address-cable dynamic interface [int-id]`
**Info**
Who has `[dest ip]`? Tell `[src ip]`

**troubleshoot**
![[p5.2.png]]
ที่มี error เพราะว่า PC1 ยังไม่รู้จัก MAC ปลายทาง เลยต้องใช้ ARP

## สรุป 
ARP ทำงานก่อน ICMP
ICMP แบ่งเป็น ICMP echo request กับ ICMP echo reply ทำงานแบบ unicast