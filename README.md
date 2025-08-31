# Wazuh Deployment Task

This repository contains my practical task where I deployed **Wazuh SIEM** on VMware, connected a Windows agent, and implemented **File Integrity Monitoring**.

---

##  Overview
- Deployed **Wazuh OVA** in VMware Workstation.
- Configured and accessed **Wazuh Dashboard**.
- Installed and connected **Windows Wazuh Agent** to the manager.
- Configured **File Integrity Monitoring** on Windows.
- Verified security events through Wazuh dashboard.

---

##  Steps Performed

### 1. Setting Up Wazuh OVA in VMware
- Downloaded Wazuh OVA from the [official Wazuh website](https://wazuh.com).
- Imported the OVA into **VMware Workstation**.
- Powered on the VM and retrieved the IP using:
    ```bash
    ip a
    ```
    (Example: `https://<your-Wazuh-IP>`)

---

### 2. Accessing the Wazuh Dashboard
- Accessed the Wazuh dashboard via:
    ```
    https://<your-Wazuh-IP>
    ```
- Used default credentials:
    ```
    Username: admin
    Password: admin
    ```

---

### 3. Installing the Wazuh Agent (Windows)
- Downloaded the Wazuh agent from the [official documentation](https://documentation.wazuh.com/).
- Configured the agent to connect to the manager (`<your-Wazuh-IP>`).

---

### 4. Connecting the Agent to the Manager
- Started the Wazuh agent service.
- Verified the agent appeared as **Active** in the Wazuh dashboard.

---

### 5. Configuring File Integrity Monitoring
- Edited the configuration file:
    ```
    C:\Program Files (x86)\ossec-agent\ossec.conf
    ```
- Added the directory path for monitoring inside `<ossec_config>` block.
- Restarted the agent service.

---

### 6. Testing File Monitoring
- Created `testfile.txt` in the monitored directory to trigger an event.

---

### 7. Verifying Logs on the Dashboard
- Checked **Security Events** in Wazuh dashboard and confirmed the event was logged successfully.

---

##  Files Included
- **Task 1.pdf** → Complete report with detailed steps and screenshots.

---

##  Skills Demonstrated
- Virtualization using VMware
- SIEM Deployment & Configuration
- Endpoint Monitoring
- File Integrity Monitoring (FIM)
- Security Event Analysis

---

### 🔍 How to View the Full Report
Download or open the [Task 1.pdf](./Task%201.pdf) file from this repository.
