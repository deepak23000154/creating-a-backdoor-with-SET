# creating-a-backdoor-with-SET
creating a backdoor with SET - Ethical Hacking Techniques course

# AIM:
To Create a backdoor with Social Engineering Toolkit (SET)

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode


### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

### Architecture Diagram

```
+----------------+        +------------------------+        +----------------------+
| Attacker's PC  | -----> | SET (Credential        | -----> | Fake Login Page      |
| (Kali Linux)   |        | Harvester via Apache)  |        | (Hosted by SET)      |
+----------------+        +------------------------+        +----------------------+
       |                                                             |
       |                                                             v
       |   1. Configure SET with phishing site (e.g., Gmail clone)   |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Victim's Browser     |
       | <------------------------------------------------| Clicks Phishing Link|
       |                                                 +----------------------+
       |                                                             |
       |                                                             v
       |     2. Victim Enters Credentials → Sent to SET/Attacker    |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Credentials Captured |
       |                                                 | in Apache log/SET DB |
       |                                                 +----------------------+

```

## EXECUTION STEPS AND ITS OUTPUT:
Social Engineering attacks are the various cons used by the hackers to trick people into providing sensitive data to the attackers.

**Steps to Use SET for Phishing (Credential Harvester Attack Method)**

**1. Open terminal:**
```bash
sudo setoolkit
```
<img width="866" height="951" alt="Screenshot 2025-09-27 094811" src="https://github.com/user-attachments/assets/a5168af4-d7a7-4343-ac0c-27e739ac3b77" />


**2. Navigate:**
```bash
1) Social-Engineering Attacks  
2) Website Attack Vectors  
3) Credential Harvester Attack Method  
```
<img width="943" height="477" alt="Screenshot 2025-09-27 094821" src="https://github.com/user-attachments/assets/5830f82e-b391-425c-b114-430ca29bc6a1" />


<img width="979" height="321" alt="Screenshot 2025-09-27 094830" src="https://github.com/user-attachments/assets/0d49bd34-9542-4e88-a907-16b2e8a01ece" />



**3. Enter your IP address as the attacker server.**
**4. Choose:**
```bash
2) Site Cloner
```
<img width="863" height="351" alt="Screenshot 2025-09-27 094839" src="https://github.com/user-attachments/assets/d0e8cbcc-576f-4151-bf1b-7d0e07eb94e2" />


**5. Enter the URL of the legitimate site ```(e.g., https://accounts.google.com)```**

<img width="1165" height="98" alt="image" src="https://github.com/user-attachments/assets/0476a220-719c-482c-bdc0-36db5fd58c5a" />




**6. Send the generated link to the victim.**
<img width="948" height="994" alt="Screenshot 2025-09-27 095025" src="https://github.com/user-attachments/assets/9fce1c45-4e56-46a6-9457-4692a2f22bc7" />



**7. Once the victim logs in → their credentials are stored in:**
```bash
/var/www/html/
```
<img width="935" height="664" alt="Screenshot 2025-09-27 094856" src="https://github.com/user-attachments/assets/6f066a5e-8b40-4760-9b1d-9816cfc8aa25" />




## RESULT:
The Social Engineering Toolkit (SET) is used to create backdoor is  examined successfully
