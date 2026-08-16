spanning tree protocol = IEEE  802.1D
loop free topology
ถ้าไม่ใช้ stp จะเกิด broadcast storm

1. Root bridge election (one per LAN)
	- lowest BID
2. Root port selection (one per switch)
	- lowest root cost
	- lowest neighbor BID
	- lowest neighbor port ID
	- Lowest local port ID
3. Designated port selection (one per segment)
	- Port on switch with lowest root cost
	- port on switch with lowest BID 
	- lowest local port ID
# Root Bridge Election
## Bridge ID
BID = 64 bit number แบ่งเป็น  **Bridge Priority + VLAN ID and MAC address**
Bridge Priority = 16 bits
MAC address = 48 bits
![[Pasted image 20260816150541.png]]

default priority value = 32768

BID = priority number + vlan id ถ้ามันเท่ากันทั้งหมดก็เลือก mac address ต่ำสุด

Path Cost
## Root Port Selection
![[Pasted image 20260816175317.png]]
เริ่มแรกจะคิดจาก 
- **Root Cost**
	
| Speed    | Path Cost |
| -------- | --------- |
| 10 Gbps  | 2         |
| 1 Gbps   | 4         |
| 100 Mbps | 19        |
| 10 Mbps  | 100       |
	ถ้ามี 2 Port ที่เท่ากันก็ไปเคสต่อไป

- **Neighbor BID**
	ดูว่า Port ไหน BID น้อยสุด ถ้ายังไม่ได้

- **Neighbor port ID**
	แต่ละ port มีเลขซ้ำหรือไม่ซ้ำก็ได้ ตัวอย่างเช่น
	G0/0 = 123.1
	G0/1 = 123.2
	ดังนั้น G0/0 ได้เป็น RP
	
	แต่จะมีบางกรณีอย่างเช่น
	G0/0 = 123.1
	G0/1 = 123.1
	มันเท่ากันก็ต้องไปทำ
- **Lowest port ID**
	จะเลือกจากชื่อ port เลขน้อยสุด อย่างเช่น G0/0 และ G0/1
	Root Port จะเป็น G0/0 เพราะ 0<1
# การคำนวณ
1. หา BID แต่ละ switch ว่าตัวไหนมีค่าน้อยสุดโดยคิดจาก Priority + VLAN ID and MAC address ถ้า SW ไหนน้อยได้เป็น Root Bridge (เป็นจุดศูนย์กลางของ topology)
2. หา Root Port ของแต่ละ SW ประมาณว่าเส้นทางที่เชื่อมไปยัง Root Bridge โดยใช้ Path Cost น้อยที่สุดของแต่ละ SW 
3. กำหนด DP และ BLK โดยเอาค่า BID แต่ละ SW มาคำนวณถ้าเท่ากันหมดให้คิดจาก MAC address โดย SW ที่มีเลข MAC ต่ำเป็น DP และ SW ที่เป็นเลข MAC สูงจะเป็น BLK 
ปล.
ถ้าอีกข้างเป็น RP อีกข้างต้องเป็น DP เท่านั้น !
# Conclusion
- **Root Bridge:** BID ต่ำสุด
- **Root Port (RP):** พอร์ตของ Non-Root Switch ที่ Root Path Cost ต่ำสุดวิ่งหา RB
- **Designated Port (DP):**
    - ทุกพอร์ตบน Root Bridge
    - ฝั่งที่มี Root Path Cost ต่ำกว่าบน Link นั้น
    - ฝั่งที่มี BID/MAC ต่ำกว่า (ถ้า Cost เท่ากัน)
- **Blocking Port (BLK):** พอร์ตที่เหลือที่ไม่ใช่ทั้ง RP และ DP