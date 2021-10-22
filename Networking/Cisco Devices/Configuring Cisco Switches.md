# Configuring Cisco Switches 
Figure 0x1


![image](https://user-images.githubusercontent.com/83109592/138515205-993367ee-0e86-4016-ab63-2a9dbc47b780.png)

# Basic Configuring 

**Switch>** enable

**Switch#** configure terminal

**Switch(config)#** no logging console

**Switch(config)#** hostname Switch_A

# Securing The Device

**Switch_A(config)#** line console 0

**Switch_A(config-line)#** password **<password>**
  
**Switch_A(config-line)#** login
  
**Switch_A(config-line)#** exec-timeout "<minutes>" 
  
**Switch_A(config-line)#** exit

**Switch_A(config)#** enable secret "<password>"


# Configuring Interfaces

# Configuring VLANS

# Configuring ACLs

# Configuring STP / RSTP

