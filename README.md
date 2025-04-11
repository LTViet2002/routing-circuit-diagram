![image](https://github.com/user-attachments/assets/3ea35dd5-d46b-4fc7-9f9f-7a36fa95b38e)

sơ đồ dự án thiết kế sơ đồ mạng cho công ty vừa và nhỏ

Cấu hình IP

IP 172.18.0.2/30 được sử dụng cho Router0

IP 172.18.0.21/30 được sử dụng cho Router1

IP 172.18.0.9/30 được sử dụng cho Router2

IP 172.18.0.1/30 được sử dụng cho Multilayer switch1

IP 172.18.0.22/30 được sử dụng cho Multilayer switch2

IP 172.18.0.10/30 được sử dụng cho Multilayer switch3

IP 192.168.10.2/28 được sử dụng cho Server-PT Web

IP 192.168.10.3/28 được sử dụng cho Server-PT FTP

IP 192.168.10.4/28 được sử dụng cho Server-PT DNS

Access control list

Access-list 10 deny 10.0.4.0 0.0.1.255

Access-list 10 deny 10.0.6.0 0.0.1.255

Access-list 10 permit any

int vlan 10

ip access-group 10 out

exit

int vlan 20

ip access-group 10 out

exit

int vlan 50

ip access-group 10 out

exit

Dòng lệnh này có nghĩa là không cho VLAN 10, VLAN 20, VLAN 50 không thông với các  VLAN 30, VLAN 40
