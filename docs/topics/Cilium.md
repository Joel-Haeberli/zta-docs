tags: #spiffe #spire #authentication 

# Cilium

links: [[000 Index|Index]], [[400 Tools MOC]]

---


# Cilium & Spire

- https://isovalent.com/blog/post/2022-05-03-servicemesh-security/

> Mutual Authentication

## Limitations

- Cilium Mutual Authentication is still in development and considered beta.
- Cilium’s Mutual authentication has only been validated with SPIRE, the production-ready implementation of SPIFFE. Cilium is currently only tested with the supplied SPIRE install, and using any other SPIFFE implementation is currently not supported.
- There is no current option to build a single trust domain across multiple clusters for combining Cluster Mesh and Service Mesh. Therefore clusters connected in a Cluster Mesh are not currently compatible with Mutual Authentication.
- The current support of mutual authentication only works within a Cilium-managed cluster and is not compatible with an external mTLS solution

---
links: [[000 Index|Index]], [[400 Tools MOC]]