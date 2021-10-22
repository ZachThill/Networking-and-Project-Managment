# Configuring Cisco Switches 
Figure 0x1


![image](https://user-images.githubusercontent.com/83109592/138515205-993367ee-0e86-4016-ab63-2a9dbc47b780.png)

# Basic Configuring 

Setting a Hostname

**Switch>** enable

**Switch#** configure terminal

**Switch(config)#** no logging console

**Switch(config)#** hostname ***Name***

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
 
  - Creating an encrypted enable password 

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

# Configuring Interfaces

# Configuring VLANS

# Configuring Port Channels

# Configuring LACP

# Configuring ACLs

# Configuring STP / RSTP

