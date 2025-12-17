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
# Color legend:
# WAITING = yellow
# DEPOSITED = blue
# INSPECTING = magenta
# DISPUTE PHASE = red
# CLOSED = grey
# MEDIATION = cyan
# FINALIZED = green

echo -e "\e[33m+----------------+\e[0m     \e[34m+----------------+\e[0m     \e[35m+-------------------+\e[0m"
echo -e "\e[33m| WAITING        |\e[0m---->\e[34m| DEPOSITED      |\e[0m---->\e[35m| INSPECTING        |\e[0m"
echo -e "\e[33m| FOR DEPOSIT    |\e[0m     \e[34m|                |\e[0m     \e[35m|                   |\e[0m"
echo -e "\e[33m+----------------+\e[0m     \e[34m+----------------+\e[0m     \e[35m+-------------------+\e[0m"
echo -e "        |                     |                       |"
echo -e "     (timeout)             (timeout)                  |"
echo -e "        v                     v                       v"
echo -e "\e[90m+----------------+\e[0m     \e[90m+----------------+\e[0m     \e[91m+-------------------+\e[0m"
echo -e "\e[90m| CLOSED         |\e[0m<----\e[90m| CLOSED         |\e[0m<----\e[91m| DISPUTE PHASE     |\e[0m"
echo -e "\e[90m| (no action)    |\e[0m     \e[90m| (no deposit)   |\e[0m     \e[91m|                   |\e[0m"
echo -e "\e[90m+----------------+\e[0m     \e[90m+----------------+\e[0m     \e[91m+-------------------+\e[0m"
echo -e "                                           |"
echo -e "                                           v"
echo -e "\e[36m+-------------------+\e[0m"
echo -e "\e[36m| MEDIATION         |\e[0m"
echo -e "\e[36m+-------------------+\e[0m"
echo -e "                                           |"
echo -e "                                           v"
echo -e "\e[32m+-------------------+\e[0m"
echo -e "\e[32m| FINALIZED         |\e[0m"
echo -e "\e[32m+-------------------+\e[0m"

                                                          v
                                                 +-------------------+
                                                 |   FINALIZED       |
                                                 |                   |
                                                 +-------------------+
