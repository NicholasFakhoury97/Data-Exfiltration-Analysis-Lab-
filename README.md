# # Data Exfiltration Analysis Lab: Investigating PCAP Traffic
This lab involves analyzing a PCAP file to investigate suspicious network activity and identify data exfiltration. Examining traffic from a compromised host transferring files from a Samba server to an external location.

## Steps and Questions

### 1. Analyze the `network_activity.pcap` File
- Open the PCAP file with Wireshark.
- Use filters and tools to investigate the traffic.

![image](https://github.com/user-attachments/assets/874eb7c9-34d9-49ac-80be-6ef2bd719de1)

### 2. What is the IP address of the Samba server used to back up files?

**Explanation:**
1. **Identify High-Traffic IPs:** Look for IPs with high packet counts.
2. **Focus on TCP Traffic:** Filter by TCP traffic and port `445` (Samba).
3. **Inspect Communication:** Determine that IP `172.17.0.2` is the Samba server based on file requests.

![image](https://github.com/user-attachments/assets/aaef0df8-d063-4e06-9fa3-52b966fa2503)
![image](https://github.com/user-attachments/assets/0b4fd5cc-0a82-44ec-9928-7089a8821afa)
![image](https://github.com/user-attachments/assets/b82ad3c8-945f-4240-920b-44568106262f)

### 3. How many CSV files were downloaded from the Samba server?

**Explanation:**
1. **Search for CSV Files:** Use Wireshark’s Find function with `.csv`.
2. **Record File Names:** Note all CSV files found.

![image](https://github.com/user-attachments/assets/035c248d-68a5-45b6-8f1e-bb08a86946a8)
![image](https://github.com/user-attachments/assets/de648782-9054-42e6-a7db-7272cf431fc0)


### 4. What is the IP address of the host machine used to download the backup files?

**Explanation:**
1. **Identify Requests:** The IP making requests to the Samba server is the host machine.

![image](https://github.com/user-attachments/assets/ef72edf7-b02e-47c7-840a-a2d1419e470a)
![image](https://github.com/user-attachments/assets/497a691e-e7b9-40ea-8508-9c50d48b8fa7)

### 5. What protocol was used to exfiltrate data to the external server?

**Explanation:**
1. **Filter Traffic:** Look for FTP or other relevant protocols.
2. **Verify Protocol:** Check for login and file transfers to identify the protocol.

![image](https://github.com/user-attachments/assets/0e8f8ac8-73e8-43c0-9770-ff2c0b0470d6)
![image](https://github.com/user-attachments/assets/18c7543e-94dc-4079-877c-cb5ddb7fe0a1)

### 6. What is the IP address of the external server?

**Explanation:**
1. **Identify Communication:** The external server is the IP communicating with the host.

![image](https://github.com/user-attachments/assets/dbd7274e-5256-4156-b1ed-e955f4611823)
![image](https://github.com/user-attachments/assets/5477b43f-fa49-411e-959a-26f347d45dfc)

### 7. What username was used to authenticate to the external server?

**Explanation:**
1. **Search for Username:** Look in the authentication packets.

![image](https://github.com/user-attachments/assets/eea84d04-4738-41e5-87ab-6fb7db6897ba)
![image](https://github.com/user-attachments/assets/b444a403-4106-4018-b42a-79e359f319f0)

### 8. What password was used to authenticate to the external server?

**Explanation:**
1. **Locate Password:** Find it within the authentication packets.

![image](https://github.com/user-attachments/assets/6d7b82e3-1619-4e45-a4ca-6bc0b552fea3)
![image](https://github.com/user-attachments/assets/259d340f-188c-433c-9e53-0bee7957df1f)

### 9. What file name was used to transfer the compressed CSV files to the external server?

**Explanation:**
1. **Find File Name:** Search for the file name in the packets.

![image](https://github.com/user-attachments/assets/f0bbb960-807c-40b7-b24f-e4c3d1ee06ad)
![image](https://github.com/user-attachments/assets/5f7405fc-fb07-4445-91a9-82eb7a53608c)


## Purpose

The goal of this lab is to practice network traffic analysis and identify data exfiltration techniques.

## Tools Used

- **Wireshark**: For PCAP analysis.
- **tcpdump**: Optional for packet capture.

## Conclusion

Completed the lab by answering the questions based on my analysis of the PCAP file.

## Additional Resources

- [Wireshark Documentation](https://www.wireshark.org/docs/)
- [tcpdump Documentation](https://www.tcpdump.org/manpages/tcpdump.1.html)

## Certification
![image](https://github.com/user-attachments/assets/fd3e04bb-a829-47c8-aee5-03737dc8f343)




