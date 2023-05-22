# computer-networks

## Task 1
![task 1](https://github.com/telman03/computer-networks/blob/main/img/1.png)

### Commands
- Switch> en
- Switch# conf t
#### Configure VLAN
- Switch(config)# vlan 10
- Switch(config-vlan)# exit
- Switch(config)# vlan 20
- Switch(config-vlan)# exit

#### Configure trunk port on switch:



- Switch(config)# interface fa0/5
- Switch(config-if)# switchport mode trunk 
- Switch(config-if)# switchport trunk allowed vlan 10-20
- Switch(config-if)# exit

#### Set ports to access mode & assign ports to VLAN


- Switch(config)# interface fastEthernet 0/1
- Switch(config-if)# switchport mode access 
- Switch(config-if)# switchport access vlan 10
- Switch(config-if)# exit
- Switch(config)# interface fastEthernet 0/2
- Switch(config-if)# switchport mode access
- Switch(config-if)# switchport access vlan 10
- Switch(config-if)# exit 
- Switch(config)# interface fastEthernet 0/3
- Switch(config-if)# switchport mode access
- Switch(config-if)# switchport access vlan 20
- Switch(config-if)# exit 
- Switch(config)# interface fastEthernet 0/4
- Switch(config-if)# switchport mode access
- Switch(config-if)# switchport access vlan 20
- Switch(config-if)# exit
- Router(config)#hostname A 
- A(config)# interface gigabitEthernet 0/0/0 
- A(config-if)# no shutdown 
- A(config-if)# exit

#### Create sub-interfaces, set 802.1Q trunking protocol and ip address on each sub-interface



- A(config)# interface gigabitEthernet 0/0/0.10
- A(config-subif)# no shutdown 
- A(config-subif)# encapsulation dot1Q 10
- A(config-subif)# ip address 192.168.1.1 255.255.255.0
- A(config-subif)# exit
- A(config)# interface gigabitEthernet 0/0/0.20
- A(config-subif)# no shutdown 
- A(config-subif)# encapsulation dot1Q 20
- A(config-subif)# ip address 172.168.1.1 255.255.255.0
- A(config-subif)# exit


## Task 2
![task 2](https://github.com/telman03/computer-networks/blob/main/img/2.png)

### Commands
- Switch> en
- Switch# conf t
#### Configure VLAN
- Switch(config)# vlan 10
- Switch(config-vlan)# exit
- Switch(config)# vlan 20
- Switch(config-vlan)# exit

#### Set ports to access mode & assign ports to VLAN


- Switch(config)# interface fastEthernet 0/1
- Switch(config-if)# switchport mode access
- Switch(config-if)# switchport access vlan 10
- Switch(config-if)# switchport nonegotiate
- Switch(config-if)# exit
- Switch(config)# interface fastEthernet 0/2
- Switch(config-if)# switchport mode access
- Switch(config-if)# switchport access vlan 10
- Switch(config-if)# switchport nonegotiate
- Switch(config-if)# exit
- Switch(config)# interface fastEthernet 0/3
- Switch(config-if)# switchport mode access
- Switch(config-if)# switchport access vlan 20
- Switch(config-if)# switchport nonegotiate
- Switch(config-if)# exit
- Switch(config)# interface fastEthernet 0/4
- Switch(config-if)# switchport mode access
- Switch(config-if)# switchport access vlan 20
- Switch(config-if)# switchport nonegotiate
- Switch(config-if)# exit


- Switch(config)# interface Vlan10
- Switch(config-if)# ip address 192.168.1.1 255.255.255.0
- Switch(config-if)# exit
- Switch(config)#interface Vlan20
- Switch(config-if)# ip address 192.168.2.1 255.255.255.0
- Switch(config-if)# exit

#### Don`t forget !!!
- Switch(config)# ip routing

## Task 3
![task 3 dhcp](https://github.com/telman03/computer-networks/blob/main/img/dhcp.png)
- [DHCP commands](https://github.com/telman03/computer-networks/blob/main/dhcp.txt)

## Task 4
![task 4 port security](https://github.com/telman03/computer-networks/assets/70106877/61a98bb8-4759-4743-a36d-f59b027b7b86)

How to Configure Port Security in Cisco Packet Tracer |

- Switch(config)#int fastEthernet 0/1
- Switch(config-if)#switchport mode access 
- Switch(config-if)#switchport port-security mac-address sticky 
- Switch(config-if)#switchport port-security maximum 1
- Switch(config-if)#switchport port-security violation shutdown 


- Switch(config)#int fastEthernet 0/2
- Switch(config-if)#switchport mode access 
- Switch(config-if)#switchport port-security mac-address sticky 
- Switch(config-if)#switchport port-security maximum 1
- Switch(config-if)#switchport port-security violation shutdown 

To see the :
- Switch#show port-security 

- Switch#show port-security interface fastEthernet 0/1
