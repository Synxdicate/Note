# Routing
**Routing** is the process routers use to determine the optimal path for **IP packets** to travel across a network to reach their destination
- **routing** 
- **routing table** เก็บ route ไว้แล้วว่าต้องไป next-hop ไหน
instruction:
จะส่งไปยัง network X ต้องส่ง packet ไป next-hop Y
**method**:
1. Dynamic Routing
2. Static Routing

C-connected = network อย่างถ้า router รู้จัก network วงนี้จะส่งไปที่ interface นี้ ส่งตรง "net วงนี้อยู่ที่ interface นี้ ให้ส่งมานี่เลย"
L-local route = IP address ของ router ใน interface นั้น ๆ `/32` ก็แปลว่า fix  
![[CCNA/images/p11.1.png|546]]
จะเก็บ 2 route ไว้

ถ้าใช้ `no shut` แล้ว C กับ L จะ route ให้เลย

ถ้ามี packet ส่งเข้ามาที่ router แล้ว ใน packet ส่ง `192.168.1.1`
ตัว router จะ route ไปยังที่**เจาะจงก่อน** ( most specific ) เลือก prefix length มากกว่า

ถ้า router ไม่รู้จัก ip desc ก็ drop ทิ้ง
ต่างกับ switch จะ flood
## commands
`show ip route`