# Computer Networks
## Lab Manual
### Table of Contents
1. [Study of Network Devices](#Devices)
2. [Datalink Layer Framing Methods](#datalinklayer)
  1. [Character stuffing](#cs)
  2. [Bit Stuffing](#datalinklayer)
3. [Datalink Layer Framing Method checksum](#datalinklayer)
4. [Hamming code generation](#datalinklayer)
5. [Cyclic Redudancy check (CRC)](#datalinklayer)
6. [Sliding Window Protocal](#datalinklayer)
  1. [GoBack-N](#datalinklayer)
  2. [Selective-repeat-ARQ](#datalinklayer)
7. [Stop&Wait Protocol](#datalinklayer)
8. [Congestion control using leaky bucket algorithm](#datalinklayer)
9. [Dijkstra‘s algorithm to compute the Shortest path](#datalinklayer)
10. [Distance vector routing algorithm](#datalinklayer)
11. [Broadcast tree by taking subnet of hosts](#datalinklayer)

<a name="Devices"></a>
# Network devices
 Refrence: Geeks for Geeks. \
 link:https://www.geeksforgeeks.org/network-devices-hub-repeater-bridge-switch-router-gateways/


<a name="datalinklayer"></a>
# Datalink Layer Framing Methods
  There are two types of Datalink Layer Framing Methods. \
  1. Character stuffing
  2. Bit stuffing
  <a name="cs"></a>
  ## Character Stuffing
    ```
    ###Algorithm
    1. SET i =0,j=0
    2. READ a
    3. SET b[j++] = 'd'
    4. SET b[j++] = 'l'
    5. SET b[j++] = 'e'
    6. SET b[j++] = 's'
    7. SET b[j++] = 't'
    8. SET b[j++] = 'x'
    9. REPEAT 1-2 WHILE i<LENGTH(a):
       1. IF a[i]='d' and a[i+1]='l' and a[i+2]='e' THEN:
          SET b[j++]='d'
          SET b[j++]='l'
          SET b[j++]='e'
       [END IF]
       2. SET b[j++]:=a[i]
       [END FOR]
    10. SET b[j++] = 'd'
    11. SET b[j++] = 'l'
    12. SET b[j++] = 'e'
    13. SET b[j++] = 'e'
    14. SET b[j++] = 't'
    15. SET b[j++] = 'x'
    16. PRINT b.
    
