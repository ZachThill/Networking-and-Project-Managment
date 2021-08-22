# Configuring Cisco Routers with CLI 
**Authored by Zachary Thill - IT Student Project Leader @ RRCC**

Figure 0x1

![image](https://user-images.githubusercontent.com/83109592/130343285-dd587231-ab58-471d-a5ae-48c21be514e0.png)


# Configuring Hostname / Console
**Router> enable**  

**Router# conf t**  

**Router(config)# no logging console**  

**Router(config)# line console 0**

**Router(config-line)# password _____________**

**Router(config-line)# login** 

**Router(config-line)# exit**  

**Router(config)# hostname ____________**  

**Router(config)# exit** 

**Router# copy run start** 

# Configuring Interfaces 

**Router(config)# interface Gi0/1**  

**Router(config-if)# description LAN**  

**Router(config-if)# ip address 192.168.1.1 255.255.255.0** 

**Router(config-if)# ip nat inside**  

**Router(config-if)# no shutdown** 

**Router(config-if)# exit** 

**Router(config)# interface Gi0/0** 

**Router(config-if)# description WAN** 

**Router(config-if)# ip address 91.223.224.42 255.255.240.0**

**Router(config-if)# ip nat outside** 

**Router(config-if)# no shutdown** 

**Router(config-if)# exit** 

**Router(config)# exit**

**Router# copy run start**  

# Configuring DHCP Pools

**Router# conf t**   

**Router(config)# service dhcp** 

**Router(config)# ip dhcp excluded-address 192.168.1.1 192.168.1.10**

**Router(config)# ip dhcp pool vlan1** 

**Router(config-dhcp)# network 192.168.1.0 255.255.255.0** 

**Router(config-dhcp)# default-router 192.168.1.1** 

**Router(config-dhcp)# dns-server 1.1.1.1**  

**Router(config-dhcp)# exit** 

**Router(config)# exit**  

**Router# copy run start**

# Configuring NATing 

**Router(config)# ip nat inside source list 1 interface Gi0/0 overload** 

**Router(config)# access-list 1 permit 192.168.1.0 0.0.0.255**

**Router(config)# ip route 0.0.0.0 0.0.0.0 91.223.224.42**

# Configuring Dynamic Routing - EIGRP 

# Configuring Dynamic Routing - OSPF  

# Configuring Dynamic Routing - RIPv1 / RIPv2 

# Configuring Static Routing 

# Configuring "Router on a Stick" (Sub-Interfaces)

