**protocol** คือกฎการคุยกันอ่ะ
**IEEE**
- 802.3 ethernet
- 802.11 wifi
**IETF**
- TCP,IP,UDP,HTTP,etc.
- RFC
stack of protocols = **network stack**
RFC 791 = "internet protocol"
## Layers
![[p3.1.png]]
Content layer -> Recipient Layer -> Address Layer -> Local Delivery Layer -> Infra Layer


**application layer** - คุยผ่าน app
**transport layer** - คุยผ่าน port (end-to-end)
**internet layer** - คุยผ่าน IP address กับ routers (end-to-end) 
**local network layer** - คุยผ่าน MAC กับ switch (hop-to-hop)
**physical layer** - คุยผ่านสาย, fiber optic, ไร้สาย

### layer 2: local network layer
hop to hop นับได้จาก host to router, router to router
MAC(media access control) address ของรูเสียบ LAN
### layer 3: internet layer
internet = inter-network ก็คือระหว่างคุยระหว่าง network
เน้น router ใช้ IP address คุยกันส่งไปหา host IP ปลายทาง
protocol:
- IP
- ICMP
### layer 4: transport layer
process-to-process, service-to-service
ใช้เลข port คุยกัน
protocol:
- TCP
- UDP
### layer 5: Application layer
ดูว่า app ต้องการรูปแบบการคุยแบบไหน
- อย่าง web ใช้ HTTP,HTTPS

## Encapsulation & Decapsulation
![[p3.2.png]]
> ตรง L2 trailer ไว้เช็ค transmission error

## PDU
PDU(protocol data unit)

L4PDU = segment(TCP) datagram(UDP)
L3PDU = packet
L2PDU = frame

payload ตัวที่โดน encap ชั้นก่อนหน้า
- frame เป็น payload ของ segment
## Adjacent-layer interaction
![[p3.3.png]]
layer n ต้นทาง คุยกับ layer n ปลายทาง


ส่วนใหญ่ network resource ใช้ 5-layer
L7 - application, presentation, session 
L2 - data link
L3 - network