# TIPS
tips

qcow2 压缩
```
qemu-img convert -c -O qcow2 /dev/shm/win.qcow2 /home/soft/kvm/ocr.qcow2
```
端口转发
```
#清空所有规则：
iptables -Z
iptables -X
iptables -F

#恢复所有访问
iptables -P INPUT ACCEPT
iptables -P FORWARD ACCEPT
iptables -P OUTPUT ACCEPT


echo 1 > /proc/sys/net/ipv4/ip_forward
[root@localhost test]# iptables -t nat -A PREROUTING -p tcp -i ens33 --dport 3389 -j DNAT --to 192.168.122.232:3389
[root@localhost test]# 
[root@localhost test]# iptables -t nat -A POSTROUTING -j MASQUERADE
[root@localhost test]# iptables -t nat -L -n --line-number
```
