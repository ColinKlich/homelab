# My Homelab Setup
This is an overview of my homelab setup and the services I'm currently running. 

## Navigation
* [Apps](https://github.com/colinklich/homelab/tree/main/apps) - List of all the apps and services.
* [Home Assistant](https://github.com/colinklich/homelab/tree/main/homeassistant) - Smart home services and automation.
* [Media Server](https://github.com/colinklich/homelab/tree/main/media) - Plex, Jellyfin, *arr stack, and more.
* [Server Monitoring](https://github.com/colinklich/homelab/tree/main/monitoring) - Graphs and Visualizations for Unraid, Proxmox, and more.
* [Storage](https://github.com/colinklich/homelab/tree/main/storage) - Current Storage and Backup Solution.
* [Proxy Managment](https://github.com/colinklich/homelab/tree/main/proxy) - NGINX Proxy Manager, DDNS with Cloudflare, Local Domains, and more.

## Hardware

(Picture coming soon!)

### Servers and NAS
#### Rackmount Server (Proxmox)
This machine is running our Proxmox Server. This machine currently hosts a Pi-hole DNS server, a Docker stack (n8n, OpenwebUI, Portainer), and a Kubernetes Cluster. Future plans include migrating the Plex stack, a minecraft server, and building out the Kubernetes cluster beyond bare metal.
* Intel(R) Xeon(R) CPU E5-2697A v4 (16c/32t)
* 256GB SODIMM DDR4 RAM
* 256GB NVMe SSD (Boot Drive)
* Nvidia Quadro P5000 16GB (PCIe passthrough to VMs)
* x2 1TB HDD (ZFS Drive)
* x2 Western Digital 4TB WD Red Plus (future addition)

#### AI/Gaming Rig (Windows 11)
This machine is running Windows 11 currently with plans to upgrade to Ubunut 24.04 in the future. This PC hosts my Ollama server, making use of 2x RTX 3090 GPUs to server up local ai models. I also use it to play games (which is why it is still windows).
* Ryzen 9 5900x (12c/24t)
* 64GB DDR4 RAM 3600mhz
* x2 RTX 3090 24GB GPUs (Ai Workloads)
* x1 1TB NVME (Boot Drive)
* x1 2TB NVME (AI models/games)

#### Synology NAS DS220+ (DSM)
This is the first machine in the homelab. It currently runs all the backup software as well as the Plex stack. Future plans include migrating the Plex stack to the PVE.
* Intel Celeron J4025
* 10GB DDR4 RAM (2GB included/8GB added)
* x1 8TB HDD
* x1 10TB HDD

### Networking
#### AT&T BGW-500
Gigabit networking with all the hiccups of AT&T. Passthrough to Orbi.

#### Orbi Wifi 6 Mesh System
handles all routing.

#### Netgear Prosafe 24 port Gigabit unmanaged Switch JGS524 V2
Eventually upgrade to 2.5gb or higher. 1gb is plenty for now.

