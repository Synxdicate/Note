# IPv4 Header

**Version** 4 bits ใช้บอกเวอร์ชั่นอย่าง IPv4=0100, IPv6=0110 
1. **Internet Header Length (IHL)**
	4 bits (สูงสุด 15 bits) บอก total length header -> `n*4-bytes` 
	- minimum ipv4 header length = 20 bytes
	- maximum ipv4 header length = 60 bytes

2. **DSCP&ECN**
	- **DSCP** 6 bits ใช้ทำ QoS
	- **ECN**   2 bits แจ้งเตือนอาการคอขวดระหว่าง router

3. **Fragmentation**
	- **Identification** 16 bits เก็บ ID ของ packet
	- **Flag** 3 bits
		- bit 1: reserved
		- bit 2: DF
		- bit 3: MF ถ้า 1 มีต่อ ถ้า 0 คือชิ้นสุดท้าย
	- **Fragment Offset** 13 bits บอกลำดับ

4. **TTL** 8 bits กัน Routing loop ทีละ hop ลดทีละหนึ่ง

5. **Protocol** 8 bits L4PDU
	- 1=ICMP
	- 6=TCP
	- 17=UDP
	- 89=OSPF
**Header Checksum**
เช็ค error ใน IPv4 header 
L4 protocol checksum error ใน encap data
**Source/Dest IP Address**
32 bits
**options**
0-320 bits

MTU(**M**aximum **T**ransmission **U**nit)=1500 bytes

# เพิ่มเติม
Padding ใน options ถ้า data ยาวไม่พอที่จะหาร 4 ลงตัว จะเติม 0 เพื่อให้จบที่ 32-bit boundary
