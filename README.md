# Analyzing-HTTP-Traffic-with-Wireshark

## Lab Goal: 

To familiarize students with TCP traffic analysis via Wireshark, focusing on connection establishment, the three-way handshake, and the interpretation of key TCP header fields and flags.

## 🛠️ Lab Setup

Wireshark (latest stable version)
http://altoro.testfire.net/(for Testing purpose)

## 📘 What is Wireshark?

Wireshark is an open-source tool that captures and analyzes network traffic, allowing you to inspect data packets flowing in and out of a system in real time or from saved files.

## 🛡️ Wireshark Use Cases for SOC Analysts

* Forensic Detective Work: When a security breach happens, analysts comb through the packet captures to trace exactly how an attacker moved through the network or communicated with their command server.

* Hunting Digital Footprints: Analysts use it like a digital microscope to isolate malware traffic and pull out hard evidence—such as malicious IP addresses, domain names, or downloaded files—for threat intelligence.

* Proactive Threat Hunting: Instead of waiting for an alarm, analysts proactively scan network logs to sniff out hidden threats, like secret data-exfiltration tunnels or unauthorized remote access tools.

* Root-Cause Troubleshooting: When a critical service goes down or acts strangely, it helps pinpoint whether the root cause is a misconfigured protocol, dropped packets, or unexpected network latency.

  ## Launch the Wireshark Application:

   Initialize the binary or daemon with administrative or root privileges to ensure proper access to the underlying network interface controllers (NICs).
  <img width="1920" height="991" alt="The Wireshark Network Analyzer 17_10_2026 19_09_48" src="https://github.com/user-attachments/assets/f53b91f7-8f1a-415f-aa75-d44354ca24d2" />


