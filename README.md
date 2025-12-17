# 🏦 **EscrowFlow v1.0**  
*A Comprehensive Marlowe Smart Contract for Secure Transactions with Dispute Resolution*

[![Marlowe](https://img.shields.io/badge/Built%20with-Marlowe-6741a5)](https://marlowe.iohk.io)
[![Cardano](https://img.shields.io/badge/Platform-Cardano-0033ad)](https://cardano.org)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

## 🎯 Overview

**EscrowFlow** is a production-ready Marlowe smart contract implementing a secure escrow system with integrated dispute resolution. Designed for Cardano blockchain, it automates payment holding, conditional release, and conflict resolution between transacting parties while minimizing trust requirements.

### **Key Value Propositions**
- 🛡️ **Secure Fund Custody** - Assets held in contract until explicit conditions met
- ⚖️ **Fair Dispute Resolution** - Three-tier resolution system with mediator arbitration
- ⏱️ **Time-Bound Processes** - Prevents indefinite fund locking with configurable deadlines
- 🔍 **Transparent Logic** - Verifiable on-chain execution with clear decision paths
- 🌐 **Permissionless Access** - No geographical restrictions or intermediary approvals
graph TD
    A[WAITING FOR DEPOSIT] -->|Buyer deposits| B[DEPOSITED]
    A -->|Timeout| C[CLOSED <br/> no action]
    B -->|Timeout| D[CLOSED <br/> no deposit]
    B -->|Buyer inspects| E[INSPECTING]
    E -->|Accept| F[FINALIZED <br/> Seller paid]
    E -->|Report problem| G[DISPUTE PHASE]
    G -->|Seller confirms| H[FINALIZED <br/> Buyer refunded]
    G -->|Seller disputes| I[MEDIATION]
    I -->|Mediator confirms| J[FINALIZED <br/> Buyer refunded]
    I -->|Mediator dismisses| K[FINALIZED <br/> Seller paid]
    
    style A fill:#ffeb3b,stroke:#333
    style B fill:#2196f3,stroke:#333
    style C fill:#9e9e9e,stroke:#333
    style D fill:#9e9e9e,stroke:#333
    style E fill:#e91e63,stroke:#333
    style G fill:#f44336,stroke:#333
    style I fill:#00bcd4,stroke:#333
    style F fill:#4caf50,stroke:#333
    style H fill:#4caf50,stroke:#333
    style J fill:#4caf50,stroke:#333
    style K fill:#4caf50,stroke:#333
