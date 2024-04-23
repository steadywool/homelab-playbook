# 🕹️ Selfhosted Playbook

Create Podman containers with Ansible.

## 🚀 Installation

> [!IMPORTANT]
> Important variables are present in the `group_vars` directory. You need to edit them to customize your installation. </br></br>
> You also need to edit the `inventory` file to add your server IP adress by replacing the "REMOTE_SERVER" placeholder. </br></br>
> Never run this playbook with `sudo` or as root. If you need privileges, use the `-K` argument.

Firstly, install Ansible:
```
# apt install ansible
```

You can then clone this repository and enter it:
```
$ git clone https://github.com/steadywool/selfhosted-playbook.git
$ cd selfhosted-playbook
```

Start the playbook and configure your system with this command:
```
$ ansible-playbook playbook.yml -K
```

## 🔧 Configuration

✨ You can perform partially run of playbook using tags:
- main
- games
- games.minecraft
- services
- services.caddy
- services.syncthing
- services.wireguard