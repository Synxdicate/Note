# Switch Interfaces
up/up (status/Protocol) เปิด auto ถ้าเชื่อมต่อแล้ว

administratively down $\ne$ down/down
## Duplex
**Half Duplex** - ส่งพร้อมกันไม่ได้ ถ้ารับข้อมูลอยู่ต้องรอค่อยส่ง แก้ปัญหาโดยใช้ **CSMA/CD** (collision detection)
**Full Duplex** - ส่งพร้อมกันได้
![[p9.1.png]]
## Speed/Duplex Autonegotiation
speed auto และ deplex auto ตั้งเป็น default
![[p9.2.png]]
host กับ switch จะเลือก best ของ speed/duplex เพื่อใช้ได้เต็มที่

ถ้า autonegotiation ปิดอยู่ 
- จะเลือก **SPEED** ต่ำสุด อย่างมี 10/100/1000 จะเลือก 10
- Duplex : 
	- ถ้า SPEED เป็น 10 หรือ 100 -> Half Duplex
	- ถ้า SPEED เป็น 1000 -> Full Duplex

![[p9.3.png]]

## command
`show interfaces status`
`speed ?` ใน (config-if)
`duplex ?` ใน (config-if)
`interface range [int][num] - [num], [int] - [int]`