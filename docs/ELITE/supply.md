---

title: Supply Distribution
grand_parent:
parent: ELITE, Our Token
has_children:
nav_order: 3
author: "FTM1337"
date: "Dec. 1st, 2021"

---

<h1 align="center"> Supply Distribution of ELITE</h1>

| 🔎 [ftmscan](https://ftmscan.com/token/0xf43Cc235E686d7BC513F53Fbffb61F760c3a1882) | [CoinMarketCap](https://coinmarketcap.com/currencies/elite-1337) | [CoinGecko](https://www.coingecko.com/coins/elite-1337) | [Nomics](https://nomics.com/assets/elite2-ftmguru) |

This document attempts to address how the 1337 ELITEs are distributed.  
_^ implies approximation._
### API Endpoint
[https://ftm.guru/rawdata/supplies.json](https://ftm.guru/rawdata/supplies.json)

## Overview
### Max Supply = 1337 ELITE
- The theoretical maximum number of ELITE that can ever exist together.
- Includes each and every ELITE.

### Total Supply = 1336.9999 ELITE
- The present number of total ELITEs in existence.
- Excludes the ELITE burned directly by the Protocol's burn function.

### Current Supply = 250^
- Includes only the ELITE that can be accessed by general public
- Excludes Protocol Reserve (671 ELITE)
- Excludes ELITEs considered burnt.
- Excludes Team Tokens (13.37 ELITE)
- Excludes E..L.I.T.E. D.A.O. Treasury (12 ELITE)

### Burned Supply
- Includes ELITE burned directly by the Protocol's burn function. (<0.1 ELITE)
- Includes ELITE burned directly to "Zero-addresses" (>17 ELITE)
  - Burns by Voting
  - Burns by Taxation
  - Other burns to
    - "Zero-address" : `0x0000000000000000000000000000000000000000`
    - "Dead-address" : `0x000000000000000000000000000000000000DEAD`
    - "Dead-Elite address" : `0x00000000000000000000000000000000DEAD1337`

## Calculations
- `CALL:f()` format notation implies calling the ELITE Smart Contract's specified view-function.
Call `0xf43Cc235E686d7BC513F53Fbffb61F760c3a1882` on Chain-ID `0xFA` (250:Fantom Opera).
- Following notation implies adding ("plus") or subtracting ("minus") the ELITE balances at the specific addresses.
i.e.  `CALL:balanceOf(<specific-address-here>)`

### Max Supply
1337
### Total Supply
`CALL:totalSupply()`
### Circulating Supply
`CALL:totalSupply()`  
  minus `0x5c146cd18fa53914580573c9b9604588529406ca`  
  minus `0x74BFb7E94bEf5767F5F6Ace2D0df73a224ADB689`  
  minus `0xbab9645d1B78425A7e4e9e78E8DD32aAbd800a16`  
  minus `0x167D87A906dA361A10061fe42bbe89451c2EE584`  
  minus `0x0000000000000000000000000000000000000000`  
### Unreserved Supply
`CALL:circulatingSupply()`
### Burned Supply
1337
minus `CALL:totalSupply()`
plus `0x0000000000000000000000000000000000000000`  
plus `0x000000000000000000000000000000000000dEaD`  
plus `0x000000000000000000000000000000001337dEaD`  

## Special Addresses
### Protocol Reserve & Genesis Address
`0xbab9645d1B78425A7e4e9e78E8DD32aAbd800a16`
#### Purupose:
- Create ELITE
- Set-up the "KingMaker"
- Manage the Protocol Reserve
- Special transactions to smart contracts
  - To exceed holding limit (8.9 ELITE)
  - To seed farms with Rewards tax-free

### Official Dev-Team Address
`0x5C146cd18fa53914580573C9b9604588529406Ca`
#### Purpose:
- Deploy all Offical Smart Contracts for Guru Network
- Queue timelocked transactions

### E.L.I.T.E. D.A.O. Treasury
`0x167D87A906dA361A10061fe42bbe89451c2EE584`
#### Purpose:
- Collect all Protocol Taxes
- Collect all Protocol Fees
- Hold & Manage the treasury
- Manage all DAO-owned Smart Contracts
- Queue timelocked transactions for all DAO-owned Smart Contracts

### Publicly-Extensible Infinite Timelock
`0x74BFb7E94bEf5767F5F6Ace2D0df73a224ADB689`
#### Purpose:
- Special timelocking concept invented by ftm.guru.
- A contract that can lock the ELITE tokens held by it for an infinite duration of time.
- Anyone can freely call the "`relock`" function on it to extend the timelock further.
- These ELITE were originally supposed to be added as liquidity to 3 more DEXes (133.7 ELITE each), but the community voiced its opinion against it.
Ever since, they have been staying timelocked.
- Will be upgraded in future to incentivise public `relock`ing

## XELITE
`0x1BE23c78038B6057172848534AcD62667fA2620d`
- Interest Bearing ELITE
- Earn a small yet stable passive income for holding ELITE
- https://ftm.guru/xelite

## Known DEX Smart Contracts
#### SpookySwap : WFTM + ELITE
`0xea035a13b64cb49d85e2f0a2736c9604cb21599c`
#### Sushi : WFTM + ELITE
`0x50576ed9d94cf934bc32abf76e08ec6ddcd54bf0`
#### SpiritSwap : WFTM + ELITE
`0x7c8f47d2d151cedfdb847ab3c5b67d05daf3539b`
#### ZooDEX : WFTM + ELITE
`0xad28B6C529714954AE2B6d390c8eaD874ddc4970`
#### ZooDEX : ZOO + ELITE
`0x7618793c51e0dc954ba1dd2eeeb3dfa08f777d0a`
#### Sushi : USDC + ELITE
`0x1dfcddf675038ead27f1d75b435b5b05ba825e9a`
#### SpookySwap : USDC + ELITE
`0x20DD18EcA4Bd91B4d23534603D836174Fd5123c9`
#### Elk DEX : WFTM + ELITE
`0xf25417182FbfdEbf1a92142b31A1B32135f1Fd60`
#### Elk DEX : USDC + ELITE
`0xDeC1a7eF080B22fEe247aCD033a8Aca8666bDdcb`
#### ShibaSwap : WFTM + ELITE
`0x0652Dec650566439CFFEB4BEb201F062fc13243F`
#### ShibaSwap : USDC + ELITE
`0xe2121F534316CD3fc91E70a39AAa25785e1c20C1`
#### NipdEX : WFTM + ELITE
`0x736c1462feEc9D936dF0B99F4BE5eD019118534a`
#### HyperJump : WFTM + ELITE
`0xdc79C700EeDc83bE8d19Ad2d245717c7539DFA1c`
#### CyberSwap : WFTM + ELITE
`0x2668141243eCbFEb1b7556D5F08c11Bd94d9b6db`
#### PaintSwap : WFTM + ELITE
`0xF33c436E3C1f0AD9EcB400aA28183910585eFe21`
#### TotemSwap : WFTM + ELITE
`0x6511D0222D90A1135A755c9AC643b862824c79F6`
#### SoulSwap : WFTM + ELITE
`0xE03a36ceC8E6A5cdE1Dae1dd10A5131683F53C3A`
#### WraithSwap : WFTM + ELITE
`0x5817Edb6378B58Bcc9405C864191EB869F7CEc66`
#### SpiritSwap : SUN + ELITE
`0xf91c58d3b908831461b462D341271959e0Aec34D`
#### WraithSwap : WRA + ELITE
`0x0Ec3f086C8be2efc1bE8C1480C6d48E9b42b816a`
#### EmpireDEX : USDC + ELITE
`0x1218a2F1CE880c01D174C6b1AEb7f2115A152Fa1`
#### WraithSwap : USDC + ELITE
`0x2221b4ed9d5f2a706f6bf4fcd40ee36da88d2476`
#### EmpireDEX : USDC + ELITE
`0x7808640c1127B31764d549c7Cf0d0bCbA599f7B4`
#### Kyber-DMM : USDC + ELITE
`0xba293BeBB30CB8Aa144CB6246ed0cDC1232e12fF`
#### Kyber-DMM : USDC + ELITE
`0x2AFb5E33Dd34C6dA03d64444721251B7D17D15BE`
#### Dfyn : WFTM + ELITE
`0x8E6f0C6c4D3Ad3606001b1C918e8C45Ffbb8678D`
#### MorpheusSwap : USDC + ELITE
`0x0068ecb52df9ca8D9e25f38A7370F54B9F413a48`
#### SpookySwap : DAI + ELITE
`0x6B3AF21Cb0aED1C9C91b48a5afb60D412468811a`
#### SpookySwap : WETH + ELITE
`0xB70c24D275caC060f357C0AEf163B99B6dee24F5`
#### SpookySwap : UST + ELITE
`0x6906976bf20102611D723379d4E83e2b985fb823`
#### SpiritSwap : SPIRIT + ELITE
`0xad70c7cbc8f856681b4ebdd37aeac58cf7100736`

## Known Yield-bearing Smart Contracts containing ELITE

|Farm|Uses|From|Gives|Smart Contract Address|
|----|----|----|----|----|
|[↗ ftm.guru YieldState 1](https://ftm.guru/YS/1)|ELITE-FTM LP|Sushi|ELITE|`0xeF66A11788a3B3180be4Aa31A5743c6a6e87a555`|
|[↗ ftm.guru YieldState 2](https://ftm.guru/YS/2)|ELITE-FTM LP|SpookySwap|ELITE|`0xAD70c7cBC8f856681b4ebdD37AEAc58cF7100736`|
|[↗ ftm.guru XELITE](https://ftm.guru/xelite)|ELITE| ftm.guru/xelite |ELITE|`0x1BE23c78038B6057172848534AcD62667fA2620d`|
  
## Top-25 Addresses
#### Type-Legend

| Symbol | Meaning |
| ---- | ---- |
| 🔐 | Excluded from Circulating Supply |
| Ⓒ | Included in Circulating Supply |
| 👷 | Team Controlled Address |
| 🖧 | Smart Contract |
| 👤 | Regular User |

#### List of Holders

|	Rank 	|	Address 	|	Type	|	Quantity (Token) 	|	Percentage	|	Description	|
|----|----|----|----|----|----|
|	1	|	0x74bfb7e94bef5767f5f6ace2d0df73a224adb689	|	🖧 🔐	|	384.683723970419758060	|	28.7722%	|	Infinite Timelock	|
|	2	|	0x0000000000000000000000000000000000000000	|	🖧 🔐	|	17.652120461849605950	|	1.3203%	|	Zero-address	|
|	3	|	0x1be23c78038b6057172848534acd62667fa2620d	|	🖧 Ⓒ	|	16.900524787334781976	|	1.2641%	|	XELITE	|
|	4	|	0xea035a13b64cb49d85e2f0a2736c9604cb21599c	|	🖧 Ⓒ	|	16.481926647566076448	|	1.2328%	|	DEX Pair	|
|	5	|	0x5c146cd18fa53914580573c9b9604588529406ca	|	👷 🔐	|	13.370000000000003088	|	1.0000%	|	Development Reserve	|
|	6	|	0x167d87a906da361a10061fe42bbe89451c2ee584	|	👷 🔐	|	12.265640688942309201	|	0.9174%	|	E.L.I.T.E. D.A.O.	|
|	7	|	0xd260c954fcda31917c948a6049a9bee4d4d64ee3	|	👤 Ⓒ	|	8.890616039009351170	|	0.6650%	|	Regular User	|
|	8	|	0x5a08502d88f3fe9a9a60f8914c4eb7924b77ce7f	|	👤 Ⓒ	|	8.889751652926338189	|	0.6649%	|	Regular User	|
|	9	|	0xb09c2a82f73b4e1ab8330dfe4f169d16a6c201fb	|	👤 Ⓒ	|	8.888713209178669973	|	0.6648%	|	Regular User	|
|	10	|	0x50576ed9d94cf934bc32abf76e08ec6ddcd54bf0	|	🖧 Ⓒ	|	8.002021261744614543	|	0.5985%	|	DEX Pair	|
|	11	|	0xdfbf4575f97f409a15d09f61c5ef886fd0b030ff	|	👤 Ⓒ	|	7.965245303540713425	|	0.5958%	|	Regular User	|
|	12	|	0x836e8ff06eca3666519dd7d54d4a5223db4714ae	|	👤 Ⓒ	|	7.879670000000000000	|	0.5894%	|	Regular User	|
|	13	|	0xd580bbb36787efad0f1bc09082f62d17623b5028	|	👤 Ⓒ	|	7.480790947488709469	|	0.5595%	|	Regular User	|
|	14	|	0xa0d7c2576dbdc215cea06cbabb61960d08c6bce8	|	👤 Ⓒ	|	6.908383260000000000	|	0.5167%	|	Regular User	|
|	15	|	0xd0e6862264e6b6f6defe5e7960822507ccd4e081	|	👤 Ⓒ	|	6.161025110162262072	|	0.4608%	|	Regular User	|
|	16	|	0x20dd18eca4bd91b4d23534603d836174fd5123c9	|	🖧 Ⓒ	|	5.976645453000678659	|	0.4471%	|	DEX Pair	|
|	17	|	0xf965ca8db3e227995713f9b1c291c907f7aea0fd	|	👤 Ⓒ	|	5.922443901000000000	|	0.4430%	|	Regular User	|
|	18	|	0x83bf2c65fcdc947e5a746cfcfcfca8216e402cd9	|	👤 Ⓒ	|	5.808310359869135441	|	0.4344%	|	Regular User	|
|	19	|	0xd299f4f826a880501575b3575a510d0c2b13279a	|	👤 Ⓒ	|	4.934531282000000000	|	0.3691%	|	Regular User	|
|	20	|	0x49b7614a7842c6033bfa238481a24f008affdbfd	|	👤 Ⓒ	|	4.927522390010236102	|	0.3686%	|	Regular User	|
|	21	|	0xe2ae9775df097f48ffff4af9318b102a2c53b0eb	|	👤 Ⓒ	|	4.851672764046908445	|	0.3629%	|	Regular User	|
|	22	|	0x426d48d5754cac8b87c1f62069425e1546a0ad64	|	👤 Ⓒ	|	4.649614248857681192	|	0.3478%	|	Regular User	|
|	23	|	0xb70c24d275cac060f357c0aef163b99b6dee24f5	|	🖧 Ⓒ	|	4.260643245235161231	|	0.2915%	|	DEX Pair	|
|	24	|	0xccff9b35ec5d7893ea728e154d3719e27eefca89	|	👤 Ⓒ	|	4.111656563812836293	|	0.3075%	|	Regular User	|
|	25	|	0x90660dae63ee2736a40c38651416868f3876eabc	|	👤 Ⓒ	|	4.100000000000000000	|	0.3067%	|	Regular User	|
