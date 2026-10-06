# vlans
So today i learnt about vlans and their purposes.
A vlan seperates broadcast domains ie a group of devices that receive a broadcast frame.
VLANS are configured on switch interfaces and all devices connected on those interfaces are under the same vlan.
Broadcast frames are not forwarded outside a vlan

## Access Switchport vlans
These are switchports that carry traffic of a single vlan, usually connects end hosts

### Below is an access port configuration
Nine PCs, One Switch, One Router
<img width="1406" height="905" alt="image" src="https://github.com/user-attachments/assets/1f8917ea-fafb-4335-a09f-6b6f13dc6358" />
<u>NOTE:</u> for the default gateways, i used the last usable host

## Trunk Switchport vlans
These are switchports that carry traffic of a multiple vlans, on on interface

### Below is an trunk port configuration
Eight PCs, Two Switches, One Router
<img width="2038" height="933" alt="image" src="https://github.com/user-attachments/assets/623eeb4f-5408-49ba-af7a-e89d50ee97e8" />
<u>NOTE:</u> for the default gateways, i used the last usable host

## Router on a Stick
Instead of having multiple connections for each vlan on separate interfaces, we can use one connections with multiple sub-interfaces as default gateways.
Below i used sub-interface G0/0.10 FOR VLAN 10, G0/0.20 FOR VLAN 20, G0/0.30 FOR VLAN 30
<img width="1747" height="906" alt="image" src="https://github.com/user-attachments/assets/d67478e7-129a-4a9c-83ea-ba5855b02b7e" />

## Multilayer Switch
Multilayer Switch also know as Layer 3 switch can be configured to perform inter vlan routing, this eliminates the need for a router. That would require us to know what is a SVI Switch Virtual Interface and what it does, A SVI is a virtual interface where one can assign an IP address to in a Layer 3 Switch.
<u>NOTE:</u> The has to be enabled for routing using the command <b>ip routing</b> in configuration mode
<img width="1400" height="816" alt="image" src="https://github.com/user-attachments/assets/ad557e82-735d-465b-a536-da365be880f5" />
<b>AND HOW TO CONFIGURE SVI</b>
<img width="471" height="231" alt="image" src="https://github.com/user-attachments/assets/0b5d4861-da2b-438b-9791-181376124467" />
<u>NOTE:</u> SVI are shutdown by default use <b>no shutdown</b> to enable them
