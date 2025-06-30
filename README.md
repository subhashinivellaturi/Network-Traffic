Task 5 – Network Traffic Capture Using Wireshark

##  Objective
To capture live network traffic using Wireshark in Kali Linux and analyze various network protocols.

---

##  Steps Followed

1. Installed Wireshark on Kali Linux.
2. Started capture on the active network interface.
3. Generated traffic by:
   - Pinging websites (`ping google.com`)
   - Accessing HTTP websites (`curl http://example.com`)
4. Captured packets for ~1 minute.
5. Applied filters to view different protocols (`dns`, `tcp`, `arp`, `http`, `icmp`).
6. Saved each filtered capture as a `.pcap` file.
7. Transferred `.pcap` files to Windows using a shared folder.
8. Prepared this report and GitHub submission.

---

##  Files Included

| File Name    | Protocol Captured | Description                        |
|--------------|--------------------|------------------------------------|
| `dns.pcap`   | DNS                | Domain name resolution queries     |
| `arp.pcap`   | ARP                | MAC address resolution in LAN      |
| `tcp.pcap`   | TCP                | TCP handshakes and connections     |
| `http.pcap`  | HTTP               | Browsing traffic to unencrypted websites |
| `icmp.pcap`  | ICMP               | Ping (Echo request/reply) packets  |

---

##  Protocols Identified

1. DNS (Domain Name System) – Resolves domain names to IP addresses.
2. ARP (Address Resolution Protocol) – Maps IP addresses to MAC addresses in local network.
3. TCP (Transmission Control Protocol) – Handles reliable communication between hosts.
4. HTTP (HyperText Transfer Protocol) – Used for loading web pages.
5. ICMP (Internet Control Message Protocol) – Used by `ping` for network diagnostics.

---

## Summary of Findings and Packet Details

During the packet capture session, I analyzed and filtered multiple types of network traffic using Wireshark:

- DNS.pcap : Captured 12 DNS query and response packets. These included name resolution requests to `google.com` and `example.com`, mostly using port 53 (UDP).
  
- ARP.pcap : Captured 6 packets showing local MAC-IP resolution in my network. This included ARP requests like “Who has 192.168.1.1? Tell 192.168.1.2”.
  
- TCP.pcap : Observed over 30 TCP packets including SYN, ACK, and FIN flags indicating connection establishment and closure. Most traffic was over ports 80 and 443.
  
- HTTP.pcap : Contained GET requests to websites like `example.com` and responses with HTTP status codes (e.g., 200 OK).
  
- ICMP.pcap : Captured echo request and echo reply packets while running `ping google.com`. Total of 10 ICMP packets, confirming host reachability.

These captures show successful identification of multiple protocols and clear understanding of how to filter and analyze them using Wireshark.

---

##  Tools Used

- Kali Linux (VirtualBox)
- Wireshark
- Terminal tools (`ping`, `curl`)
- Shared Folders to move files to Windows

---

## Conclusion

Successfully captured and filtered multiple types of network traffic using Wireshark. Learned to identify different network protocols and analyze packet details in a `.pcap` file. Gained hands-on experience in protocol filtering and packet inspection.

---

