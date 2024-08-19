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

## Tools
- Virtual machine (VMware) and Linux.
- Wireshark installed in Linux.
- internet connection .

# Exercise 1: Sniffing HTTP Traffic
## objective :- In this excercise I have performed the HTTP traffic analysis and sniff the login password of the http website 
# step 1 :-
- open the linux terminal and type wirehsrak to begin/open the wireshark window![kali-linux-2024 2-vmware-amd64 - VMware Workstation 17 Player (Non-commercial use only) 8_19_2024 11_13_56 AM](https://github.com/user-attachments/assets/36e2bdf0-6481-4859-b2fa-c26a946913a1)
# step 2 :- 
- select the interface like(eth0,wifi,wlan0) and begin the packet analyzing .
![kali-linux-2024 2-vmware-amd64 - VMware Workstation 17 Player (Non-commercial use only) 8_19_2024 11_34_37 AM](https://github.com/user-attachments/assets/638ab06c-3eed-420f-a795-ded52be2452c)
# step 3 :- 
- Open the browser and search for (test.php) and open the website . In left side click on the signup and enter any random login password on the login password field and after that click login. 
![kali-linux-2024 2-vmware-amd64 - VMware Workstation 17 Player (Non-commercial use only) 8_19_2024 12_16_45 PM](https://github.com/user-attachments/assets/147bbb13-bd04-458a-8d48-acd5c3193b43)
# step 4 :- 
- Now, the on the wireshark window click on stop capture button .
# step 5 :- 
- In the filter field type (http.request.method == POST) to see the further details. ![kali-linux-2024 2-vmware-amd64 - VMware Workstation 17 Player (Non-commercial use only) 8_19_2024 11_38_23 AM](https://github.com/user-attachments/assets/722eba5c-7f4a-4269-b4a9-615d6a4bf0b1)
## step 6 :- 
- after that click on the edit and click on "find packet" and select (string from drop down option) click (packet list) click (narrow and wide and select the narrow(UTF-8/ASCII) from drop down option.In the field next to the string type "pwd" and click the find button.
![kali-linux-2024 2-vmware-amd64 - VMware Workstation 17 Player (Non-commercial use only) 8_19_2024 11_39_56 AM](https://github.com/user-attachments/assets/70b10194-f75e-4f23-8a1d-5f63bdcaaac9)
# result :- Wireshark now display the sniff password from the captured packet .
![kali-linux-2024 2-vmware-amd64 - VMware Workstation 17 Player (Non-commercial use only) 8_19_2024 11_48_36 AM](https://github.com/user-attachments/assets/297682ef-253a-445a-a4fd-4287c32ccc8e)



## Exercise 2 :- Applying Filters
# Objective: Used Wireshark filters to narrow down and focus on specific types of traffic.

## step 1 :-
- Open the linux terminal and type wireshark ![splunk 8_19_2024 12_10_28 PM](https://github.com/user-attachments/assets/ad885fd7-984a-4fff-ae41-bae406c8ff77)
- select the interface like(eth0,wlan0,wifi ect) and on the filter bar type ( host <your ip> && tcp port 80) to see the tcp packet .
- ![kali-linux-2024 2-vmware-amd64 - VMware Workstation 17 Player (Non-commercial use only) 8_19_2024 12_16_07 PM](https://github.com/user-attachments/assets/2df72f93-f6c2-44b1-ab3a-c85b2c020395)
## step2 :-
- open the browsre and type(test.php) and open the http website and in the login password field type the random login password
- ![kali-linux-2024 2-vmware-amd64 - VMware Workstation 17 Player (Non-commercial use only) 8_19_2024 12_16_45 PM](https://github.com/user-attachments/assets/3a0eecf8-7679-4396-8b20-03d2d8ce859d)

## step 3 :-
- In the filder bar type ip.addr== (your ip address) and tcp.port==80
  ![kali-linux-2024 2-vmware-amd64 - VMware Workstation 17 Player (Non-commercial use only) 8_19_2024 12_17_18 PM](https://github.com/user-attachments/assets/772b86fb-194e-4eb2-996e-d7ddebdca00f)
  - Now we can see the packets whch we captured

  ## step 4 :-
  - Now type (dns) on the filter bar to see  the dns packets.
    ![kali-linux-2024 2-vmware-amd64 - VMware Workstation 17 Player (Non-commercial use only) 8_19_2024 12_24_14 PM](https://github.com/user-attachments/assets/d685011c-5594-4779-926f-07a8b2293c75)
    - now search for (dns.flags.response == 0) to search for dns query.
      ![kali-linux-2024 2-vmware-amd64 - VMware Workstation 17 Player (Non-commercial use only) 8_19_2024 12_24_46 PM](https://github.com/user-attachments/assets/8237f969-99a1-4077-957c-1291faf39d1d)

      - Now type (dns.flags.response == 1 ) to search for dns response.
        ![kali-linux-2024 2-vmware-amd64 - VMware Workstation 17 Player (Non-commercial use only) 8_19_2024 12_24_54 PM](https://github.com/user-attachments/assets/ecbd740c-3631-4618-ab66-e50cecc0e538)
# result :-  Filtered list of packets that match the criteria specified in the filter bar.

## Conclusion :-
By completing these exercises, I have gained practical experience in capturing and analyzing network traffic using Wireshark on a Linux system. I have learned how to filter and examine packets, identify potential malicious activities, and extract files from network captures.











