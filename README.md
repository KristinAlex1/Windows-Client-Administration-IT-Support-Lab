# 🖥️ Windows Server & Active Directory  
## University-Style Systems Administration Project

## 🧩 System Design Summary
<img width="1536" height="1024" alt="Diagram" src="https://github.com/user-attachments/assets/915ac970-8cdb-40b2-9260-c82e43c46bf1" />


This project simulates a **university-style Active Directory environment** built around a centralized **Windows Server 2022 Domain Controller (DC01)** and a **Windows 10 domain-joined client**, connected through an internal network representing a campus LAN.

The Domain Controller hosts **Active Directory Domain Services (AD DS)**, **DNS**, and **Group Policy Objects (GPOs)** to manage identities, authentication, and policy enforcement across student and faculty accounts. Organizational Units (OUs) and security groups are used to reflect real academic role separation.

A domain-joined Windows 10 client validates authentication flows and Group Policy enforcement for end users.

The environment also includes **simulated help desk operations**, where common university IT support scenarios are handled directly through Active Directory:
- Student account unlocks before exams  
- Secure password resets with enforced policy  
- New student account onboarding and group assignment  
- Faculty access and permission verification  


## 📌 Project Overview

This project demonstrates the design, deployment, and administration of a **university-style on-premises Active Directory environment** using **Windows Server 2022** and a **Windows 10 domain-joined client**.

The lab simulates how a university IT department manages:

- Student and faculty identities  
- Domain-joined endpoints  
- Group Policy enforcement  
- Identity-related IT support tickets  

The project also includes **real troubleshooting scenarios** and **documented ticket resolutions**, reflecting real-world systems administration work.

---

## 🧰 Technologies Used

- Windows Server 2022  
- Active Directory Domain Services (AD DS)  
- DNS  
- Group Policy  
- Windows 10 (Domain-joined client)  
- VirtualBox (Internal Network)  
- GitHub (Documentation)

---

## 🏗️ Architecture Overview

- **Domain:** `acadialab.local`  
- **Domain Controller:** DC01  
- **Client Machine:** Windows 10  
- **Network Type:** Internal Network (Simulated campus LAN)

---

## 🔹 Phase 1: Windows Server Installation & Base Configuration


### What Was Done
- Installed Windows Server 2022  
- Assigned static IP address  
- Renamed server to **DC01**

# Screenshot 1
<img width="1033" height="830" alt="Project3-1" src="https://github.com/user-attachments/assets/27b3ff2e-592f-4939-830d-9103066a62f3" />

# Screenshot 2
<img width="1024" height="832" alt="Project3-2" src="https://github.com/user-attachments/assets/df0ec698-4571-45cd-8379-74209730f6a1" />


### Skills Learned
- Server OS installation  
- Static IP configuration  
- Importance of fixed addressing for infrastructure servers  

---

## 🔹 Phase 2: Active Directory Domain Services & DNS

### What Was Done
- Installed Active Directory Domain Services (AD DS)  
- Promoted server to Domain Controller  
- Created a new forest and domain `acadialab.local`  
- Installed DNS integrated with Active Directory

# Screenshot 3
<img width="805" height="570" alt="Project3-3" src="https://github.com/user-attachments/assets/28e669e1-a60a-44ac-ad9e-291c1b7a2112" />

# Screenshot 4
<img width="1026" height="772" alt="Project3-4" src="https://github.com/user-attachments/assets/e9af4282-d9ee-473e-8c0c-5f500ec34e2e" />

# Screenshot 5
<img width="1051" height="797" alt="Project3-6" src="https://github.com/user-attachments/assets/02b976de-2156-42f1-96a6-860a1618d1f4" />

### Skills Learned
- Active Directory fundamentals  
- Forests, domains, and domain controllers  
- DNS integration with Active Directory  

---

## 🔹 Phase 3: Active Directory Design (University Structure)

### What Was Done
- Created Organizational Units (OUs):
  - Students  
  - Faculty  
  - Staff  
- Created domain users:
  - `student01`  
  - `faculty01`  
- Created security groups for role-based access

# Screenshot 6
<img width="1032" height="776" alt="Project3-7" src="https://github.com/user-attachments/assets/d429e5ce-5873-4d01-a1dc-2407d70fa9e7" />

# Screenshot 7
<img width="957" height="787" alt="Project3-8" src="https://github.com/user-attachments/assets/5612c808-547c-4c26-b9c6-8a166378ea0b" />



### Skills Learned
- OU design and hierarchy  
- User lifecycle management  
- Role-based access control (RBAC)  

### 📸 Screenshot – AD OU Structure

