# Routing
- **routing** 
- **routing table**
method:
1. Dynamic Routing
2. Static Routing

C-connected = network อย่างถ้า router รู้จัก network วงนี้จะส่งไปที่ interface นี้
L-local = IP address router ของ interface นั้น ๆ `/32` ก็แปลว่า fix 
![[p11.1.png|546]]

ถ้าใช้ `no shut` แล้ว C กับ L จะ route ให้เลย

ถ้ามี packet ส่งเข้ามาที่ router แล้ว ใน packet ส่ง `192.168.1.1`
ตัว router จะ route ไปยังที่**เจาะจงก่อน** 
## commands
`show ip route`