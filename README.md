# vlans
So today i learnt about vlans and their purposes.
A vlan seperates broadcast domains ie a group of devices that receive a broadcast frame.
VLANS are configured on switch interfaces and all devices connected on those interfaces are under the same vlan.
Broadcast frames are not forwarded outside a vlan

## Access Switchport vlans
These are switchports that carry traffic of a single vlan, usually connects end hosts

### Below is an access port configuration
Nine PCs, One Multilayer Switch, One Router
<img width="1406" height="905" alt="image" src="https://github.com/user-attachments/assets/1f8917ea-fafb-4335-a09f-6b6f13dc6358" />
NOTE: for the default gateways i used the last usable host
