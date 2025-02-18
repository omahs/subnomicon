---
title: Node Types
sidebar_position: 1
description: Participants in the Subspace Network
keywords:
    - Consensus
    - Network
    - Node
    - Peer
---

## Node Configurations
A Subspace Node can run in several modes depending on configuration:

### Full Node

Full Nodes participate fully in the network by processing all blocks, participating in consensus, and serving peers. Full nodes retain recent history and state for a configurable number of recent blocks until it is archived and pruned. A full node is a default configuration for farmers and operators.

### Archival Node

Archival Nodes are a superset of full nodes. They retain the entire blockchain history and state in addition to all the functions performed by full nodes. Archival nodes are useful for block explorers and historical queries. Subspace Labs will maintain several archival nodes as a public good.

### Light Client

A Light Client is a node that does not retain the full blockchain state. Instead, it connects to full nodes and processes block headers, but doesn’t run the state transitions nor retains any history. Light clients are useful for mobile or low-resource devices that need to interact with the network without running a full node. It can run in a browser, for instance, with [Substrate Connect](https://github.com/paritytech/substrate-connect).

The network's health, robustness, and resistance to censorship rely on the constant online presence of numerous full nodes that are independently managed and spread across different geographic locations. Each full node supports newly joined nodes by providing them with the necessary block data to start their participation. Additionally, operating a full node allows the participant to independently verify all blocks, ensuring an authoritative assessment.
Subspace is dedicated to the promotion of decentralization through full nodes by keeping the hardware requirements low enough that individuals can run them from home while still providing sufficient resources to support the network.

## Node Roles

The Subspace network is made up of different types of nodes that each play a specific role:

### Farmer

A Farmer is responsible for maintaining consensus (safety of the Consensus Chain). A Farmer plots pieces of Archival History to disk, farms the created plot for block rewards, joins the DSN as a node for data retrieval (for syncing nodes, other farmers and returning data to various Clients).

### Domain Operator

A Domain Operator is responsible for running arbitrary computation on Domains, state transitions, maintaining state (liveness of the Execution Chain).

### Timekeeper
A Timekeeper is responsible for running Proof-of-Time chain and maintaining the randomness beacon for the Consensus Chain.
