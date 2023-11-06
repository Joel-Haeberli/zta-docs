tags: #spiffe #authentication

# SPIFFE

links: [[000 Index|Index]], [[400 Tools MOC]]

---

## General

SPIFFE is a framework for workload *authentication* as the name *[Secure Production Identity Framework for Everyone (SPIFFE)](https://github.com/spiffe/spiffe/blob/main/standards/SPIFFE.md#secure-production-identity-framework-for-everyone-spiffe)* states. To fulfill its tasks, SPIFFE comes with three main components:

- [The SPIFFE ID](# [The SPIFFE Identity and Verifiable Identity Document](https://github.com/spiffe/spiffe/blob/main/standards/SPIFFE-ID.md#the-spiffe-identity-and-verifiable-identity-document))
- [The SPIFFE Identity and Verifiable Identity Document (SVID)](https://github.com/spiffe/spiffe/blob/main/standards/SPIFFE-ID.md#3-spiffe-verifiable-identity-document)
- [The Workload-API](https://github.com/spiffe/spiffe/blob/main/standards/SPIFFE_Workload_API.md#the-spiffe-workload-api)

(All relevant standard documents can be found on the official [spiffe github repository](https://github.com/spiffe/spiffe/tree/main/standards))

## Attesting things

SPIFFE is basically designed using a three-layer architecture. We have the SPIFFE-Server which deals as our trust-anchor against which all SPIFFE-Agents must authenticate in order to be able to attest Workload via the [Workload-API](https://github.com/spiffe/spiffe/blob/main/standards/SPIFFE_Workload_API.md#the-spiffe-workload-api).

Simplified this means:

- We trust the SPIFFE-Server
- The SPIFFE-Server attests SPIFFE-Agents (Node Attestation)
- The SPIFFE-Agent attests the SPIFFE-Workloads (Workload Attestation)

The workloads are managed by the SPIFFE-Server and *not* the SPIFFE-Agent. 

---
links: [[000 Index|Index]], [[400 Tools MOC]]