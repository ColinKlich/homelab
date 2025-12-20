# 🚀 K3s GitOps Dashboard Pipeline

This folder contains the Kubernetes manifests for the Homelab Dashboard. It is powered by a **CI/CD Pipeline** using GitHub Actions, Tailscale, and K3s.

## 🏗️ Architecture
The pipeline follows a "GitOps" pattern where the GitHub repository is the source of truth for the dashboard configuration.

1. **Trigger:** A developer pushes a change to the \`kubernetes/homepage/\` directory.
2. **Tunnel:** GitHub Actions initiates a **Tailscale** ephemeral node to securely connect to the home network.
3. **Deploy:** The action uses \`kubectl\` to apply changes to the K3s cluster via the Tailscale IP (**100.81.147.1**).
4. **Secrets:** Sensitive API keys (Proxmox, Pi-hole, Grafana) are pulled from a pre-existing Kubernetes Secret on the cluster.

## 📁 File Structure
* \`deployment.yaml\`: Defines the Homepage pod, resources, and environment variable mappings.
* \`configmap.yaml\`: Contains the \`services.yaml\` and \`widgets.yaml\` (UI layout).

## 🔐 Security & Secrets
To keep the repository public-safe, we use **Environment Variables**. 

Real keys are stored in a Kubernetes Secret named \`homepage-secrets\` on the cluster. The YAML files in this repo only refer to placeholders like:
\`\`\`yaml
key: "{{HOMEPAGE_VAR_GRAFANA_TOKEN}}"
\`\`\`

### Required GitHub Secrets
The following secrets must be set in the GitHub Repository Settings:
* \`KUBECONFIG\`: The cluster's kubeconfig file (pointing to the Tailscale IP).
* \`TAILSCALE_AUTHKEY\`: An ephemeral auth key from the Tailscale Admin Console.

## 🛠️ How to make changes
1. **Modify** the YAML files in \`kubernetes/homepage/\`.
2. **Commit** and **Push** to the \`main\` branch.
3. **Monitor** the "Actions" tab in GitHub to see the live deployment.

> **Note:** Always use \`kubectl-neat\` when exporting existing cluster configs to keep these files clean of system-generated metadata.