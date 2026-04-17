# IPv4 Addressing (Part 2)
![[p8.1.png]]

maximum ของ host per network
จากรูป (p8.1)
256-2=254 แปลว่าเหลือ host ให้ใช้งานได้ 254
โดย -2 มาจาก 
host portion all 0s = **network address** (network ID)
host portion all 1s = **broadcast address**
$$maximum\ host\ per\ network=2^n-2$$
$$when\ n =number\ of\ host\ bit$$

![[p8.2.png]]

## commands
`show ip interface brief`
`show interfaces [interface]`
`interface [int-name] [x/x]`
`ip address [ip-address] [subnet]`
`no shut` state -> up (enable)
`do sh ip int br`
`show interfaces description`
`description [commends]` ทำอยู่ใน (config-if)

![[p8.3.png]]
- status ของ L1
- Protocol ของ L2

## quiz
```
network address: 43.0.0.0
maximum host: 2^24-2 (16,777,214 host)
broadcast address: 43.255.255.255
first: 43.0.0.1
last: 43.255.255.254

129.221.23.13/16
network address: 129.221.0.0
maximum host: 2^16-2 (65,534 hosts)
broadcast address: 129.221.255.255
first: 129.221.0.1
last: 129.221.255.254

209.221.3.22/24
network address: 209.221.3.0
maximum host: 2^8-2 (254 hosts)
broadcast address: 209.221.3.255
first: 209.221.3.1
last: 209.221.3.254

2.71.209.233/8
- 2.0.0.0
- 2^24-2 (16,777,214 hosts)
- 2.255.255.255
- 2.0.0.1
- 2.255.255.254

155.200.201.141/16
- 155.200.0.0
- 2^16-2 (65,534 hosts)
- 155.200.255.255
- 155.200.0.1
- 155.200.255.254
```
