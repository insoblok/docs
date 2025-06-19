# Containers: Distributed Sovereignty Nodes

**Containers** are decentralized data nodes that store and validate all InSoBlok AI user activity off-chain. Any participant can run a Container on local hardware or in the cloud, contributing to storage replication, gossip syncing, and diff-based message reconciliation.

Each Container:

* Syncs with Layer 1 to stay aware of all account keys and state
* Validates message signatures and constraints (e.g., byte limits, message lifespan)
* Stores user content, structured metadata, and TasteScore computation inputs
* Replicates messages across peers using **libp2p's gossipsub protocol**
* Enforces **CRDT (Conflict-Free Replicated Data Types)** to resolve update conflicts deterministically

Containers operate with **strong eventual consistency**, ensuring that nodes may fall behind temporarily but always catch up without state corruption.
