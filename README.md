<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Simulate and troubleshoot account lockouts by repeatedly entering incorrect passwords for a domain user until the account becomes locked. Then, unlock the account using Active Directory Users and Computers (ADUC).

- Disable and re-enable user accounts in ADUC to test how access is impacted on Client-1. Attempt logins before and after re-enabling to verify behavior.

- Observe security and system logs on the Domain Controller (DC-1) using Event Viewer, paying close attention to logs under:
Windows Logs > Security
Windows Logs > System
Look for event IDs related to login attempts, account lockouts, and user changes.

- Check client-side logs on Client-1 in Event Viewer to see how domain activity appears from the user's perspective. Focus on login attempts, lockouts, and Group Policy events.


<h2>Actions and Observations</h2>

-  Simulate and troubleshoot account lockouts by repeatedly entering incorrect passwords for a domain user until the account becomes locked. Then, unlock the account using Active Directory Users and Computers (ADUC).

  ![image](https://github.com/user-attachments/assets/aab8a1d9-f265-4c38-91d2-1e93f4dae1fc)
  ![image](https://github.com/user-attachments/assets/bbe6f892-b333-46fe-ad88-825dd9ad45ae)
  ![image](https://github.com/user-attachments/assets/0ded611d-53ee-497c-bdbc-8dddea819f12)


- Disable and re-enable user accounts in ADUC to test how access is impacted on Client-1. Attempt logins before and after re-enabling to verify behavior.

![image](https://github.com/user-attachments/assets/fa3871fd-919b-41a6-936f-9f38a54e8ba1)
![image](https://github.com/user-attachments/assets/c4b0d660-c2f6-42a8-9de9-2c9e36bb0c8d)
![image](https://github.com/user-attachments/assets/d3a04ce8-1ba0-4659-b131-fc12b645edfa)

- Observe security and system logs on the Domain Controller (DC-1) using Event Viewer, paying close attention to logs under:
Windows Logs > Security
Windows Logs > System
Look for event IDs related to login attempts, account lockouts, and user changes.

 ![image](https://github.com/user-attachments/assets/f963f7ca-de27-465e-a6a0-f088195cdfcc)

- Check client-side logs on Client-1 in Event Viewer to see how domain activity appears from the user's perspective. Focus on login attempts, lockouts, and Group Policy events.

 ![image](https://github.com/user-attachments/assets/c26b03ab-f469-4000-aace-32c13838c1ef)

