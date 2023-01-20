# computer-networks

## Task 1
![example 1](C:\Users\telma\Downloads\1.png)

### Commands
- Switch> en
- Switch# conf t
- Switch(config)# vlan 10
- Switch(config-vlan)# exit
- Switch(config)# vlan 20
- Switch(config-vlan)# exit
- Switch(config)# interface fa0/5
- Switch(config-if)# switchport mode trunk 
- Switch(config-if)# switchport trunk allowed vlan 10-20
- Switch(config-if)# exit