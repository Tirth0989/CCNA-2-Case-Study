# CCNA 2 Case Study — XYZ Legal Solutions

This repository contains a Routing and Switching Essentials case study for a
small legal firm. The network serves Sales, IT, Administration, and HR across
two office floors and is designed around performance, reliability, and
scalability.

## Repository contents

| Path | Description |
| --- | --- |
| [`packet-tracer/FINAL PHYSICAL.pkt`](packet-tracer/FINAL%20PHYSICAL.pkt) | Cisco Packet Tracer topology and device configuration |
| [`docs/Case_Study_Document2.pdf`](docs/Case_Study_Document2.pdf) | Completed case-study report, design decisions, command journal, and troubleshooting notes |
| [`docs/Running-config.pdf`](docs/Running-config.pdf) | Captured running configurations for the router and switches |
| [`Tirth CCNA2.zip`](Tirth%20CCNA2.zip) | Original submitted archive |

## Network overview

The design uses router-on-a-stick inter-VLAN routing, a core switch, two access
switches, VTP, LACP EtherChannel, spanning-tree tuning, DHCP for IPv4 and IPv6,
and NAT/PAT for Internet access.

| VLAN | Department | IPv4 subnet | IPv6 prefix |
| ---: | --- | --- | --- |
| 5 | Sales | `192.168.7.0/28` | `2001:1111:7:1::/64` |
| 10 | IT | `192.168.7.16/29` | `2001:1111:7:2::/64` |
| 15 | Administration | `192.168.7.24/29` | `2001:1111:7:3::/64` |
| 20 | HR | `192.168.7.32/30` | `2001:1111:7:4::/64` |

## Requirements

- Cisco Packet Tracer to open and simulate the `.pkt` file
- A PDF reader for the report and captured configurations

## Getting started

1. Clone or download this repository.
2. Open `packet-tracer/FINAL PHYSICAL.pkt` in Cisco Packet Tracer.
3. Review `docs/Case_Study_Document2.pdf` for the addressing plan, design,
   configuration steps, validation evidence, and troubleshooting analysis.
4. Use `docs/Running-config.pdf` as a reference for the device configurations.

Packet Tracer file compatibility depends on the application version. If the
topology cannot be opened, try the current Cisco Packet Tracer release.

## Validation

The archive and extracted files can be checked locally with:

```bash
unzip -t "Tirth CCNA2.zip"
sha256sum docs/*.pdf packet-tracer/*.pkt
```

Functional network validation should be performed in Packet Tracer using the
verification and connectivity tests described in the case-study report.
