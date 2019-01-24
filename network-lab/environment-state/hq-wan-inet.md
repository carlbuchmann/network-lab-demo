# hq-wan-inet Environment State Summary

##  show ip route

```
Codes: L - local, C - connected, S - static, R - RIP, M - mobile, B - BGP
       D - EIGRP, EX - EIGRP external, O - OSPF, IA - OSPF inter area 
       N1 - OSPF NSSA external type 1, N2 - OSPF NSSA external type 2
       E1 - OSPF external type 1, E2 - OSPF external type 2
       i - IS-IS, su - IS-IS summary, L1 - IS-IS level-1, L2 - IS-IS level-2
       ia - IS-IS inter area, * - candidate default, U - per-user static route
       o - ODR, P - periodic downloaded static route, H - NHRP, l - LISP
       a - application route
       + - replicated route, % - next hop override, p - overrides from PfR

Gateway of last resort is not set

      172.16.0.0/16 is variably subnetted, 3 subnets, 2 masks
D        172.16.101.0/24 [90/15411200] via 172.16.102.22, 00:21:16, Tunnel11
                         [90/15411200] via 172.16.102.21, 00:21:16, Tunnel11
C        172.16.102.0/24 is directly connected, Tunnel11
L        172.16.102.1/32 is directly connected, Tunnel11
      172.20.0.0/16 is variably subnetted, 5 subnets, 3 masks
D        172.20.0.0/16 is a summary, 00:21:08, Null0
C        172.20.0.4/30 is directly connected, GigabitEthernet3
L        172.20.0.5/32 is directly connected, GigabitEthernet3
C        172.20.255.0/30 is directly connected, Loopback0
L        172.20.255.2/32 is directly connected, Loopback0
D     172.21.0.0/16 [90/61491200] via 172.16.102.21, 00:21:08, Tunnel11
D     172.22.0.0/16 [90/61491200] via 172.16.102.22, 00:21:08, Tunnel11
```

##  show ip interface brief

```
Interface              IP-Address      OK? Method Status                Protocol
GigabitEthernet1       172.16.1.12     YES TFTP   up                    up      
GigabitEthernet2       192.168.20.2    YES manual up                    up      
GigabitEthernet3       172.20.0.5      YES manual up                    up      
Loopback0              172.20.255.2    YES manual up                    up      
Tunnel11               172.16.102.1    YES manual up                    up
```

##  show ip eigrp neighbor

```
EIGRP-IPv4 VR(ENTERPRISE-EIGRP) Address-Family Neighbors for AS(100)
H   Address                 Interface              Hold Uptime   SRTT   RTO  Q  Seq
                                                   (sec)         (ms)       Cnt Num
1   172.16.102.21           Tu11                     54 00:22:02   10   100  0  8
0   172.16.102.22           Tu11                     43 00:22:02   11   100  0  10
```
