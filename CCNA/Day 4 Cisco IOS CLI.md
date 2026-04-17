# Cisco IOS cli
console port ใช้ config
ใช้สาย rollover cable config รู RJ45 ไม่ก็ mini-USB

`>` USER EXEC mode
`#` PRIV EXEC mode
## command
`enable` - enter priv
`configure terminal` - global config mode
`enable password [text]`
`enable secret [text]` ดีกว่า pwd ใช้ MD5
`service password-encryption` เปิดกันมอง pwd 

**mode config**
1. running-config 
2. startup-config

**show config**
`show running-config`
`do sh run`

**save config**
`write`
`write memory`
`copy running-config startup-config`

**output เพิ่มเติมกันลืม**
`enable secret 5 $1$mERr$YlCkLMcTYWwkF1Ccndtll.` 
`enable password 7 08026F6028`
> 5 กับ 7 เป็น mode pwd

