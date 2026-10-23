# Wireshark ICMP Packet Analysis

## 1. Objective

Understand how ICMP Echo Request and Echo Reply packets work and learn how to inspect network packets using Wireshark.

## 2. Lab Environment

- Operating system: Kali Linux
- Packet analysis tool: Wireshark
- Network interface: wlan0
- Traffic generation tool: ping
- Test destination: 1.1.1.1

## 3. Procedure

1. Open Wireshark.
2. Select the `wlan0` network interface.
3. Start capturing packets.
4. Generate test traffic using `ping -c 4 1.1.1.1`.
5. Apply the display filter `icmp`.
6. Select an ICMP Echo Request packet.
7. Inspect the Ethernet, IPv4, and ICMP fields.
8. Compare the request with its corresponding reply.

## 4. Packet Observations

Record the values from your actual packet capture.

- Source IP address: `192.168.0.5`
- Destination IP address: `1.1.1.1`
- IP protocol: ICMP (Protocol 1)
- ICMP message: Echo Request
- ICMP type: 8
- ICMP code: 0
- IPv4 header length: 20 bytes
- IPv4 total length: 84 bytes

Verify these values against your capture before publishing.

## 5. Analysis

An ICMP Echo Request is commonly used to test network reachability. The destination may respond with an ICMP Echo Reply.

Wireshark displays the Ethernet header, IPv4 header, and ICMP message details. ICMP does not use TCP or UDP port numbers.

A successful reply indicates that the destination responded to the request, but it does not prove that every service on the destination is reachable.

## 6. Evidence
Wireshark ICMP Packet Capture




## 7. What I Learned

- How to capture network traffic in Wireshark.
- How to filter ICMP packets.
- How to identify IP addresses and ICMP message types.
- How to distinguish an Echo Request from an Echo Reply.

## 8. Conclusion

This lab helped me understand how ICMP can be used for basic network troubleshooting and how Wireshark reveals the structure of captured packets.
