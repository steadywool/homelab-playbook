# 🕹️ Homelab Playbook

Create containers with Ansible.

## 🚀 Installation

> [!IMPORTANT]
> Important variables are present in the `group_vars` directory. You need to edit them to customize your installation. </br></br>
> You must also edit the `inventory` and Playbooks file.

Firstly, install Ansible:
```
# apt install ansible
```

You can then clone this repository and enter it:
```
$ git clone https://github.com/steadywool/homelab-playbook.git
$ cd homelab-playbook
```

> [!IMPORTANT]
> Never run this playbook with `sudo` or as root. If you need privileges, use the `-K` argument.

Start the playbook and configure your system with this command (replace PLAYBOOK_FILE with an existing one):
```
$ ansible-playbook playbooks/PLAYBOOK_FILE -u USER -K
```

## ✨ Configuration

You can perform partially run of playbook using tags.

You can list them with this command:
```
$ ansible-playbook playbooks/production.yml --list-tags
```

Then use them with the `-t ROLE` parameter.