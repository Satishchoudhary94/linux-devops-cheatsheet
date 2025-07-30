# ⚙️ Ansible Basics — Beginner to Advanced

Ansible is a powerful **IT automation tool** used for configuration management, application deployment, and task automation.

---

## 🔧 What is Ansible?

- Agentless (no software required on managed nodes)
- Uses **SSH** for communication
- Automation is written in **YAML** files called **Playbooks**
- Push-based system (from control node to targets)

---

## 🚀 Installation Guide

### ✅ On Ubuntu / Debian

```bash
sudo apt update
sudo apt install ansible -y
```

✅ On CentOS / RHEL

```bash
sudo yum install epel-release -y
sudo yum install ansible -y

```

✅ On macOS

```bash
brew install ansible
```

✅ On Windows

> Use WSL (Ubuntu) or Virtual Machine
> Then follow Linux install instructions

🔍 Verify installation:

```bash
ansible --version
```

📁 Inventory File
Create an inventory.ini file to define your target machines:

```bash
[webservers]
192.168.1.101
192.168.1.102

[dbservers]
192.168.1.200 ansible_user=ubuntu ansible_ssh_private_key_file=~/.ssh/id_rsa

```

Group names in square brackets
You can define connection details like ansible_user, key file, etc.

📜 First Playbook Example
Let’s write a playbook to install Apache Web Server on remote Ubuntu machines.

Create a file install_apache.yml:

```bash
---
- name: Install Apache Web Server
  hosts: webservers
  become: yes

  tasks:
    - name: Update apt cache
      apt:
        update_cache: yes

    - name: Install apache2
      apt:
        name: apache2
        state: present

    - name: Start and enable Apache service
      service:
        name: apache2
        state: started
        enabled: yes
```

▶️ Running the Playbook

```bash
ansible-playbook -i inventory.ini install_apache.yml

```

## 🔍 Useful Commands

| Command                                      | Use                    |
| -------------------------------------------- | ---------------------- |
| `ansible all -m ping -i inventory.ini`       | Ping all machines      |
| `ansible all -a "uptime" -i inventory.ini`   | Run a shell command    |
| `ansible-playbook site.yml -i inventory.ini` | Run a playbook         |
| `ansible-doc -l`                             | List available modules |
| `ansible --version`                          | Check Ansible version  |

---

Use in playbook:

```bash
vars_files:
  - secrets.yml
```

Run:

```bash
ansible-playbook playbook.yml --ask-vault-pass
```
