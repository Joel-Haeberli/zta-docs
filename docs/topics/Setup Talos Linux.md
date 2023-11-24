- Create VMs on Proxmox (3 control-plane, 2 worker)
	- control-plane: 2vCPU / 4GiB Memory
	- worker: 4vCPU / 8GiB Memory
- Minio for Loki & Velero
- Firewall / Switch
	- VLANs
	- WAN IPs (Incoming / Outgoing)
	- BGP config
	- Rules
- NFS as Storage
- Monitoring Cluster (Dead Man Snitch)

- cilium
	- architecture: https://docs.cilium.io/en/stable/overview/component-overview/#component-overview
	- bgp
	- wireguard encryption
	- hubble

```bash
# validate setup
kubectl -n kube-system exec -ti ds/cilium -- bash
cilium status | grep Encryption
```