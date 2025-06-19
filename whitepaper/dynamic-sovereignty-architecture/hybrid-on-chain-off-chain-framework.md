# Hybrid On-Chain / Off-Chain Framework

<figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

InSoBlok AI separates **critical state logic** from **high-volume, performance-sensitive operations** using a dual-layer system:

**On-Chain Layer (Security-Critical State Management)**

The **on-chain contract layer**, deployed on **InSoBlok Layer 1**, ensures the cryptographic integrity and trustworthiness of identity mappings, validator interactions, and tokenized asset ownership. Only operations that require **immutability, consensus, or fraud protection** are processed on-chain. These include:

* Account creation and DID registration
* Rent payments to reserve message slots
* Key management for connected applications
* Token staking and governance voting
* Smart contract execution logs with TasteScore-conditional logic

By maintaining minimal but essential state on-chain, the protocol balances **security and cost-efficiency** while anchoring trust for higher-order operations off-chain.

**Off-Chain Layer (Performance-Critical Data Operations)**

The **off-chain execution layer** is composed of a distributed, peer-to-peer network of specialized servers known as **Containers**. These nodes handle high-throughput, low-latency operations such as:

* Posting public messages, media, or polls
* Following, liking, and replying
* Updating profile images, VTO metadata, or creator badges
* Decentralized chat (including emoji, image, P2P payments)

All off-chain actions are cryptographically signed using a user’s on-chain keys and validated according to protocol rules. This design supports **massively scalable, socially dynamic interactions** with strong **eventual consistency guarantees**.
