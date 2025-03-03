# Node Exporter Installation with Ansible

## 📌 Overview
This repository contains an Ansible playbook to install **Node Exporter** on Linux servers.

## 📌 Prerequisites
- Ensure Ansible is installed on your control node.
- The target machines should allow SSH connections.
- Add your SSH keys or use passwords via Ansible Vault.

## 🛠️ **Step-by-Step Guide**
### 1️⃣ **Update Server Info**
Edit `inventory.ini` and replace `CHANGE_ME` with your instance IP.

Example:
```ini
[node_exporters]
myserver ansible_host=192.168.1.10 ansible_user=ubuntu


## 🚀 How to Use
1. Clone this repo:
   ```bash
   git clone https://github.com/yourrepo/node_exporter_repo.git
   cd node_exporter_repo

  ansible-playbook playbooks/install_node_exporter.yml -i your_inventory.ini

  ### Verify Installation
  systemctl status node_exporter

  ### Access metrics
  curl http://localhost:9100/metrics

