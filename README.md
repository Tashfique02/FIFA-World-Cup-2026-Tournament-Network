# FIFA-World-Cup-2026-Tournament-Network
A detailed network topology among some football nations.  
This project involves designing and implementing a complete network infrastructure in Cisco Packet Tracer for six team headquarters (Argentina, Brazil, England, France, Germany, and Spain) during the 2026 FIFA World Cup. The network simulates an independent but interconnected administrative backbone.

**Key Project Requirements:**

* **Topology Design:** A custom WAN architecture where France acts as a primary hub. It includes specific point-to-point connections, a shared Layer-2 switch for Brazil, Argentina, and France, and an alternative backup link between England and Germany. Each headquarters includes a local LAN with a switch, PCs, and a network printer.
* **IP Addressing (VLSM):** IPv4 subnetting using Variable Length Subnet Masking (VLSM) based on a specific `/16` base network (`15.47.0.0/16`, derived from a student ID). Subnets must accommodate specific user capacities ranging from 60 to 280 users per headquarters.
* **Routing Configuration:** A hybrid routing environment featuring:
* **RIPv2:** Dynamic routing between France, Brazil, and Argentina.
* **Static Routing:** Default static routes (Spain), recursive next-hop static routes (England), and directly attached static routes (Germany).
* **Floating Static Routes:** Configured failover paths between England and Germany to ensure connectivity if primary links to France fail.


* **Network Services:**
* **DHCP:** A mix of router-based DHCP (France serving multiple LANs) and dedicated server-based DHCP (England, Germany) for dynamic IP allocation.
* **DNS:** A centralized DNS server located in the France headquarters resolving all network domain names.
* **Web Servers:** Hosted in Brazil (`[www.brazil2026.com](https://www.brazil2026.com)`) and Germany (`[www.germany2026.com](https://www.germany2026.com)`).
* **Email Servers:** Hosted in Argentina and England with cross-domain communication capabilities.
