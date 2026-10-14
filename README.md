# Techno Tech Multi-Branch Network (LAN & WAN)

A full network design for a company with four international branches, built and tested
in Cisco Packet Tracer. University group project, team of 4.

## Branches

| Branch | Designed by |
|--------|-------------|
| Malaysia | Ani |
| Singapore | **Hajrah (me)** |
| Australia | Aya |
| Japan | Hanan |
| WAN connecting all branches | **Hajrah (me)** |

## My part 1: Singapore branch (LAN)

- Extended star topology with a **3560 multilayer switch** at the core, so inter-VLAN routing happens on the switch with no router needed inside the LAN
- **5 departments, each on its own VLAN:** Marketing (10), Social Media (20), Customer Service (30), Admin (40) and IT Support (50)
- A separate **voice VLAN (60)** for IP phones, plus a native VLAN on trunk links and a management VLAN
- **VLSM subnetting**, so each department gets only the addresses it needs (from 20 to 60 hosts)
- **DHCP** gives addresses to devices automatically
- **WPA2-PSK** secures every department's wireless access point
- Console, VTY and privileged mode passwords set and encrypted on every device

## My part 2: WAN

- **Full mesh topology:** every branch has a direct link to every other branch, so one broken link never cuts off a branch
- **RIPv2** dynamic routing shares the LAN and WAN routes between branches
- After merging the four branch designs, I re-checked every branch and fixed the IP ranges and DHCP pools that had changed

## How to open it

1. Install **Cisco Packet Tracer** (free from Cisco Networking Academy)
2. Open `WAN_DESIGN.pkt`
