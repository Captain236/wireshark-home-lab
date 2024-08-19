# Network Traffic Analysis with Wireshark on Linux
## Introduction
Network traffic analysis is a crucial skill for cybersecurity professionals. It involves capturing, inspecting, and understanding the packets of data that travel across a network. Wireshark is a powerful tool that allows users to capture and analyze network traffic in real-time. This lab will guide you through the process of using Wireshark on a Linux system to analyze network traffic, identify potential security issues, and understand network protocols.

## Skill Learned
- Understand the concept of network traffic analysis
- deep understanding of wireshark tool and it's features
- Captured Network Traffic
- Used Wireshark filters to narrow down and focus on specific types of traffic.
- Analyzed HTTP Traffic
- gets hands on wireshark tool.

## Exercise 1: Sniffing HTTP Traffic
# objective :- In this excercise I have performed the HTTP traffic analysis and sniff the login password of the http website 
# step 1 :- open the linux terminal and type wirehsrak to begin/open the wireshark window![kali-linux-2024 2-vmware-amd64 - VMware Workstation 17 Player (Non-commercial use only) 8_19_2024 11_13_56 AM](https://github.com/user-attachments/assets/36e2bdf0-6481-4859-b2fa-c26a946913a1)
# step 2 :- select the interface like(eth0,wifi,wlan0) and begin the packet analyzing .
![kali-linux-2024 2-vmware-amd64 - VMware Workstation 17 Player (Non-commercial use only) 8_19_2024 11_34_37 AM](https://github.com/user-attachments/assets/638ab06c-3eed-420f-a795-ded52be2452c)
# step 3 :- Open the browser and search for (test.php) and open the website . In left side click on the signup and enter any random login password on the login password field and after that click login. ![kali-linux-2024 2-vmware-amd64 - VMware Workstation 17 Player (Non-commercial use only) 8_19_2024 11_35_51 AM](https://github.com/user-attachments/assets/25f867c4-0cdb-433f-9bdb-6656c576221a)
# step 4 :- Now, the on the wireshark window click on stop capture button .
# step 5 :- In the filter field type (http.request.method == POST) to see the further details. ![kali-linux-2024 2-vmware-amd64 - VMware Workstation 17 Player (Non-commercial use only) 8_19_2024 11_38_23 AM](https://github.com/user-attachments/assets/722eba5c-7f4a-4269-b4a9-615d6a4bf0b1)
## step 6 :- after that click on the edit and click on "find packet" and select (string from drop down option) click (packet list) click (narrow and wide and select the narrow(UTF-8/ASCII) from drop down option.In the field next to the string type "pwd" and click the find button.
![kali-linux-2024 2-vmware-amd64 - VMware Workstation 17 Player (Non-commercial use only) 8_19_2024 11_39_56 AM](https://github.com/user-attachments/assets/70b10194-f75e-4f23-8a1d-5f63bdcaaac9)
# result :- Wireshark now display the sniff password from the captured packet .
![kali-linux-2024 2-vmware-amd64 - VMware Workstation 17 Player (Non-commercial use only) 8_19_2024 11_48_36 AM](https://github.com/user-attachments/assets/297682ef-253a-445a-a4fd-4287c32ccc8e)






