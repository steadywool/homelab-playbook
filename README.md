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
> If you need a "sudo" password, use the `-K` (upper-case) argument. </br></br>
> If you don't use SSH keys, add the `-k` (lower-case) argument. </br></br>
> If you use an Ansible Vault, add the `-J` argument to ask the vault password.

Start the playbook and configure your system with this command:
```
$ ansible-playbook playbooks/swarm.yml
$ ansible-playbook playbooks/site.yml
```

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

## 📕 Exemples

Only install syncthing & filebrowser on the production hosts :
```
$ ansible-playbook playbooks/production.yml -t syncthing,filebrowser
```

Install Qemu Guest Agent & Docker on every hosts that need them :
```
$ ansible-playbook playbooks/site.yml -t qemu,docker
```

Execute the entire vpn playbook but skip the watchtower installation :
```
$ ansible-playbook playbooks/vpn.yml --skip-tags watchtower
```

For more arguments, check the man page with the command `man ansible-playbook`.