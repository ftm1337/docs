---

title: Contracts
grand_parent:
parent: 🍑 Thick
has_children:
nav_order:

---

# On Chain
> Thick runs on multiple blockchain networks!

Thick contract addresses are chain agnostic and current support the following Networks

## Networks
This is the core contract responsible for creating a 'liquidity **pool**' for a '**pair**' of tokens. A 'pair' can have multiple pools!

Blockchain         | Network          | Gas  | Chain ID      | Network ID
------------------ | ---------------- | ---- | ------------- | ------------
Fantom             | Opera            | FTM  | `0x`FA        | 250
Arbitrum           | One              | ETH  | `0x`A4B1      | 42161
XDAI Chain         | Gnosis           | XDAI | `0x`64        | 250
Base               | Mainnet          | ETH  | `0t`BA_E      | 42161
Sonic              | Sonic            | S    | `0x`92        | 146

## Liquidity & Management
### V2 Addresses - 2THICK
```
All "2Thick" addresses are Same on Base, Fantom & Sonic
- `0x7Ca1dCCFB4f49564b8f13E18a67747fd428F1C40` = v3CoreFactory
- `0x9B500c0a544B870D9C4c441147dCaEf599e542E7` = multicall2
- `0x30f45DEfBbce0030eE14F9E08D36102115e5CE3b` = proxyAdmin
- `0x547DB6759B0aF9e050855106993e3CEFC16E937E` = tickLens
- `0x79C26D7AC184BB9C453B996475F484668E516dE5` = nonfungibleTokenPositionManager
- `0xc701e92Db1Ef14AB64f66F18536b1E07678dB678` = quoterV2
- `0xE4Ba08712C404042b8EEfC3fdF3b603c977500dF` = swapRouter02
```

### V1 Addresses

Artifact    | Smart Contract Address
----------- | ------------------------------------------
Factory     | 0xE6dA85feb3B4E0d6AEd95c41a125fba859bB9d24
Multicall   | 0x4c29682a07c50dD5F6BdF36EB97fb28F5C1681E3
Proxy Admin | 0x687dad08623C88452a5deB3A4482c979fA3F571E
Tick Lens   | 0xb80a72281c76464CC0e1FbF2431A897393E0d757
ArtLibrary  | 0x97A7B2f95FDa7181dA16aec3072cD55a58D85073
Art         | 0x6bD73537da943723124C2A50F0f95557f4aCC9A2
Art Proxy   | 0x4bfb3993733b13bba2376e56f9d7ffaf56e047cf
NFT Manager | 0x2B52294425a9a229322228de659eDE9D146D7c2f
Quoter      | 0xF5B7181877FeAB982A4b49a99E84BB7cBEBEFF98
Router      | 0x1F7A12B40bFc8e8561008Bc2ca1FBdc71A36d0e8



### Fees Synthesizers

Network  | Fee-Tier | Pairing      | Synthesizer Smart Contract Address
-------- | -------- | ------------ | -----------------------------------
Fantom   | 30 bps   | WFTM/lzUSDC  |
Arbitrum | 5 bps    | WETH/USDC    |
Base     | 5 bps    | WETH/USDC    |

