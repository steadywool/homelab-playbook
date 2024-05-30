# 🐋 Homelab Playbook

Create containers with Ansible.

This playbook use Docker Swarm to create an overlay network across differents hosts.

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
> Never run this playbook with `sudo` or as root. If you need privileges, use the `-K` (upper-case) argument. </br></br>
> If you don't use SSH keys, add the `-k` (lower-case) argument. </br></br>
> If you use an Ansible Vault, add the `-J` argument to ask the vault password.

Start the playbook and configure your system with this command (replace `PLAYBOOK_FILE`):
```
$ ansible-playbook playbooks/PLAYBOOK_FILE -K -J
```

**You should start with the `swarm.yml` playbook. It initialize the mandatory Docker network.**

## 🔧 Configuration

<details open>
    <summary>✨ You can perform partially run of playbook using tags:</summary>
    <ul>
        <li>qemu</li>
        <li>docker</li>
        <li>swarm</li>
        <li>baikal</li>
        <li>filebrowser</li>
        <li>firefly-iii</li>
        <li>freshrss</li>
        <li>jellyfin</li>
        <li>jellyseerr</li>
        <li>lidarr</li>
        <li>minecraft</li>
        <li>portainer</li>
        <li>prowlarr</li>
        <li>qbittorrent</li>
        <li>radarr</li>
        <li>syncthing</li>
        <li>traefik</li>
        <li>uptime-kuma</li>
        <li>watchtower</li>
        <li>wireguard</li>
    </ul>
</details>