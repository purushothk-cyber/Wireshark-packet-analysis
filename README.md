# Task 5: Wireshark Network Traffic Analysis 

## Tools Used
- Kali Linux
- Wireshark (Network protocol analyzer)

## Objective
Capture live network traffic using Wireshark and analyze at least three different protocols to understand how data flows in a network.

## Steps Performed
1. Opened Wireshark on Kali Linux.
2. Selected the active network interface (`wlan0`, `eth0`, or similar).
3. Started live packet capture.
4. Generated traffic using:
   - `ping google.com` (ICMP + DNS)
   - Accessed `http://example.com` using Firefox and `curl` (HTTP + TCP)
5. Stopped the capture after around 1 minute.
6. Applied display filters to isolate:
   - `dns`
   - `http`
   - `tcp`

## Protocols Identified
| Protocol | Purpose | Observation |
|----------|---------|-------------|
| **DNS** | Resolving domain names to IP addresses | A-record query and response for `google.com` |
| **HTTP** | Web browsing | GET request and HTTP/1.1 200 OK response |
| **TCP** | Reliable data transfer | SYN, SYN-ACK, ACK handshake for connection setup |

## Packet Highlights
- **DNS**: Domain query to resolve hostnames like `google.com`.
- **HTTP**: Observed headers and status codes in request/response.
- **TCP**: Standard 3-way handshake sequence visible.

## Screenshots
Above are screenshots taken during packet capture and filtering:

- `dns_capture.png` – Filtered DNS traffic
- `http_capture.png` – HTTP GET request
- `tcp_handshake.png` – TCP 3-way handshake

To view, click on the image files in this repository or download them for reference.

## Files Included
- `network_capture.pcap` – Full capture file
- `report.txt` – Detailed protocol analysis
- `README.md` – Project documentation
- `*.png` – Screenshot images showing filtered packets

## Learnings
- Learned how to perform real-time traffic capture and filtering
- Understood the structure and behavior of common protocols
- Gained confidence using Wireshark for protocol-level analysis
