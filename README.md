# 🏠 My Homelab Setup

> _A living, ever-evolving collection of self-hosted services, automation, and hardware tinkering!_

---

## 🚀 Navigation
- [💾 Services](https://github.com/colinklich/homelab/tree/main/services) — Current Services running within my PVE
- [🗂️ Apps](https://github.com/colinklich/homelab/tree/main/apps) — List of all the apps and services
- [🏡 Home Assistant](https://github.com/colinklich/homelab/tree/main/homeassistant) — Smart home services & automation
- [🎬 Media Server](https://github.com/colinklich/homelab/tree/main/media) — Plex, Jellyfin, *arr stack, and more
- [📊 Server Monitoring](https://github.com/colinklich/homelab/tree/main/monitoring) — Graphs & Visualizations for Unraid, Proxmox, and more
- [💾 Storage](https://github.com/colinklich/homelab/tree/main/storage) — Current Storage and Backup Solution
- [🌐 Proxy Management](https://github.com/colinklich/homelab/tree/main/proxy) — NGINX Proxy Manager, DDNS with Cloudflare, Local Domains, and more

---

## 🖥️ Hardware

(Picture coming soon!)

### 🗄️ Servers and NAS

<details>
<summary><strong>Rackmount Server (Proxmox)</strong></summary>

- **CPU:** Intel(R) Xeon(R) E5-2697A v4 (16c/32t)
- **RAM:** 256GB SODIMM DDR4
- **Boot:** 256GB NVMe SSD
- **GPU:** Nvidia Quadro P5000 16GB (PCIe passthrough to VMs)
- **Storage:** 2× 1TB HDD (ZFS), 2× 4TB WD Red Plus (future)
- **Services:** Pi-hole, Docker stack (n8n, OpenwebUI, Portainer), Kubernetes, future Plex & Minecraft

</details>

<details>
<summary><strong>AI/Gaming Rig (Windows 11)</strong></summary>

- **CPU:** Ryzen 9 5900x (12c/24t)
- **RAM:** 64GB DDR4 3600MHz
- **GPU:** 2× RTX 3090 24GB (AI workloads)
- **Storage:** 1TB NVMe (Boot), 2TB NVMe (AI models/games)
- **Notes:** Hosts Ollama server for local AI models, comfyui(stable diffusion), gaming, planned upgrade to Ubuntu 24.04

</details>

<details>
<summary><strong>Synology NAS DS220+ (DSM)</strong></summary>

- **CPU:** Intel Celeron J4025
- **RAM:** 10GB DDR4 (2GB stock + 8GB added)
- **Storage:** 8TB HDD + 10TB HDD
- **Role:** Backup software, Plex stack (to be migrated to PVE)

</details>

---

### 🌐 Networking

- **AT&T BGW-500:** Gigabit networking (passthrough to Orbi)
- **Orbi Wifi 6 Mesh:** Handles all routing
- **Netgear Prosafe 24-port Gigabit Switch (JGS524 V2):** Unmanaged, future upgrade to 2.5GbE or higher

---

> _Have questions or want to see more? Check out the [Apps](https://github.com/colinklich/homelab/tree/main/apps) directory for detailed guides and screenshots!_

---

