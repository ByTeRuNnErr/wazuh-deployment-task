# Wazuh Deployment Task

## 1. Setting Up Wazuh OVA in VMware
- Downloaded Wazuh OVA (Open Virtual Appliance) from the [official Wazuh website](https://wazuh.com).
- Imported the OVA into **VMware Workstation**:
    - Open VMware Workstation
    - Click **Open a Virtual Machine**
    - Select the downloaded `.ova` file
    - Follow the prompts to import the appliance
- Powered on the VM and ran:
    ```bash
    ip a
    ```
    to get the IP address (e.g., `192.168.100.232`) for dashboard access.

---

## 2. Accessing the Wazuh Dashboard
- Accessed the Wazuh dashboard via:
    ```
    https://192.168.100.232
    ```
- Used default credentials:
    ```
    Username: admin
    Password: admin
    ```

---

## 3. Installing the Wazuh Agent (Windows)
- Downloaded the Windows Wazuh agent from the [official documentation](https://documentation.wazuh.com/).
- Configured the agent to connect to the manager (`192.168.100.232`).

---

## 4. Connecting the Agent to the Manager
- Started the Wazuh agent service.
- Verified the agent appeared as **Active** in the Wazuh dashboard.

---

## 5. Configuring File Integrity Monitoring
- Edited the config file:
    ```
    C:\Program Files (x86)\ossec-agent\ossec.conf
    ```
- Added the directory path for monitoring inside `<ossec_config>` block.
- Restarted the agent service.

---

## 6. Testing File Monitoring
- Created `testfile.txt` in the monitored directory to trigger an event.

---

## 7. Verifying Logs on the Dashboard
- Checked **Security Events** in Wazuh dashboard and confirmed the event was logged successfully.

---

## 8. Conclusion
- Successfully deployed Wazuh Manager on VMware.
- Installed and connected a Windows agent.
- Configured and verified **File Integrity Monitoring**.

---

###  **Skills Demonstrated**
- Virtualization using VMware
- SIEM setup and configuration
- Endpoint monitoring
- File integrity monitoring
