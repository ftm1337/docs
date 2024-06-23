---

title: 💸 TVL Guru
grand_parent:
parent:
has_children:
nav_order:

---


# FTM.guru : TVL Contract
## On-Chain Total Value Locked Adapter

*Note: Please use the latest version of TvlGuru. You can import your old TvlGuru into a new one as a `tvl_e` (External TVL) module, which exports `tvl` (18-decimal tvl in USD)*

----

### Introduction
We have deployed  a Smart Contract that calculates instantaneous TVL (via on-chain calls) & per-block TVL (via web3 calls) of any Decentralized Finance platform.
The ftm.guru platform, taking in consideration its huge collection of on-chain Stores of Value, uses this Smart Contract across its products.
#### Index
Universal usage:
- Smart Contract Details
- Summary of Modules
- On-chain Usage (`ITVL`)
- Off-chain Usage (A.B.I.)
- Accounts & DataBanks

ftm.guru's Databanks & Adapters:
- Banks (Account Details)
- Finding TVL via adapter

----

## Universal Usage
### General
- The Universal TVL Finder can work with any Protocol, Project or EVM-like blockchain.
- `coin` refers to the native unit of the blockchain. On Fantom Opera, it refers to the FTM.

### Our own instances of `tvlGuru`
`tvlGuru.sol` is a template anyone can deploy for their own use. The base contract is same for everyone yet the contract storage is unique for each instance. We utilize our own instances of `tvlGuru` for kcc.guru and ftm.guru TVL calculations.