Active Directory OU Structure](screenshots/phase4-ad-structure/ou-structure.png

---

## 🔹 Phase 4: Group Policy Implementation

### What Was Done
- Created Group Policy Objects (GPOs)
- Linked GPOs to the Students OU
- Applied user-based restrictions
- Verified GPO scope and enforcement


# Screenshot 8
<img width="957" height="787" alt="Project3-8" src="https://github.com/user-attachments/assets/134ba924-44ec-4ecd-a682-bc4d0f178f84" />

# Screenshot 9
<img width="909" height="598" alt="Project3-9" src="https://github.com/user-attachments/assets/1e5308d8-5439-43e8-892b-78620d34664b" />

# Screenshot 10
<img width="951" height="652" alt="Project3-11" src="https://github.com/user-attachments/assets/6f8561c8-c5fb-426d-b447-50631ffd8199" />

# Screenshot 11
<img width="959" height="664" alt="Project3-12" src="https://github.com/user-attachments/assets/63aa4164-be6a-4b70-abb0-307106532c80" />


## Skills Learned
- Group Policy creation and linking
- User vs computer policies
- Policy inheritance and enforcement


---

## 🔹 Phase 5: Client Domain Join & Validation

### What Was Done
- Installed Windows 10 client
- Assigned static IP address and DNS
- Joined client to acadialab.local
- Logged in using domain credentials
- Verified Group Policy enforcement

# Screenshot 12
<img width="1020" height="811" alt="Project3-14-1" src="https://github.com/user-attachments/assets/d64214ac-670b-4b71-8e40-1985834f918b" />

# Screenshot 13
<img width="1015" height="801" alt="Project3-14-2" src="https://github.com/user-attachments/assets/4725d99a-4890-412d-8f31-7bcd2618b1c3" />

# Screenshot 14
<img width="957" height="689" alt="Project3-15" src="https://github.com/user-attachments/assets/658c71a2-2801-41eb-b09c-f6fefbba18c3" />

# Screenshot 15
<img width="1021" height="858" alt="Project3-13" src="https://github.com/user-attachments/assets/35a50cc3-db90-43dc-ba0c-ae59edaee1b1" />

## Skills Learned
- Domain join process
- Client-server authentication
- DNS dependency in Active Directory
- Endpoint policy validation

##🔹 Phase 6: IT Ticketing & Operations (Real-World Scenarios)

This phase simulates real university IT support tickets handled by a systems administrator.

# Tickets Handled
- Student account locked before exam
- Student password reset
- New student onboarding
- Faculty access verification

## All tickets are documented in ticket-log.md.
# Skills Learned
- Identity troubleshooting
- Secure access restoration
- IT documentation
- Operational decision-making
  
# 🎫 Ticket 1: Student Account Locked Before Exam
## Issue:
 A student was locked out of their university account after multiple failed login attempts just before an exam.

## Action Taken:
- Located the user account in Active Directory Users and Computers
- Verified account lockout status
- Unlocked the account using the Account tab

## Tools Used:
- Active Directory Users and Computers (ADUC)

## Outcome:
- Account access restored
- Student successfully logged in to domain resources

# 📸 Screenshot – Account Unlock
<img width="1022" height="770" alt="Project3-Phase6-Ticket1" src="https://github.com/user-attachments/assets/af3d13da-fd9e-435a-b4fd-5ca47de3bdb0" />


## Skills Demonstrated:
- Identity troubleshooting
- Time-sensitive incident resolution
- Active Directory account management

# 🎫 Ticket 2: Student Password Reset Request
## Issue:
A student forgot their password and was unable to log in to university systems.

## Action Taken:
- Reset the user password in Active Directory
- Enforced “User must change password at next logon” for security

## Tools Used:
- Active Directory Users and Computers (ADUC)

## Outcome:
- Secure access restored

## Password policy enforced:
📸 Screenshot – Password Reset
<img width="1024" height="768" alt="Project3-Phase6-Ticket2" src="https://github.com/user-attachments/assets/ec7702d0-32d6-4344-a953-ff4519347105" />

## Skills Demonstrated:
- Secure credential handling
- Identity lifecycle management
- Policy enforcement

# 🎫 Ticket 3: New Student Account Onboarding
## Issue:
A new student joined mid-semester and required access to university systems.

## Action Taken:
- Created a new user account in the Students OU
- Assigned correct security group membership

## Tools Used:
- Active Directory Users and Computers (ADUC)

## Outcome:
- Account provisioned successfully

## Access aligned with student role:

📸 Screenshot – Student Account Created

<img width="1024" height="773" alt="Project3-Phase6-Ticket3-1" src="https://github.com/user-attachments/assets/2d5442c2-a060-4a1d-bee8-2e66be37575f" />

<img width="1028" height="772" alt="Project3-Phase6-Ticket3-2" src="https://github.com/user-attachments/assets/0a5ac490-118d-46b1-909b-94a6df183fbd" />

## Skills Demonstrated:
- User provisioning
- OU-based identity management
- Role-based access control (RBAC)

# 🎫 Ticket 4: Faculty Access Verification
## Issue:
A faculty member requested verification of access to required university resources.

## Action Taken:
- Reviewed group memberships
- Confirmed faculty role-based permissions
- No unnecessary changes made

## Tools Used:
- Active Directory Users and Computers (ADUC)

## Outcome:
- Access confirmed
- RBAC compliance verified

📸 Screenshot – Faculty Group Membership

<img width="1032" height="769" alt="Project3-Phase6-Ticket4" src="https://github.com/user-attachments/assets/52dcaa23-84cf-4ddf-b836-f376d4736da7" />


## Skills Demonstrated:
- Access auditing
- Principle of least privilege
- Operational judgment

# 📌 Conclusion

 This project demonstrates hands-on experience with Windows Server, Active Directory, and real IT operational workflows, with a strong focus on problem solving, documentation, and user support in a university setting.
