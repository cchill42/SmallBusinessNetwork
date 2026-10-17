Switch configuration:
- enable a secret password (247472)
- enable password encryption
- secured console with same password
- On VLAN 99, has IP address 192.168.99.2
	- Also has default gateway 192.168.99.1
- domain name business.local
- 1024-bit RSA key and using SSH v1.99
	- SSH version 2

Router config:
- hostname SB_ROUTER
- enable a secret password (247472)
- enable password encryption
- secured console with same password
- Subinterfaces on switch interface
	- g0/0.10 - MANAGEMENT_GATEWAY
	- g0/0.20 - POS_GATEWAY
	- g0/0.30 - GUEST_WIFI_GATEWAY
	- g0/0.99 - NETWORK_MANAGEMENT_GATEWAY
- DCHP Pools
	- First 20 addresses are excluded
	- Excluding network management
	- each one follows subnet 192.168.XX.0 255.255.255.0 template

VLAN configuration:
- 10 - MANAGEMENT
- 20 - POS
- 30 - GUEST_WIFI
- 99 - NETWORK_MANAGEMENT

Interface Ranges (Switch)
- fe0/1-4 - GUEST_WIFI
- fe0/5-9 - MANAGEMENT
- fe0/10-14 POS