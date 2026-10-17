# Analyzing-HTTP-Traffic-with-Wireshark

## Lab Goal: 

To familiarize students with TCP traffic analysis via Wireshark, focusing on connection establishment, the three-way handshake, and the interpretation of key HTTP header fields and flags.

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

  ## 🦈Wireshark Profile

  A Wireshark configuration profile is a persistent, task-specific environment template that encapsulates customized user interface layouts, parsing parameters, and filtering logics.

*  Display Filters: Predefined query expressions designed to instantly isolate targeted telemetry.

*  Coloring Rules: Custom conditional formatting schemes that visually highlight packet categories or anomalous traffic patterns.

*  Column Layout: Tailored tabular schemas determining which packet metadata attributes are rendered in the interface.

*  Protocol Preferences: Granular decoding logic adjustments for specific OSI layer dissecting engines.

<img width="1920" height="991" alt="_WiFi 17_10_2026 19_30_56" src="https://github.com/user-attachments/assets/7048c97d-bc63-4167-9dbe-37e5a04488ed" />
<img width="1280" height="793" alt="_WiFi 17_10_2026 19_37_11" src="https://github.com/user-attachments/assets/629fce98-784f-4652-b055-0bd4831a337d" />
<img width="1920" height="991" alt="_WiFi 17_10_2026 19_40_25" src="https://github.com/user-attachments/assets/17a5a516-8542-430c-a0b7-1c45ae289f3c" />

## Initialize the Capture Interface:

Navigate to the Altoro Mutual web application via a browser and interact with the service (e.g., submitting login credentials or browsing pages) to initiate HTTP requests and responses.

* Initiate the Application Session: Launch a web browser and navigate to the Altoro Mutual training environment, then authenticate by submitting your credentials to generate active HTTP traffic.

* Execute the Packet Capture: Open Wireshark, select the active network interface, and start a live capture session to record ingress and egress packets transiting the local system.

* Apply a Display Filter: In the Wireshark filter toolbar, input the targeted display filter—such as tcp.port == 80 or http—to isolate unencrypted web traffic, parsing out extraneous network chatter to focus exclusively on port 80 application transactions.
  <img width="1920" height="1020" alt="Altoro Mutual - Personal - Microsoft​ Edge 17_10_2026 19_52_11" src="https://github.com/user-attachments/assets/2d3d8b7d-15aa-4325-bb27-39936ad0f35d" />
  <img width="1920" height="1020" alt="Altoro Mutual - Personal - Microsoft​ Edge 17_10_2026 19_52_38" src="https://github.com/user-attachments/assets/142eb630-30fb-4c10-8ca1-05593f1b9b14" />
<img width="1920" height="991" alt="Altoro Mutual - Personal - Microsoft​ Edge 17_10_2026 19_55_35" src="https://github.com/user-attachments/assets/a8cb3ca5-4fd8-4390-a5c6-7d8918c9ef12" />

## Payload Transmission: 

Unlike the GET method—which appends parameters to the Uniform Resource Identifier (URI)—POST encapsulates data within the message body of the HTTP request. This prevents sensitive or bulky payloads from appearing in browser history logs or server access logs (assuming transport-layer security is applied).
<img width="1920" height="991" alt="_WiFi 17_10_2026 20_17_15" src="https://github.com/user-attachments/assets/681b3496-1c6f-4084-8a05-3f8d5b2c74ae" />

FRAME
<img width="1920" height="991" alt="_WiFi 17_10_2026 20_23_09" src="https://github.com/user-attachments/assets/5ad185d3-3e7c-4dc9-b9f6-192d4e46b832" />

## Packet List Analysis

Reviewing the top pane of the Wireshark interface, which renders a tabular summary of every captured frame.
<img width="1920" height="991" alt="_WiFi 17_10_2026 20_46_49" src="https://github.com/user-attachments/assets/006a761e-484b-45d3-a255-aa00f3ca2d45" />

FOLLOW HTTP STREAM
<img width="1280" height="986" alt="_WiFi 17_10_2026 20_53_04" src="https://github.com/user-attachments/assets/9b39ea94-3a2e-42ca-8776-b1cdecba8d06" />


ETHERNET
<img width="1920" height="991" alt="_WiFi 17_10_2026 20_37_53" src="https://github.com/user-attachments/assets/83da5b43-eb2d-4aab-8530-9925ac17cc30" />

INTERNET PROTOCOL
<img width="1920" height="991" alt="_WiFi 17_10_2026 20_38_13" src="https://github.com/user-attachments/assets/72e055cc-1cb0-441c-826b-7f28696088d1" />

HTML
<img width="1920" height="991" alt="_WiFi 17_10_2026 20_38_26" src="https://github.com/user-attachments/assets/5fcc6828-0229-4ce0-bcd1-6fb9925c9394" />


NOTE -
CLIENT = THE RED COLOR REPRESENT THE COMMUNICATION FROM THE CLIENT SIDE.
SERVER = THE BLUE COLOUR REPRESENT THE COMMUNICATION FROM SERVER SIDE.


## Conclusion: Analyzing HTTP Traffic with Wireshark

Analyzing HTTP traffic with Wireshark gives you complete visibility into unencrypted web data, making it a powerful tool for troubleshooting and security auditing, while starkly highlighting the vulnerability of cleartext communications compared to modern HTTPS.













