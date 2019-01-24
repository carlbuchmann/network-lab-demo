# branch1-wan Environment State Summary

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

      172.16.0.0/16 is variably subnetted, 4 subnets, 2 masks
C        172.16.101.0/24 is directly connected, Tunnel10
L        172.16.101.21/32 is directly connected, Tunnel10
C        172.16.102.0/24 is directly connected, Tunnel11
L        172.16.102.21/32 is directly connected, Tunnel11
D     172.20.0.0/16 [90/56371200] via 172.16.101.1, 00:21:07, Tunnel10
      172.21.0.0/16 is variably subnetted, 4 subnets, 3 masks
D        172.21.0.0/16 is a summary, 00:22:01, Null0
C        172.21.0.0/30 is directly connected, GigabitEthernet4
L        172.21.0.1/32 is directly connected, GigabitEthernet4
C        172.21.255.1/32 is directly connected, Loopback0
D     172.22.0.0/16 [90/61491200] via 172.16.101.1, 00:21:07, Tunnel10
```

##  show ip interface brief

```
Interface              IP-Address      OK? Method Status                Protocol
GigabitEthernet1       172.16.1.15     YES TFTP   up                    up      
GigabitEthernet2       10.255.21.2     YES manual up                    up      
GigabitEthernet3       192.168.21.2    YES manual up                    up      
GigabitEthernet4       172.21.0.1      YES manual up                    up      
Loopback0              172.21.255.1    YES manual up                    up      
Tunnel10               172.16.101.21   YES manual up                    up      
Tunnel11               172.16.102.21   YES manual up                    up
```

##  show ip eigrp neighbor

```
EIGRP-IPv4 VR(ENTERPRISE-EIGRP) Address-Family Neighbors for AS(100)
H   Address                 Interface              Hold Uptime   SRTT   RTO  Q  Seq
                                                   (sec)         (ms)       Cnt Num
1   172.16.101.1            Tu10                     59 00:21:08   10   100  0  7
0   172.16.102.1            Tu11                     47 00:22:02   12   100  0  9
```
