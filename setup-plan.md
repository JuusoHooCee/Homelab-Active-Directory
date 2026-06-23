# Setup Plan – Home Lab (Active Directory)

## 🎯 Objective
Build a working Active Directory environment to simulate a real-world IT infrastructure.

---

## 🧱 Phase 1 – Infrastructure

### Step 1: Prepare virtualization
- Use Proxmox as hypervisor ✅ (already done)
- Verify network configuration
- Ensure enough RAM and storage

---

## 🖥️ Phase 2 – Windows Server (Domain Controller)

### Step 2: Create Windows Server VM
- Install Windows Server (Evaluation version)
- Configure:
  - Static IP address
  - Hostname (e.g. DC01)

### Step 3: Install roles
- Add Active Directory Domain Services (AD DS)
- Add DNS Server role

### Step 4: Promote to Domain Controller
- Create new forest:
  - Domain name: lab.local
- Set Directory Services Restore Mode (DSRM) password

---

## 👥 Phase 3 – Active Directory configuration

### Step 5: Create structure
- Organizational Units (OU)
  - Users
  - Computers
  - Admins

### Step 6: Create users and groups
- Standard user accounts
- Admin accounts (separate from normal users)
- Security groups

---

## 💻 Phase 4 – Client setup

### Step 7: Create Windows 11 VM
- Install Windows 11
- Configure DNS to point to Domain Controller

### Step 8: Join domain
- Join client to: lab.local
- Test domain login

---

## ⚙️ Phase 5 – Group Policy (GPO)

### Step 9: Basic GPO configuration
- Password policy
- Lock screen settings
- Desktop restrictions (test)

---

## ☁️ Phase 6 – Future (Hybrid Identity)

### Planned steps:
- Create Microsoft Entra ID tenant
- Install Entra Connect (Azure AD Connect)
- Sync users to cloud
- Test login and identity sync

---

## 🧠 Learning goals

- Understand AD structure and roles
- Learn DNS importance in domain environments
- Practice user and access management
- Prepare for hybrid identity (AD + Entra)

---

## 📒 Notes

This plan will be updated as the lab progresses.
