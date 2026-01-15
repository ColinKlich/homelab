# Proxmox Services
Here is a list of the services running within my PVE.

## 1. Pi-hole DNS
- Debian LXC
- network-wide ad filtering

## 2. Docker Stack
- Debian image (LXC had too many problems)
- Combines all docker services together

### Docker Services
1. Open Web UI
- connects to AI-Rig through Tailscale Meshnet
- Frontend for Ollama
- ChatGPT replacement

2. N8n
- Experimenting with Automation
- Connects to Ollama service through Tailscale Meshnet

## 3. Windows 11 VM
- Experiementing with virtualized gaming
- Uses Parsec to connect for low latency gameplay
- Radeon RX 480 8GB GPU
- Uses Proxmox GPU passthrough and VirtIO drivers

## 4. Ollama Local (Debian)
- localized Ollama service running on Debian
- Nvidia Quadro P5000 16GB GPU
- Uses Proxmox GPU passthrough

## 5. Plex (pending)
- Migrate from Synology for more processing/better transcoding
- Will allow more simultaneous users (friends & family)

## 6. K3s Kubernetes Cluster
- Comprised of master node (Debian) and 2 worker nodes (Debian)
- Currently runs Grafana and Homepage dashboards
- Hosts [Algomap](https://github.com/ColinKlich/AlgoMap) backend
- More info in the [kubernetes](https://github.com/ColinKlich/homelab/tree/main/kubernetes) folder