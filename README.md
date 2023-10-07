<img src="https://i.imgur.com/x0MFl0y.png" height="100%" width="100%">

## RIP Routing
  
 Stands for Routing Information Protocol. It is an Entries and Distance
vector Routing Protocol.Maximum hop count limit is 15 Hop (16 Hop will unreadable)

• Routing Information Protocol (RIP) is a distance-vector routing
protocol. Routers running the distance-vector protocol send all
or a portion of their routing tables in routing-update messages to
their neighbors.
<br/>
• AD value of RIP is 12
<br/>
• RIP is an intra-domain routing protocol used within an
autonomous system.
<br/>
• IT calculate best route to send information (Hop matrix use)
<br/>
• RIPV1 Stands for only classful IP address.
<br/>
• RIPV2 Support both classful & classless IP address
<br/>
Rip Timers
<br/>
Route Update Time :- 30 second
<br/>
Route invalid Time :- 180 second
<br/>
Route Hold down Time :- 180 second
<br/>
Route Flush Time :- 240 second>

## RIP Router Topology 
Enable Interface of R3, R3 And R3 (Serial and Fast Ethernet)
<br/>
Router 1
<br/>
Router>Enable
<br/>
Router# Configure Terminal
<br/>
Router (Config)#hostname R1
<br/>
R1 (Config)# interface Se1/0
<br/>
R1 (Config-if)# ip address 10.0.0.1 255.0.0.0
<br/>
R1 (Config-if)# clock rate 64000
<br/>
R1 (Config-if)# bandwidth 64
<br/>
R1 (Config-if)# no shutdown
<br/>
R1 (Config-if)# int fa0/0
<br/>
R1 (Config-if)# ip add 192.168.0.1 255.255.255.0
<br/>
R1 (Config-if)# no sh
<br/>
R1 (Config-if)# do show ip interface brief
<br/>
R1 (Config-if)# ctrl + z
<br/>
R1#
<br/>
Router 2
<br/>
Router>Enable
<br/>
Router# Conf t
<br/>
Router (Config)#hostname R2
<br/>
R2 (Config)#int se1/0
<br/>
R2 (Config)#ip add 10.0.0.2 255.0.0.0
<br/>
R2 (Config)#no sh
<br/>
R2 (Config-if)#int se1/1
<br/>
R2 (Config-if)#ip add 20.0.0.1 255.0.0.0
<br/>
R2 (Config-if)#clock rate 64000
<br/>
R2 (Config-if)#bandwidth 64
<br/>
R2 (Config-if)#no sh
<br/>
R2 (Config-if)#int fa0/0
<br/>
R2 (Config-if)#ip add 172.168.0.1 255.255.0.0
<br/>
R2 (Config-if)#no sh
<br/>
R2 (Config-if) #^Z
<br/>
R2#
<br/>
Router 3
<br/>
Router>Enable
<br/>
Router# Configure Terminal
<br/>
Router (Config)#hostname R3
<br/>
R3 (Config)# interface Se1/0
<br/>
R3 (Config-if)# ip address 0.0.0.2 255.0.0.0
<br/>
R3 (Config-if)#no sh
<br/>
R3 (Config-if)#int fa0/0
<br/>
R3 (Config-if)#ip add 125.168.0.1 255.0.0.0
<br/>
R3 (Config-if)#no sh
<br/>
R3 (Config-if)#do show ip int br
<br/>
R3 (Config-if)#^Z
<br/>

## Assign IP Address in All PC 
### Step 1 Click on PC , Go to Desktop and click , Click on IP configuration

<img src="https://i.imgur.com/tnjwJNY.png" height="100%" width="100%"> 
<br/>
<br/>

<br/>
<img src="https://i.imgur.com/IbzqI2J.png" height="100%" width="100%">
<br/>

## Enable Router
<br/>
R1>en
<br/>
R1#conf t
<br/>
R1(config)#router rip
<br/>
R1(config-router)#Network 192.168.0.0
<br/>
R1(config-router)#Net 10.0.0.0
<br/>
R1(config-router)# ctrl+z
<br/>
write
<br/>
R2
<br/>
R2>en
<br/>
R2#conf t
<br/>
R2(config)#router rip
<br/>
R2(config-router)#Network 10.0.0.0
<br/>
R2(config-router)#Net 172.168.0.0
<br/>
R2(config-router)#Net 20.0.0.0
<br/>
R2(config-router) #^Z
<br/>
write
<br/>
R3
<br/>
R3>en
<br/>
R3#conf t
<br/>
R3(config)#router rip
<br/>
R3(config-router)#Network 20.0.0.0
<br/>
R3(config-router)#Net 125.168.0.0
<br/>
R3(config-router) #^Z
<br/>
Write
<p/>
