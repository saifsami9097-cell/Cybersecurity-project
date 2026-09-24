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

5. Findings
DNS query generated:Yes 
DNS packets displayed: Yes 
Source IP: 192.168.52.128
Destination IP: 192.168.52.2
Domain queried: example.com
DNS response:Observed
6. Observation
During the DNS capture, Wireshark successfully captured DNS query and response packets between the Kali Linux VM (192.168.52.128) and the DNS server (192.168.52.2). The DNS query was generated using `nslookup example.com`, and the corresponding DNS response was observed. Initially, DNS communication timed out, but the lookup eventually returned IP addresses for example.com.

7. Conclusion

This activity was performed to understand DNS traffic analysis using Wireshark. The final result is based on the packets observed during the lab exercise.

