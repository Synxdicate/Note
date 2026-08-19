# DTP ( Dynamic Trunking Protocol )
ใช้ negotiate การตั้ง trunk ระหว่าง 2 sw แทนการ manual
Switchport Mode
1. access — ปิด tag
2. trunk — เปิดใช้ tag
3. dynamic desirable — active trunk
4. dynamic auto — passive trunk
5. nonegotiate — ปิด DTP

DTP จะเปิด enable by default
`switchport mode access`
`switchport mode trunk`
`switchport mode ?`

dynamic desirable
```
switchport mode trunk
switchport mode dynamic desirable
switchport mode dynamic auto
```


ถ้า SW1 `switchport mode dynamic auto` และ SW2 `switchport mode dynamic auto` จะ operate เป็น ***static access***


ถ้า SW1 `switchport mode trunk` และ SW2 `switchport mode access` จะ operate เป็น error

![[Pasted image 20260819154640.png]]

ถ้า SW support **.1Q** กับ ISL ใช้ **DTP** ได้
default: `switchport trunk encapsulation negotiate`
ISL > .1Q
## command
```
show int [int] switchport
```

```
Switch(config-if)# switchport mode access              // access ถาวร
Switch(config-if)# switchport mode trunk               // trunk ถาวร
Switch(config-if)# switchport mode dynamic auto        // passive
Switch(config-if)# switchport mode dynamic desirable   // active
Switch(config-if)# switchport nonegotiate              // ปิด DTP
```

```
Switch# show dtp                        // สรุปสถานะ DTP ทั้งสวิตช์
Switch# show dtp interface fa0/1        // ดู DTP รายพอร์ต
Switch# show interfaces switchport      // ดูโหมดที่ตั้ง + โหมดที่ทำงานจริง
Switch# show interfaces trunk           // ดูพอร์ตที่เป็น trunk จริงๆ
```
# VTP ( VLAN Trunking Protocol )
สร้าง VLAN ที่ SW เดียวแล้วให้มันไปแจกจ่าย VLAN เอง

VTP mode
1. server
	add/modify/delete VLANs
2. client
	cant add/mod/del VLANs จะ sync กับ VLAN database เข้ากับ server
3. transparent — forward อย่างเดียว ไม่มีรับจาก VLAN จากตัวอื่น revision number = 0
4. off
VTPv1/v2 ไม่ support extended VLAN range (1006-4094)

## command
```
Switch(config)# vtp domain MYDOMAIN          // ตั้งชื่อ domain
Switch(config)# vtp mode server              
Switch(config)# vtp password MYPASS          // ตั้งรหัส
Switch(config)# vtp version [n]                // เลือกเวอร์ชัน
Switch(config)# vtp pruning                  
```

```
Switch# show vtp status         
Switch# show vtp password       // ดูรหัส VTP
Switch# show vtp counters       // ดูสถิติ advertisement
```