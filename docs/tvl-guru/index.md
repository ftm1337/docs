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

#### Special note:
ftm.guru TVL accumulations started in [June 2021](https://ftmscan.com/tx/0x294a18e9961af8a4084b14a3e57b963640c5aae6e6a669f1e067a0340889cfab) with YieldState - 1.
The `v6` contract features an advanced `p_lpt_tt_coin_usd` module, which is an improvement over the sub-optimal module on `v5`.  
Our `v5` TVL gets imported cummulatively into the new `v6` as an `e_usd` Bank. Doing this has the following specialities:
- Saves time required for making 25+ transactions.
- Economical since gas is now more expensive on Fantom.
- Compatible interface and modularity helps make easy upgrades.
- `v6` cannot be queried for historical data behind 2021-01-16.
- `v5` should be used for historical data between 2020-12-26 and 2021-01-16.
- `v6` is recommended for all uses, applications and analytics.


### Smart Contract Details
#### v6 Address
- `fantom:0x0786c3a78f5133F08C1c70953B8B10376bC6dCad` [Read on ftmscan](https://ftmscan.com/address/0x0786c3a78f5133F08C1c70953B8B10376bC6dCad#readContract)
- `kcc:0x426a4A4B73d4CD173C9aB78d18c0d79d1717eaA9` [Read on scan.kcc](https://scan.kcc.io/address/0x426a4A4B73d4CD173C9aB78d18c0d79d1717eaA9/read-contracts)
- `echelon:0xc42974d6554F9054265b477723C3f689d8699239` [Read on scout.ech](https://scout.ech.netowork/address/0xc42974d6554F9054265b477723C3f689d8699239/read-contracts)
- `multivac:0x426a4A4B73d4CD173C9aB78d18c0d79d1717eaA9` [Read on scan.kcc](https://scan.kcc.io/address/0x426a4A4B73d4CD173C9aB78d18c0d79d1717eaA9/read-contracts)

#### v5 Address
- `0x3f0458FfB6D106d2F5CdeC9CEdc9054A69275489` [Read on ftmscan](https://ftmscan.com/address/0x3f0458FfB6D106d2F5CdeC9CEdc9054A69275489#readContract)

#### v4 Address
- `0x41b9231e528a417341382b2c995c6dde21cea93d` [Read on ftmscan](https://ftmscan.com/address/0x41b9231e528a417341382b2c995c6dde21cea93d#readContract)



----

# ftm.guru's Databanks & Adapters:
## ftm.guru's Banks : Account Details
Below are detailed all Banks, by chronology.  
Beneath it, are detailed all Banks, grouped acccording to modules.

## Banks : By Chronology

### KCC

|  №  |    Asset Locked Up          | Pool Contract locker              | ITVL Interface Module |             Asset Contract Address           |              Pool Contract Address           |  
| --- |           ---               |          ---                      |           ---         |                  ---                         |                    ---                       |
| 1   | KCS                         | Kucino Casino - Profitshare       | `coin_usd`            | `0xEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEE` | `0x4c9fa6297d3413fbbe7ba935e14022d0e5a39dc7` |
| 2   | wKCS-BNB Kudex LPT          | Kompound Protocol - GRAIN#3101    | `e_usd`               | `0x7b693def9d5E34DC867b0328409380DDD80b2d93` | `0xddca793284b546cce25e03af53c2ac0f949a8b8d` |
| 3   | wKCS-USDT Kudex LPT         | Kompound Protocol - GRAIN#3102    | `e_usd`               | `0x9528b555666E36490574217ec9E159a9B89203e2` | `0xf5be9634549fead60f7dce272fe9a4b96c3b1926` |
| 4   | wKCS-USDC Kudex LPT         | Kompound Protocol - GRAIN#3103    | `e_usd`               | `0xfcFE2562fb9edD16aBbA43295D66B154f79C56D1` | `0x727A82566ff09AC80ce9D33651197dDCDaFd5a3D` |
| 5   | wKCS-USDT Kuswap LPT        | Kompound Protocol - GRAIN#3201    | `e_usd`               | `0x6c31e0F5c07b81A87120cc58c4dcc3fbafb00367` | `0x5Bb3895D4faC7Ce3AfBb163A9e0a9364aa7AA07d` |
| 6   | wKCS-USDC Kuswap LPT        | Kompound Protocol - GRAIN#3202    | `e_usd`               | `0x943F29A00415D8cE38607aBb81e36cdDfDCAA77f` | `0x974822c6fd06709709fbf880d29352EF19A7CF88` |
| 7   | wKCS-DAI Kuswap LPT         | Kompound Protocol - GRAIN#3203    | `e_usd`               | `0xe2c3a808dc1ed72f7d148d073def94ddbef87c51` | `0x2A5C9F52b0211Ed72f776a3692de192Cef8B160F` |
| 8   | wKCS-BTCK Kuswap LPT        | Kompound Protocol - GRAIN#3204    | `e_usd`               | `0x009fe8daccdcb2c82f5bde0e9a28d0d802ff93fd` | `0x03010C2C9E5eC5779fF744e79A86921d58486085` |

*To-do: Push TVL info from all the Casino & Games Contracts*


### Fantom

|  №  |    Asset Locked Up          | Pool Contract locker              | ITVL Interface Module |             Asset Contract Address           |              Pool Contract Address           |  
| --- |           ---               |          ---                      |           ---         |                  ---                         |                    ---                       |
| 1   | ELITE-WFTM Sushi LPT        | YieldState                        | `lpt_coin_usd`        | `0x50576ed9d94cf934bc32abf76e08ec6ddcd54bf0` | `0xef66a11788a3b3180be4aa31a5743c6a6e87a555` |
| 2   | ELITE-WFTM Spooky LPT       | YieldState 2                      | `lpt_coin_usd`        | `0xea035a13b64cb49d85e2f0a2736c9604cb21599c` | `0xad70c7cbc8f856681b4ebdd37aeac58cf7100736` |
| 3   | ELITE                       | XELITE                            | `t_coin_usd`          | `0xf43cc235e686d7bc513f53fbffb61f760c3a1882` | `0x1BE23c78038B6057172848534AcD62667fA2620d` |
| 4   | FTM                         | BO#1 FTMUSD 3-day Call/Put Option | `coin_usd`            | `0xEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEE` | `0x92679257ecA3c3Dba25b777185EB82cD81991e72` |
| 5   | FTM                         | DeGam - Micro Jackpot             | `coin_usd`            | `0xEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEE` | `0x21eE31ea0e5B4628aC3c1b2Ec6602aeB60d8D124` |
| 6   | FTM                         | DeGam - Mini Jackpot              | `coin_usd`            | `0xEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEE` | `0x9A6eb015aebC6466d407d40D278894bc773bd009` |
| 7   | FTM                         | DeGam - FTM Coin-Flip             | `coin_usd`            | `0xEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEE` | `0xC318D7be0f170C0Cc446D2d62132180367956591` |
| 8   | NIPS-WFTM ZooDEX LP         | LITE Farmlands - LF#1:NIPS        | `lpt_coin_usd`        | `0xdEAD5ee1d489b8f0d3815E4d26554fE1aeF01281` | `0x0d039CF5d0A8a1A8019797474c215d3c61fAC49f` |
| 9   | DEATH-WFTM Spooky LP        | LITE Farmlands - LF#23:DEATH      | `lpt_coin_usd`        | `0xae368F02b66d58827db39eF3248afEFE370cA9A4` | `0xc8207c5c54b4cf54AA3F5538Cc8a2C6dfA2716d8` |
| 11  | BabySpirit-WFTM Spirit LP   | LITE Farmlands - LF#151:BabySpirit| `lpt_coin_usd`        | `0xB0002624766dA87e249eae3B6175D4EAE7373eAb` | `0xF88005D839A2f14E6b4f14938bb3DEB4521cff21` |
| 12  | BabySpirit-WFTM Spirit LP   | LITE Farmlands - LF#152:BabySpirit| `lpt_coin_usd`        | `0xB0002624766dA87e249eae3B6175D4EAE7373eAb` | `0xCd1430673B0EA81A3c027f13BCb1cC13EDEc6680` |
| 13  | TCUZ-WFTM Sushi LP          | LITE Farmlands - LF#301:TCUZ      | `lpt_coin_usd`        | `0x0B7528b304fA3B89A3D1d2C4B958134512464097` | `0x8B2D8EBb49f1133522E669166E605799DC445f6E` |
| 14  | SunFinance (SUN)            | LITE Farmlands - LF#1010:SUN      | `t_coin_usd`          | `0x60e91f89A2986975822De3BfE50df002Ef46EaAD` | `0x0f907b1C407bABdbaDb57100704c3CB8CDD9Db01` |
| 15  | SUN-FTM Spirit LP           | LITE Farmlands - LF#1011:SUN      | `lpt_coin_usd`        | `0xdAaca3CA5974626E7BB18B2f2245438e04d128f1` | `0x8B759517f13337e351E0E715D5fa7De2c5c4388d` |
| 16  | SunFinance (SUN)            | LITE Farmlands - LF#1012:Nova     | `t_coin_usd`          | `0x60e91f89A2986975822De3BfE50df002Ef46EaAD` | `0x16e62E0227E9de7481817df74717d0ea72b8490C` |
| 17  | Nova-WFTM Spooky LP         | LITE Farmlands - LF#2001:BLK      | `lpt_coin_usd`        | `0xe493CE1AfDCf079d0b40FF9503D7AB5f1f125477` | `0x05BF8A10a24acB9D61b9b6dd90aeF99FB86A1C7e` |
| 18  | BLK-Nova Spirit LP          | LITE Farmlands - LF#2002:Nova     | `lpt_tt_coin_usd`     | `0x22a38F5fef8623E2F4d9Ba0243cD1bD74dbbDE2C` | `0x397162B32D1Aafe137b434f3f3B05615266E7d33` |
| 19  | SuperNova (Nova)            | LITE Farmlands - LF#2004:BLK      | `t_coin_usd`          | `0xA1Ac4AB0E58Bb6CfDFf5797c83cDBE7cB651f7e5` | `0x345551265a8938472991d60a048cae3625e0cd6d` |
| 20  | BLK-WFTM Spooky LP          | LITE Farmlands - LF#2005:Nova     | `lpt_coin_usd`        | `0x623765857B74Da6F5A52A362d228de7F7859224f` | `0x409FDAde151082444607FfA2Cb1cBFB8358c59Ff` |
| 21  | SST-WFTM Spirit LP          | LITE Farmlands - LF#2006:BLK      | `lpt_coin_usd`        | `0x634c206d44c8B392305fdBBC9263229A7C0a6891` | `0xB5aEd208a908bBAd4Cd8e4308A8Ef9E69E644127` |
| 22  | SuperNova (Nova)            | LITE Farmlands - LF#2007:SUN      | `t_coin_usd`          | `0xA1Ac4AB0E58Bb6CfDFf5797c83cDBE7cB651f7e5` | `0x7e10D986975C9CEe043090D6E8559403D47546f5` |
| 23  | USDC-WFTM Knight LP         | Kompound Protocol - GRAIN#2201    | `e_usd`               | `0xB733654453404AAb46d34E68fF24415F5f588C21` | `0x50e66D1232f272B481F349F01b5C6019896A23e3` |
| 24  | USDC-WFTM Wraith LP         | Kompound Protocol - GRAIN#2301    | `e_usd`               | `` | `` |
| 25  | BOO                         | Kompound Protocol - GRAIN#2502    | `e_usd`               | `` | `` |
| 26  | MIM-WFTM Bomb LP            | Kompound Protocol - GRAIN#2601    | `e_usd`               | `` | `` |
| 27  | USDC-WFTM Spooky LP         | Kompound Protocol - GRAIN#2701    | `e_usd`               | `` | `` |
| 33  | WFTM LP                     | Kompound Protocol - GRAIN#2201    | `e_usd`               | `0x50e66D1232f272B481F349F01b5C6019896A23e3` | `0xB733654453404AAb46d34E68fF24415F5f588C21` |
| 33  | WFTM LP                     | Kompound Protocol - GRAIN#2301    | `e_usd`               | `0xd15d6434aC56007BA85ce89377481964eBDf532a` | `0xc43b6a7ff3929be35cd4297309585e43b51ce0f4` |
| 33  | WFTM LP                     | Kompound Protocol - GRAIN#2303    | `e_usd`               | `0xFe80Ecb1B879f24B08E3Caa74246D4Ae17fbA53B` | `0x017672C6254c8C9593bc3B71F1a97E9ba45E8817` |
| 33  | WFTM LP                     | Kompound Protocol - GRAIN#2401    | `e_usd`               | `0x50e66D1232f272B481F349F01b5C6019896A23e3` | `0xB733654453404AAb46d34E68fF24415F5f588C21` |
| 33  | WFTM LP                     | Kompound Protocol - GRAIN#2502    | `e_usd`               | `0xf29C310D60e87bf54DC973DF73D64a339bb944Cb` | `0x841FAD6EAe12c286d1Fd18d1d525DFfA75C7EFFE` |
| 33  | WFTM LP                     | Kompound Protocol - GRAIN#2601    | `e_usd`               | `0x6eC2Cb84422403e06935ac55910Fa3609F55BCce` | `0x74928bfae5d4de45df48d9652de02ece529e8729` |
| 33  | WFTM LP                     | Kompound Protocol - GRAIN#2602    | `e_usd`               | `0x00bedBdD440ff2eFEC3A6a42230e8D3Bfac63d63` | `0x8264f247e4571e2879a05d5d2115c26406c0bc2b` |
| 33  | WFTM LP                     | Kompound Protocol - GRAIN#2607    | `e_usd`               | `0xC7d89a0aA32eb496222f88fA1193566C761b7681` | `0xbef5ea523ca88abb821d47a4bd872d66104ff3f5` |
| 33  | WFTM LP                     | Kompound Protocol - GRAIN#2608    | `e_usd`               | `0xD42C91A330425858BFD78e291365E1b41f56a2Ff` | `0x82c40B555f2dbb6704f214d984da3efdDE64711C` |
| 33  | WFTM LP                     | Kompound Protocol - GRAIN#2609    | `e_usd`               | `0x15FcCE81d8f5B4847e0F65243BFDA85972c98474` | `0x874bB203aBb6AB8A791b56277B680c555f29aB1c` |
| 33  | WFTM LP                     | Kompound Protocol - GRAIN#2610    | `e_usd`               | `0x2b5005f9F08f8A899c7186BD90071da4a131dD46` | `0xDe8908Bc8aA9Fe4515079E2Dbc9380f659dFAd62` |
| 33  | WFTM LP                     | Kompound Protocol - GRAIN#2701    | `e_usd`               | `0x5E62e97A73258947e1745071Ba342C6169A25E80` | `0x2b4C76d0dc16BE1C31D4C1DC53bF9B45987Fc75c` |
| 33  | WFTM LP                     | Kompound Protocol - GRAIN#2901    | `e_usd`               | `0xfD5d0aB5404dd472975922501f670d194732577B` | `0x76e0c9e6f98b27f11ff3735388f982aed1de72c9` |
| 44  | USDC (WEVE)                 | Kompound Protocol - GRAIN#4101    | `e_usd`               | `0xD7627edF607C49F525212fC09d650A91a9B222e1` | `WFTM` |
| 44  | USDC (WEVE)                 | Kompound Protocol - GRAIN#4101    | `e_usd`               | `0x1b70E038f9eC9A8f979B4e6D8CD0Dc85df677CB2` | `ETH	` |
| 44  | USDC (WEVE)                 | Kompound Protocol - GRAIN#4101    | `e_usd`               | `0x48b628ac7f6fa84298c6b3198130c2068073ab01` | `YFI	` |
| 44  | USDC (WEVE)                 | Kompound Protocol - GRAIN#4101    | `e_usd`               | `0xd072046b0928b9Eb6B2Afa9D80cbDFE759Ef3A8B` | `USDC` |
| 44  | USDC (WEVE)                 | Kompound Protocol - GRAIN#4101    | `e_usd`               | `0x69B83634B6E7C2bfFAb8B1ae3B8498d2dab6D51f` | `MIM	` |
| 44  | USDC (WEVE)                 | Kompound Protocol - GRAIN#4101    | `e_usd`               | `0x2938F27687Ae2ad54db2B91B4B836B6ADD15AC8f` | `FRAX` |
| 44  | USDC (WEVE)                 | Kompound Protocol - GRAIN#4101    | `e_usd`               | `0xe125C9c6560c17f4dF8774dB6B9e5d2b3BF9947f` | `LP		` |
| 44  | USDC (OXD)                  | Kompound Protocol - GRAIN#4101    | `e_usd`               | `0xA2B1f90A6CF0FD5451E0fE7ED67331EC15Bd1aAB` | `FTM	` |
| 44  | USDC (OXD)                  | Kompound Protocol - GRAIN#4101    | `e_usd`               | `0x27881D9Ee5F4769AdE8762E93c503D3a7C59769e` | `ETH	` |
| 44  | USDC (OXD)                  | Kompound Protocol - GRAIN#4101    | `e_usd`               | `0xC255FCEFf6967B30E1A467FA4e97560ae5fE54bA` | `BTC	` |
| 44  | USDC (OXD)                  | Kompound Protocol - GRAIN#4101    | `e_usd`               | `0x27DaBA6E82A23C5f9C264257b417D3b99435469d` | `USDC` |
| 44  | USDC (OXD)                  | Kompound Protocol - GRAIN#4101    | `e_usd`               | `0x8885dAa97a0A6590740B6139FD81613D5A543C20` | `DAI	` |
| 44  | USDC (OXD)                  | Kompound Protocol - GRAIN#4101    | `e_usd`               | `0xa638Fe74968c9B95E2E3868f9487390087Ef80aC` | `MIM	` |
| 44  | USDC (OXD)                  | Kompound Protocol - GRAIN#4101    | `e_usd`               | `0x2E24ABF15ECdA2D58E9840456D397CfbA30c9895` | `LQDR` |
| 44  | USDC (OXD)                  | Kompound Protocol - GRAIN#4101    | `e_usd`               | `0x4b7bfaF14a961D0033a2f65d07523b8321D7e477` | `TOMB` |


----
----
----

*Following sections are not up-to-date. Please refer above tables for Asset & Pool Contract's details.*

----
----
----

## Banks : By Module
### `coin_usd`
For native FTM locked in a contract, with price sourced from an FTM-USDC Spookyswap pool.

**1. BO#1 FTMUSD 3-day Call/Put Option**
Current FTM Locked in the 3-day Binary Options Contract.

| Key | Value | Description |
| --- | --- | --- |
| `asset` | `0x92679257ecA3c3Dba25b777185EB82cD81991e72` | BO#1 [FTMUSD 3-day](https://ftm.guru/bo/1)

**2. Degam - Micro JackPot**
Current FTM Locked in the Micro Jackpot.

| Key | Value | Description |
| --- | --- | --- |
| `asset` | `0x21eE31ea0e5B4628aC3c1b2Ec6602aeB60d8D124` | Degam [Micro Jackpot](https://ftm.guru/degam)

**3. Degam - Mini JackPot**
Current FTM Locked in the Mini Jackpot.

| Key | Value | Description |
| --- | --- | --- |
| `asset` | `0x9A6eb015aebC6466d407d40D278894bc773bd009` | Degam [Mini Jackpot](https://ftm.guru/degam)

**4. FTM Coin-Flip**
Current FTM Locked in the FTM Coin-Flip contract.

| Key | Value | Description |
| --- | --- | --- |
| `asset` | `0xC318D7be0f170C0Cc446D2d62132180367956591` | Casino [FTM Coin-Flip](https://ftm.guru/cointoss_1)
  

### `t_coin_usd`
For simple tokens locked in a contract, with price sourced from an FTM pool.

**1. XELITE Pool**
ELITE staked in XELITE.

| Key | Value | Description |
| --- | --- | --- |
| `asset` | `0xf43cc235e686d7bc513f53fbffb61f760c3a1882` | ELITE Token |
| `dec` | 18 | Decimals in Asset |
| `pool` | `0x1BE23c78038B6057172848534AcD62667fA2620d` | XELITE Contract - [ftm.guru/xelite](https://ftm.guru/xelite) |
| `lp` | `0xea035a13b64cb49d85e2f0a2736c9604cb21599c` |  ELITE-WFTM SpLP : Spookyswap Liquidity Token |

### `lpt_coin_usd`
For Liquidity tokens locked in a contract, with price sourced from valuation of an FTM-base pool.

**1. Sushi YieldState**

| Key | Value | Description |
| --- | --- | --- |
| `asset` | `0x50576ed9d94cf934bc32abf76e08ec6ddcd54bf0` | ELITE-WFTM SLP : Sushiswap Liquidity Token |
| `dec` | 18 | Decimals in Asset |
| `pool` | `0xef66a11788a3b3180be4aa31a5743c6a6e87a555` | Farm : YieldState#1 - [ftm.guru/YS/1](https://ftm.guru/YS/1) |
| `lp` | `0x50576ed9d94cf934bc32abf76e08ec6ddcd54bf0` |  ELITE-WFTM SLP : Sushiswap Liquidity Token |

**2. Spooky YieldState**

| Key | Value | Description |
| --- | --- | --- |
| `asset` | `0xea035a13b64cb49d85e2f0a2736c9604cb21599c` | ELITE-WFTM SpLP : Spookyswap Liquidity Token |
| `dec` | 18 | Decimals in Asset |
| `pool` | `0xad70c7cbc8f856681b4ebdd37aeac58cf7100736` | Farm : YieldState#2 - [ftm.guru/YS/2](https://ftm.guru/YS/2) |
| `lp` | `0xea035a13b64cb49d85e2f0a2736c9604cb21599c` |  ELITE-WFTM SpLP : Spookyswap Liquidity Token |



### Finding ftm.guru's TVL via adapter
 - Self-Reporting with on-chain verfied Source
 - Returns T.V.L. denominated in USD.
 - Value is extended with 18 digits such that:
 - tvl=1000000000000000000 implies $1 in TVL.
  
### Inheritable Solidity Interface

```
interface ITVL{
	function tvl() external view returns(uint256);
}
```

### A.B.I. for Polling Data
`[{"inputs":[],"stateMutability":"nonpayable","type":"constructor"},{"inputs":[],"name":"DAO","outputs":[{"internalType":"address payable","name":"","type":"address"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"uint256","name":"","type":"uint256"}],"name":"_bankOf_coin","outputs":[{"internalType":"address","name":"","type":"address"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"uint256","name":"","type":"uint256"}],"name":"_bankOf_e_usd","outputs":[{"internalType":"address","name":"","type":"address"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"uint256","name":"","type":"uint256"}],"name":"_bankOf_lpt_coin_usd","outputs":[{"internalType":"address","name":"asset","type":"address"},{"internalType":"address","name":"pool","type":"address"},{"internalType":"uint8","name":"dec","type":"uint8"},{"internalType":"address","name":"lp","type":"address"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"uint256","name":"","type":"uint256"}],"name":"_bankOf_lpt_tt_coin_usd","outputs":[{"internalType":"address","name":"asset","type":"address"},{"internalType":"address","name":"pool","type":"address"},{"internalType":"uint8","name":"dec","type":"uint8"},{"internalType":"address","name":"lp_tt","type":"address"},{"internalType":"address","name":"lp_bt_f","type":"address"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"uint256","name":"","type":"uint256"}],"name":"_bankOf_lpt_tt_usd","outputs":[{"internalType":"address","name":"asset","type":"address"},{"internalType":"address","name":"pool","type":"address"},{"internalType":"uint8","name":"dec","type":"uint8"},{"internalType":"address","name":"lp_tt","type":"address"},{"internalType":"address","name":"lp_bt_u","type":"address"},{"internalType":"address","name":"u","type":"address"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"uint256","name":"","type":"uint256"}],"name":"_bankOf_lpt_usd","outputs":[{"internalType":"address","name":"asset","type":"address"},{"internalType":"address","name":"pool","type":"address"},{"internalType":"uint8","name":"dec","type":"uint8"},{"internalType":"address","name":"u","type":"address"},{"internalType":"address","name":"lp","type":"address"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"uint256","name":"","type":"uint256"}],"name":"_bankOf_t_coin_usd","outputs":[{"internalType":"address","name":"asset","type":"address"},{"internalType":"address","name":"pool","type":"address"},{"internalType":"uint8","name":"dec","type":"uint8"},{"internalType":"address","name":"lp","type":"address"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"uint256","name":"","type":"uint256"}],"name":"_bankOf_t_tt_coin_usd","outputs":[{"internalType":"address","name":"asset","type":"address"},{"internalType":"address","name":"pool","type":"address"},{"internalType":"uint8","name":"dec","type":"uint8"},{"internalType":"address","name":"lp_tt","type":"address"},{"internalType":"address","name":"lp_bt_f","type":"address"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"uint256","name":"","type":"uint256"}],"name":"_bankOf_t_tt_usd","outputs":[{"internalType":"address","name":"asset","type":"address"},{"internalType":"address","name":"pool","type":"address"},{"internalType":"uint8","name":"dec","type":"uint8"},{"internalType":"address","name":"lp_tt","type":"address"},{"internalType":"address","name":"lp_bt_u","type":"address"},{"internalType":"address","name":"u","type":"address"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"uint256","name":"","type":"uint256"}],"name":"_bankOf_t_usd","outputs":[{"internalType":"address","name":"asset","type":"address"},{"internalType":"address","name":"pool","type":"address"},{"internalType":"uint8","name":"dec","type":"uint8"},{"internalType":"address","name":"u","type":"address"},{"internalType":"address","name":"lp","type":"address"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"uint256[]","name":"_e_usd","type":"uint256[]"},{"internalType":"uint256[]","name":"_coin_usd","type":"uint256[]"},{"internalType":"uint256[]","name":"_t_usd","type":"uint256[]"},{"internalType":"uint256[]","name":"_t_coin_usd","type":"uint256[]"},{"internalType":"uint256[]","name":"_t_tt_usd","type":"uint256[]"},{"internalType":"uint256[]","name":"_t_tt_coin_usd","type":"uint256[]"},{"internalType":"uint256[]","name":"_lpt_usd","type":"uint256[]"},{"internalType":"uint256[]","name":"_lpt_coin_usd","type":"uint256[]"},{"internalType":"uint256[]","name":"_lpt_tt_usd","type":"uint256[]"},{"internalType":"uint256[]","name":"_lpt_tt_coin_usd","type":"uint256[]"}],"name":"_puBankOf_pool2_usd","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"uint256[]","name":"_e_usd","type":"uint256[]"},{"internalType":"uint256[]","name":"_coin_usd","type":"uint256[]"},{"internalType":"uint256[]","name":"_t_usd","type":"uint256[]"},{"internalType":"uint256[]","name":"_t_coin_usd","type":"uint256[]"},{"internalType":"uint256[]","name":"_t_tt_usd","type":"uint256[]"},{"internalType":"uint256[]","name":"_t_tt_coin_usd","type":"uint256[]"},{"internalType":"uint256[]","name":"_lpt_usd","type":"uint256[]"},{"internalType":"uint256[]","name":"_lpt_coin_usd","type":"uint256[]"},{"internalType":"uint256[]","name":"_lpt_tt_usd","type":"uint256[]"},{"internalType":"uint256[]","name":"_lpt_tt_coin_usd","type":"uint256[]"}],"name":"_puBankOf_staking_usd","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"uint256","name":"n","type":"uint256"}],"name":"_pullBankOf_coin","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"uint256","name":"n","type":"uint256"}],"name":"_pullBankOf_e_usd","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"uint256","name":"n","type":"uint256"}],"name":"_pullBankOf_lpt_coin_usd","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"uint256","name":"n","type":"uint256"}],"name":"_pullBankOf_lpt_tt_coin_usd","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"uint256","name":"n","type":"uint256"}],"name":"_pullBankOf_lpt_tt_usd","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"uint256","name":"n","type":"uint256"}],"name":"_pullBankOf_lpt_usd","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"uint256","name":"n","type":"uint256"}],"name":"_pullBankOf_t_coin_usd","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"uint256","name":"n","type":"uint256"}],"name":"_pullBankOf_t_tt_coin_usd","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"uint256","name":"n","type":"uint256"}],"name":"_pullBankOf_t_tt_usd","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"uint256","name":"n","type":"uint256"}],"name":"_pullBankOf_t_usd","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"address","name":"asset","type":"address"}],"name":"_pushBankOf_coin","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"address","name":"asset","type":"address"}],"name":"_pushBankOf_e_usd","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"address","name":"asset","type":"address"},{"internalType":"address","name":"pool","type":"address"},{"internalType":"uint8","name":"dec","type":"uint8"},{"internalType":"address","name":"lp","type":"address"}],"name":"_pushBankOf_lpt_coin_usd","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"address","name":"asset","type":"address"},{"internalType":"address","name":"pool","type":"address"},{"internalType":"uint8","name":"dec","type":"uint8"},{"internalType":"address","name":"lp_tt","type":"address"},{"internalType":"address","name":"lp_bt_f","type":"address"}],"name":"_pushBankOf_lpt_tt_coin_usd","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"address","name":"asset","type":"address"},{"internalType":"address","name":"pool","type":"address"},{"internalType":"uint8","name":"dec","type":"uint8"},{"internalType":"address","name":"lp_tt","type":"address"},{"internalType":"address","name":"lp_bt_u","type":"address"},{"internalType":"address","name":"u","type":"address"}],"name":"_pushBankOf_lpt_tt_usd","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"address","name":"asset","type":"address"},{"internalType":"address","name":"pool","type":"address"},{"internalType":"uint8","name":"dec","type":"uint8"},{"internalType":"address","name":"u","type":"address"},{"internalType":"address","name":"lp","type":"address"}],"name":"_pushBankOf_lpt_usd","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"address","name":"asset","type":"address"},{"internalType":"address","name":"pool","type":"address"},{"internalType":"uint8","name":"dec","type":"uint8"},{"internalType":"address","name":"lp","type":"address"}],"name":"_pushBankOf_t_coin_usd","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"address","name":"asset","type":"address"},{"internalType":"address","name":"pool","type":"address"},{"internalType":"uint8","name":"dec","type":"uint8"},{"internalType":"address","name":"lp_tt","type":"address"},{"internalType":"address","name":"lp_bt_f","type":"address"}],"name":"_pushBankOf_t_tt_coin_usd","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"address","name":"asset","type":"address"},{"internalType":"address","name":"pool","type":"address"},{"internalType":"uint8","name":"dec","type":"uint8"},{"internalType":"address","name":"lp_tt","type":"address"},{"internalType":"address","name":"lp_bt_u","type":"address"},{"internalType":"address","name":"u","type":"address"}],"name":"_pushBankOf_t_tt_usd","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"address","name":"asset","type":"address"},{"internalType":"address","name":"pool","type":"address"},{"internalType":"uint8","name":"dec","type":"uint8"},{"internalType":"address","name":"u","type":"address"},{"internalType":"address","name":"lp","type":"address"}],"name":"_pushBankOf_t_usd","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"uint256","name":"n","type":"uint256"}],"name":"_tvlOf_coin_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"uint256","name":"n","type":"uint256"}],"name":"_tvlOf_e_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"uint256","name":"n","type":"uint256"}],"name":"_tvlOf_lpt_coin_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"uint256","name":"n","type":"uint256"}],"name":"_tvlOf_lpt_tt_coin_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"uint256","name":"n","type":"uint256"}],"name":"_tvlOf_lpt_tt_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"uint256","name":"n","type":"uint256"}],"name":"_tvlOf_lpt_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"_tvlOf_pool2_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"_tvlOf_staking_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"uint256","name":"n","type":"uint256"}],"name":"_tvlOf_t_coin_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"uint256","name":"n","type":"uint256"}],"name":"_tvlOf_t_tt_coin_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"uint256","name":"n","type":"uint256"}],"name":"_tvlOf_t_tt_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"uint256","name":"n","type":"uint256"}],"name":"_tvlOf_t_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"_tvl_coin_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"_tvl_e_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"_tvl_lpt_coin_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"_tvl_lpt_tt_coin_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"_tvl_lpt_tt_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"_tvl_lpt_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"_tvl_pool2_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"_tvl_staking_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"_tvl_t_coin_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"_tvl_t_tt_coin_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"_tvl_t_tt_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"_tvl_t_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"coinusd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"address","name":"lp","type":"address"}],"name":"p_lpt_coin_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"address","name":"bt","type":"address"},{"internalType":"address","name":"lp_tt","type":"address"},{"internalType":"address","name":"lp_bt_f","type":"address"}],"name":"p_lpt_tt_coin_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"address","name":"bt","type":"address"},{"internalType":"address","name":"lp_tt","type":"address"},{"internalType":"address","name":"lp_bt_u","type":"address"},{"internalType":"address","name":"u","type":"address"}],"name":"p_lpt_tt_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"address","name":"u","type":"address"},{"internalType":"address","name":"lp","type":"address"}],"name":"p_lpt_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"address","name":"lp","type":"address"}],"name":"p_t_coin_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"address","name":"qt","type":"address"},{"internalType":"address","name":"lp_tt","type":"address"},{"internalType":"address","name":"lp_bt_f","type":"address"}],"name":"p_t_tt_coin_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"address","name":"qt","type":"address"},{"internalType":"address","name":"lp_tt","type":"address"},{"internalType":"address","name":"lp_bt_u","type":"address"},{"internalType":"address","name":"u","type":"address"}],"name":"p_t_tt_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"address","name":"u","type":"address"},{"internalType":"address","name":"lp","type":"address"}],"name":"p_t_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"pool2","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"address","name":"tokenAddress","type":"address"},{"internalType":"uint256","name":"tokens","type":"uint256"}],"name":"rescue","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[],"name":"reset","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"address","name":"u","type":"address"},{"internalType":"address","name":"w","type":"address"},{"internalType":"address","name":"l","type":"address"}],"name":"setUW","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[],"name":"staking","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"tvl","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"address","name":"q","type":"address"}],"name":"tvlOf_coin_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"address","name":"q","type":"address"}],"name":"tvlOf_e_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"components":[{"internalType":"address","name":"asset","type":"address"},{"internalType":"address","name":"pool","type":"address"},{"internalType":"uint8","name":"dec","type":"uint8"},{"internalType":"address","name":"lp","type":"address"}],"internalType":"struct tvlGuru.lpt_coin_usd","name":"q","type":"tuple"}],"name":"tvlOf_lpt_coin_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"components":[{"internalType":"address","name":"asset","type":"address"},{"internalType":"address","name":"pool","type":"address"},{"internalType":"uint8","name":"dec","type":"uint8"},{"internalType":"address","name":"lp_tt","type":"address"},{"internalType":"address","name":"lp_bt_f","type":"address"}],"internalType":"struct tvlGuru.lpt_tt_coin_usd","name":"q","type":"tuple"}],"name":"tvlOf_lpt_tt_coin_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"components":[{"internalType":"address","name":"asset","type":"address"},{"internalType":"address","name":"pool","type":"address"},{"internalType":"uint8","name":"dec","type":"uint8"},{"internalType":"address","name":"lp_tt","type":"address"},{"internalType":"address","name":"lp_bt_u","type":"address"},{"internalType":"address","name":"u","type":"address"}],"internalType":"struct tvlGuru.lpt_tt_usd","name":"q","type":"tuple"}],"name":"tvlOf_lpt_tt_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"components":[{"internalType":"address","name":"asset","type":"address"},{"internalType":"address","name":"pool","type":"address"},{"internalType":"uint8","name":"dec","type":"uint8"},{"internalType":"address","name":"u","type":"address"},{"internalType":"address","name":"lp","type":"address"}],"internalType":"struct tvlGuru.lpt_usd","name":"q","type":"tuple"}],"name":"tvlOf_lpt_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"components":[{"internalType":"address","name":"asset","type":"address"},{"internalType":"address","name":"pool","type":"address"},{"internalType":"uint8","name":"dec","type":"uint8"},{"internalType":"address","name":"lp","type":"address"}],"internalType":"struct tvlGuru.t_coin_usd","name":"q","type":"tuple"}],"name":"tvlOf_t_coin_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"components":[{"internalType":"address","name":"asset","type":"address"},{"internalType":"address","name":"pool","type":"address"},{"internalType":"uint8","name":"dec","type":"uint8"},{"internalType":"address","name":"lp_tt","type":"address"},{"internalType":"address","name":"lp_bt_f","type":"address"}],"internalType":"struct tvlGuru.t_tt_coin_usd","name":"q","type":"tuple"}],"name":"tvlOf_t_tt_coin_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"components":[{"internalType":"address","name":"asset","type":"address"},{"internalType":"address","name":"pool","type":"address"},{"internalType":"uint8","name":"dec","type":"uint8"},{"internalType":"address","name":"lp_tt","type":"address"},{"internalType":"address","name":"lp_bt_u","type":"address"},{"internalType":"address","name":"u","type":"address"}],"internalType":"struct tvlGuru.t_tt_usd","name":"q","type":"tuple"}],"name":"tvlOf_t_tt_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"components":[{"internalType":"address","name":"asset","type":"address"},{"internalType":"address","name":"pool","type":"address"},{"internalType":"uint8","name":"dec","type":"uint8"},{"internalType":"address","name":"u","type":"address"},{"internalType":"address","name":"lp","type":"address"}],"internalType":"struct tvlGuru.t_usd","name":"q","type":"tuple"}],"name":"tvlOf_t_usd","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"usd","outputs":[{"internalType":"address","name":"","type":"address"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"usd_d","outputs":[{"internalType":"uint8","name":"","type":"uint8"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"wcoin","outputs":[{"internalType":"address","name":"","type":"address"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"wcoinusd","outputs":[{"internalType":"address","name":"","type":"address"}],"stateMutability":"view","type":"function"}]`

## Contact Us:
[https://discord.com/invite/QpyfMarNrV](https://discord.com/invite/QpyfMarNrV)
