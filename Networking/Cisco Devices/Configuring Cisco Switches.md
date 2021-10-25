# Configuring Cisco Switches 
Figure 0x1


![image](https://user-images.githubusercontent.com/83109592/138642340-d1014013-1856-463d-ac11-fbb9380b4b92.png)

# Most Common Basic Commands

**Switch>** enable

**Switch#** show running-configuration

**Switch#** copy running-config startup-config

**Switch#** configure terminal

# Securing The Device

 Securing The Console
 
  - Creating a console password

**Switch_A(config)#** line console 0

**Switch_A(config-line)#** password ***password***
  
  OPTION 1
  
**Switch_A(config-line)#** login 
  
  OPTION 2
  
**Switch_A(config-line)#** login local

**Switch_A(config-line)#** exec-timeout ***minutes*** 
  
**Switch_A(config-line)#** exit

 Securing The Command Line
 
  - Creating an Encrypted Enable Password 

**Switch_A(config)#** enable secret ***password***

**Switch_A(config)#** service password-encryption

 - Creating Local User Accounts w different Privleges 

**Switch_A(config)#** username ***name*** privilege ***0-15*** password ***password***

**Switch_A(config)#** privilege ***mode*** level ***2-14***

Securing Remote Access

 - Setting a Remote Auth Password

**Switch_A(config)#** line vty 0 15

**Switch_A(config-line)#** password ***password***

OPTION 1

**Switch_A(config-line)#** login

OPTION 2

**Switch_A(config-line)#** login local

**Switch_A(config-line)#** exec-timeout ***minutes***

 - Setting up SSH 

**Switch_A(config)#** ip domain-name ***Domain***

**Switch(config)#** hostname ***Name***

**Switch(config)#** crypto key generate rsa

**Switch(config)#** ip ssh version 2

# Configuring Physical Interfaces

**Switch(config)#** interface fa ***#/#/#***

Configuring Access Ports

**Switch(config-if)#** switchport mode access

**Switch(config-if)#** switchport access vlan ***#***

**Switch(config-if)#** no shutdown

Configuring Trunk Ports

**Switch(config-if)#** switchport mode trunk

**Switch(config-if)#** switchport trunk allowed vlan ***#,#,#***

**Switch(config-if)#** no shutdown

# Configuring VLANS

Creating VLANs (Broadcast Domains)

**Switch(config)#** vlan ***#***

**Switch(config-vlan)#** name ***Name***

Creating VLANs (Virtual Logical Interfaces)

**Switch(config)#** interface vlan ***#***

**Switch(config-if)#** description ***Name of VLAN***

**Switch(config-if)#** ip address ***dhcp/A.B.C.D***

# Configuring Port Channels

Creating Port Channels

**Switch(config)#** interface port-channel ***#***

Adding Interfaces to Port Channel Groups

**Switch(config)#** interface fa ***#/#/#***

**Switch(config-if)#** channel-group #

**Switch(config-if)#** 

# Configuring LACP

# Configuring ACLs

# Configuring STP / RSTP

