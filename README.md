Raspberry Pi PC (Pi 400) - Node-RED Backup


This folder contains the complete Node-RED dashboard and configuration backups for the IoT Model project running on the Raspberry Pi 400.

File Descriptions

flows.json
The exported Node-RED blueprint. This file contains the node wiring logic, MQTT connection settings, and the UI layout for the visual dashboard.

nodered-complete-backup.tar.gz
A full, compressed archive of the Pi 400's ~/.node-red directory. This includes the flows as well as all globally installed packages (such as node-red-dashboard) and system settings.

How to Restore

Option 1: Quick Import (Flows Only)

Open Node-RED in the browser (http://localhost:1880).

Ensure required palette plugins (e.g., node-red-dashboard) are installed.

Click the top-right menu -> Import and upload flows.json.

Option 2: Full System Restore (Exact Clone)
To instantly restore the exact environment on a fresh Raspberry Pi without having to manually install packages:

Copy nodered-complete-backup.tar.gz to the new Pi.

Extract it directly into the home directory's .node-red folder using the terminal:
tar -xzvf nodered-complete-backup.tar.gz -C ~/

Restart the Node-RED service: node-red-restart
