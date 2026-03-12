# H3C-configs
### S5130

sys

local-user admin\
password simple 123123\
service-type http https
authorization-attribute user-role network-admin
authorization-attribute user-role network-operator

line vty 0 63
authentication-mode scheme
user-role network-admin
quit

line class vty
user-role network-operator

interface vlan-interface 1
ip address 192.168.1.100 24
quit

ip http enable
ip https enable

sa f

### S6520

sys

local-user admin
password simple 123123
service-type http https
authorization-attribute user-role network-admin
authorization-attribute user-role network-operator

line vty 0 63
authentication-mode scheme
user-role network-admin
quit

line class vty
user-role network-operator
quit

interface M-GigabitEthernet 0/0/0
ip address 192.168.1.100 24
quit

ip http enable
ip https enable

sa f
