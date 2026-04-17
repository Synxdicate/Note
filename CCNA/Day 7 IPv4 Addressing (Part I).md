# IPv4 Addressing
- dotted decimal & binary
- network portion & host portion
- class
- netmask
- network address & broadcast address
![[p7.1.png]]

`xxxx.xxxx.xxxx.xxxx` มี 4 octet
`xxxx` = 8 bits
`192.168.1.1` -> dotted decimal
Example. `10011010010011100110111100100000`
`10011010` `01001110` `01101111` `00100000`
`154.78.111.32`

## Loopback Address
ตั้งแต่ `127.0.0.1 - 127.255.255.255`
ไว้ test 'network stack' บน local

## Class
![[p7.2.png]]
class A - leading bits **0**
class B - leading bits **10**
class C - leading bits **110**
class D - leading bits **1110** multicast addresses
class E - leading bits **1111** reserved (experimental)

**host address** เป็น `O's` 
**network address** ไม่สามารถ sign เป็น host ได้

`1's` หมด เป็น **broadcast address** ไม่สามารถ sign เป็น host ได้ 
