# Cisco IOS Command Mode Basics

**User Exec Mode** - **Router>**

The moment you boot your Cisco Networking device, you will begin in what's called **User Exec Mode**. Your access to viewing and changing anything will be very limited. Some of the commands you can use in this mode are: 
 - *ping*
 - *show (Limited)*
 - *enable*
 - *etc...* 
 
 **Privileged Exec Mode** - **Router#**
 
After typing the command **enable** and type in your password if one is configured, you will enter what is called **Privileged Exec Mode**. This mode still can't change anything about the current configuration but can show you a lot more about the device than **User Exec Mode**. Some commands you can use in this mode are as follows:
  - *ping*
  - *show (all)*
  - *configure terminal*
  - *copy run start*
  - *reload*
  - *etc...*

**Configuration Mode** - **Router(Config)#**

After typing in the command **conf t**, you will now be in **Global Config Mode**. From here, you will have access to configure anything and everything about the device from its hostname to the way it works. Some examples of commands you can type from here are: 
 - *interface*
 - *ip*
 - *hostname*
 - *etc...*

*Interface Configuration* 

After typing, **interface** followed by whatever interface you want to configure ***(fa 0/# / Gi 0/#)***,
*Router Configuration*

*Line Configuration*

*
 ![image](https://user-images.githubusercontent.com/83109592/130335827-ce3c1108-3758-47d5-8f4c-9d62551cf738.png)

