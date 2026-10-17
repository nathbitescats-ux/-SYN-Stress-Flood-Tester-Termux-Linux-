

# 𝗗𝗢𝗦 𝗦𝗖𝗥𝗜𝗣𝗧 ( 𝗗𝗘𝗡𝗜𝗔𝗟 𝗢𝗙 𝗦𝗘𝗥𝗩𝗜𝗖𝗘 ) 

A lightweight, high-performance raw socket SYN flood tool written in Python. It is designed for network engineers and security researchers to test the resilience of their own infrastructure against transport-layer resource exhaustion. By crafting raw IP and TCP headers with spoofed source addresses, it rapidly fills a target's connection table with half-open connections (SYN_RECV state), allowing operators to verify if their SYN-cookie defenses, load balancers, and firewall rate-limiting are functioning correctly under load.

⚖️ Legal Disclaimer & Educational Use:
This script is provided strictly for educational purposes and authorized stress testing. It is intended to be used only on infrastructure you own or have explicit, written permission to test. Running this tool against public targets, third-party networks, or infrastructure you do not control is illegal under anti-cybercrime laws (such as the Philippine RA 10175) and can result in severe criminal penalties. The author assumes no liability for misuse.

---

📋 Instructions

Prerequisites:
Because this tool uses raw sockets to spoof IP addresses, it requires root privileges. On Termux, you must have a rooted device and use tsu.

1. Install Python (if not already installed):
   ```bash
   pkg install python
   ```
2. Save the script:
   Create a file named syn_flood.py and paste the code provided below into it. You can use a text editor like nano (pkg install nano).

3. Execute the tool:
   Gain root access in Termux, then run the script with the target IP, port, and duration (in seconds) as arguments.
   ```bash
   tsu
   python syn_flood.py <TARGET_IP> <PORT> <DURATION>
   ```
   Example: python syn_flood.py 192.168.1.100 80 15 (runs for 15 seconds).

---