
# SPIFFEE at GitHub
Video: https://www.youtube.com/watch?v=vX8SS5wQuY8
## Motivation
- Make a single standard of identity between workloads a utility for teams

- DaemonSet vs. Reprovision SPIRE as a Systemd Unit
	- Availability: terminated before replacements -> Decouple from Kube Scheduler
	- Race conditions: pod creation unordered per Kube Node -> WorkloadAPI will always be started before workloads land on nodes
	- Dual Maintenance: Kube vs. Non-Kube config changes kept in sync -> one set of infrastructure code
- Exposing The Agent To Pods
	- Create Deployment with hostPath to spire-socket -> for every workload (not PSS conform)?

# Square
Video: https://www.youtube.com/watch?v=x642wq7lbpY

**Motivation**
- SPIRE
	- complete certificate issuance (X.509 SVID)
	- Pluggable architecture -> easy to extend
	- Support for Unix workload attestation
	- ...
- Migration process
	- SPIRE server cluster (2 nodes)
	- SPIRE agent on each host
	- Built a workload register
	- Update Envoy to include calls to SPIRE agents
	- Update frameworks to understand SPIFFE IDs
