# Using-Wireshark---analyzing-web-browser-artifacts-email-header-analysis
# Name: SWETHA P
# Reg No: 212222100053
## AIM:
To use Wireshark to analyze web browser activities and inspect email headers from captured network traffic.

## DESIGN STEPS:
### Step 1:
Launch Wireshark and start capturing traffic on the appropriate network interface.

### Step 2:
Use filters like http, dns, or tcp.port == 80 to monitor web browser artifacts such as visited URLs, cookies, and user-agent strings.

### Step 3:
Apply filters like smtp, pop, or imap to locate and analyze email header details (e.g., sender, receiver, subject) from email communications.

## PROGRAM:
Wireshark Web and Email Traffic Filtering Steps

## OUTPUT:
## **A. Capturing Traffic in Wireshark**

1. Open Wireshark and start capturing on the active interface (Wi-
Fi/Ethernet).

2. Perform activities like opening a website or sending an email through a
client (e.g., Gmail via browser or Thunderbird).
3. Stop the capture once done.

![image](https://github.com/user-attachments/assets/aa316b69-316c-495d-926f-d11c3823a216)

### **Analyzing Web Browser Artifacts**
**Analyze Queries:**

- Filter: http
  ![image](https://github.com/user-attachments/assets/ca5513bb-cf33-4a94-ba74-68a3f46c8ab9)

- Filter: tcp
  ![image](https://github.com/user-attachments/assets/0eb05ec7-0769-430a-aaad-ac9cd331141d)

**Inspect HTTP GET/POST requests**

![image](https://github.com/user-attachments/assets/39fe12c9-53d1-4ad5-8d9c-5d84b516acf9)

**Follow TCP Stream to reconstruct page request flow:  Right-click a packet → Follow → TCP Stream.**

![image](https://github.com/user-attachments/assets/a2dcd3cb-b9eb-4fe6-a8db-75a0cd0a449f)

**Analyze dns Queries:**

- Filter: dns
- 
![image](https://github.com/user-attachments/assets/98dd7c75-346b-4bc9-a07a-1213d3e2c8db)

### Email Header Analysis
- **Apply relevant filters**
  ```
   For SMTP: tcp.port == 25 or 587
  ```
  
   ![image](https://github.com/user-attachments/assets/625d9c10-4174-49ed-aafd-52ee30395e2d)
       
- **Locate email data**
  
    Look for SMTP packets to see sender/receiver email addresses.
    Use "Follow TCP Stream" to view the full email headers and body if unencrypted.
  
- **Extract Email Header Fields**
   Analyze From, To, Subject, Date, Message-ID, and relay servers used in sending the email.
  
  ![image](https://github.com/user-attachments/assets/0ca76b9a-46d4-4ea7-879c-4723ed84982b)
     

## RESULT:
Web browser artifacts and email headers were successfully analyzed using Wireshark
