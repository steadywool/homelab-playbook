# 🐋 Homelab Playbook

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
> If you need a "sudo" password, use the `-K` (upper-case) argument. </br></br>
> If you don't use SSH keys, add the `-k` (lower-case) argument. </br></br>
> If you use an Ansible Vault, add the `-J` argument.

All playbooks are in the `playbooks` directory. Choose one and execute it:
```
$ ansible-playbook playbooks/PLAYBOOK_FILE.yml
```

## ✨ Configuration

You can perform partially run of playbook using tags.

You can list them with this command:
```
$ ansible-playbook playbooks/site.yml --list-tags
```

Then use them with the `-t ROLE` parameter.

## 📕 Exemples

Only install syncthing & sftpgo on the "apps" host :
```
$ ansible-playbook playbooks/deploy_apps.yml -t syncthing,sftpgo
```

Install Docker on every hosts that need it :
```
$ ansible-playbook playbooks/site.yml -t docker
```

Execute the entire vpn playbook but skip the watchtower installation :
```
$ ansible-playbook playbooks/deploy_vpn.yml --skip-tags watchtower
```

For more arguments, check the man page with the command `man ansible-playbook`.