 NS-001: DNS Traffic Analysis

 1. Project Information

Project: Network Traffic Analysis Using Wireshark
Project ID: NS-001
Operating System: Kali Linux
Network Interface: eth0
Tool: Wireshark 4.4.4

2. Objective

To capture and analyze DNS traffic using Wireshark and understand how DNS queries and responses are exchanged over a network.

3. Activity Performed

1. Opened Wireshark in the Kali Linux virtual machine.
2. Started packet capture on the eth0 interface.
3. Generated a DNS lookup using `nslookup`.
4. Applied the DNS display filter in Wireshark.
5. Checked the captured packets for DNS queries and responses.

4. Display Filter Used

dns
Additional filter:
udp.port == 53

6. Findings

DNS query generated:Yes ;
DNS packets displayed: Yes ; 
Source IP: 192.168.52.128 ;
Destination IP: 192.168.52.2 ;
Domain queried: example.com ;
DNS response:Observed ;

8. Observation

During the DNS capture, Wireshark successfully captured DNS query and response packets between the Kali Linux VM (192.168.52.128) and the DNS server (192.168.52.2). The DNS query was generated using `nslookup example.com`, and the corresponding DNS response was observed. Initially, DNS communication timed out, but the lookup eventually returned IP addresses for example.com.

9. Conclusion

This activity was performed to understand DNS traffic analysis using Wireshark. The final result is based on the packets observed during the lab exercise.

TCP Traffic Analysis

Test Activity: Generated HTTP traffic using curl http://example.com.

| Handshake Packet | Source IP      | Destination IP |
| ---------------- | -------------- | -------------- |
| SYN              | 192.168.52.128 | 104.20.23.154  |
| SYN, ACK         | 104.20.23.154  | 192.168.52.128 |
| ACK              | 192.168.52.128 | 104.20.23.154  |

Observation

Wireshark captured TCP handshake packets generated during the HTTP request. The SYN packet was sent from the Kali Linux VM to the remote server. The server replied with a SYN-ACK packet, and Kali sent an ACK packet to complete the handshake.

Conclusion

The TCP 3-way handshake was successfully observed using Wireshark. This practical demonstrated how TCP establishes a connection before data transmission and helped identify the source and destination IP addresses involved in the communication.

UDP Packet Analysis

Objective: To capture and analyze UDP packets using Wireshark and identify their source and destination IP addresses and port numbers.

Tool Used: Wireshark
Network Interface: eth0
Test Activity: DNS lookup using `nslookup example.com`

Packet Details

| Parameter              | Observed Value |
| ---------------------- | -------------- |
| Frame Number           | 26             |
| Protocol               | UDP            |
| Source IP Address      | 192.168.52.128 |
| Destination IP Address | 192.168.52.2   |
| Source Port            | 55663          |
| Destination Port       | 53             |
| Packet Size            | 71 bytes       |

Observation

Wireshark captured a 71-byte UDP packet on the eth0 interface. The packet was transmitted from the Kali Linux VM (192.168.52.128) to the DNS server (192.168.52.2). The source port was 55663, while the destination port was 53, which is commonly used for DNS communication.

Conclusion

The UDP packet analysis demonstrated how DNS queries can be transmitted using UDP. Wireshark helped identify packet-level details, including IP addresses, port numbers, and frame size. This exercise improved practical understanding of UDP communication and network traffic analysis.

ICMP Traffic Analysis

Objective: To analyze ICMP packets and observe network connectivity using Wireshark.

Tool Used: Wireshark
Network Interface: eth0
Test Activity: Ping test to 192.168.52.2 using Kali Linux.

 Packet Details

| Parameter      | Echo Request     | Echo Reply     |
| -------------- | ---------------- | -------------- |
| Frame Number   | 12               | 13             |
| Source IP      | 192.168.52.128   | 192.168.52.2   |
| Destination IP | 192.168.52.2     | 192.168.52.128 |
| Packet Size    | 98 bytes         | 98 bytes       |
| ICMP Type      | 8 (Echo Request) | 0 (Echo Reply) |
| ICMP Code      | 0                | 0              |

 Observation

Wireshark captured an ICMP Echo Request from the Kali Linux VM to 192.168.52.2, followed by an ICMP Echo Reply from the destination. Both packets were 98 bytes in size. The reply indicates that the destination responded to the ping request.

 Conclusion

The ICMP traffic analysis demonstrated successful request-and-reply communication between the Kali Linux VM and the destination. Wireshark helped identify ICMP packet types, source and destination IP addresses, and packet sizes.

HTTP Traffic Analysis

Objective: To capture and analyze HTTP traffic using Wireshark.

Tool Used: Wireshark
Network Interface: eth0
Test Activity: Generated HTTP traffic using `curl http://neverssl.com`.

 Packet Details

| Parameter          | Observed Value |
| ------------------ | -------------- |
| Frame Number       | 68             |
| Protocol           | HTTP over TCP  |
| Source IP          | 34.223.124.45  |
| Destination IP     | 192.168.52.128 |
| Source Port        | 80             |
| Destination Port   | 36820          |
| TCP Payload Length | 1661 bytes     |
| Content Type       | text/html      |

Observation

Wireshark captured HTTP traffic from the remote web server to the Kali Linux VM. The packet contained reassembled TCP data, including 131 lines of HTML content from the NeverSSL webpage. The captured content was readable, demonstrating that plain HTTP does not encrypt webpage data.

Conclusion

The HTTP traffic analysis demonstrated how Wireshark can capture and inspect web communication. The practical helped identify IP addresses, TCP ports, and readable HTML content transmitted over HTTP.
