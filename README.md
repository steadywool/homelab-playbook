# 🐋 Homelab Playbook

Manage my Homelab with Ansible.

> [!NOTE]
>This Ansible project is designed to manage my infrastructure. Major changes are necessary to adapt to your needs.

## 🚀 Installation

> [!WARNING]
> Important variables are present in `group_vars` and `host_vars`. You need to edit them to customize your installation.</br></br>
> You must also edit the `inventory` file, playbooks and other files using hosts (like the Traefik config file).

Firstly, install Ansible:
```
# apt install ansible
```

```
# dnf install ansible
```

```
# pacman -S ansible
```

You can then clone this repository and enter it:
```
$ git clone https://github.com/steadywool/homelab-playbook.git
$ cd homelab-playbook
```

> [!TIP]
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
$ ansible-playbook playbooks/PLAYBOOK_FILE.yml --list-tags
```

Then use them with the `-t TAG` parameter.

You can skip some tags using the `--skip-tags TAG` parameter.

You can also run playbooks on hosts of your choice with the `--limit HOST` argument.