---

title: SWKAVA
grand_parent:
parent: 🔓 Lockless Protocol
has_children:
nav_order:

---

*Note: This documentation might be slightly outdated*

----

# swKAVA
> *Liquid Staking for Kava*

## Why do we need SWKAVA?
Everyone loves to stake KAVA as it provides a handsome yield! Aren't we right, stakers? ;)

### The Lockup
But this process ties up the depositor with an inability to unstake their KAVA quickly. They get locked for 21-days into their position and cannot unfreeze their KAVA. The market is generally too volatile and requires traders to be on their toes and ready to move their assets in tandem with the motions of the market, but bonding their tokens for a long time leaves them helpless against the tempestous market action.

### The exit lane
If the trend of market turns bearish, savvy traders would want to exit their positions as soon as possible. In preparation for such an event, most traders do not like to stake/bond/lock their tokens to stay liquid 24x7 round the clock, waiting to counter any potential downturns.

### Over-speeding penalty
But this strategy is extremely poor in terms of capital-efficiency. These traders sacrifice all the juicy yield Kava has to offer! And these opportunity costs come at the benefit of a "potential but unlikely" scenario of a huge market downturn. The penalty for this over-cautiousness is harsh - it separates you from your darling APY.

## What does SWKAVA do?
What if there was a middle ground? What if we could come close to the lovely APR, without putting ourselves into a lockup?

### The Key: S-wKAVA
SWKAVA offers just this. SWKAVA unlocks the power of your locked KAVA. It makes the value of your Bonded KAVA tradable 24x7.

## What is SWKAVA?
SWKAVA is Staked Kava, wrapped as an ERC20. SWKAVA is not a fork. SWKAVA is an original work of the Guru Network.

Let's see what sets it apart:
### No Locks & No Bondage
SWKAVA has no lockups, no bonding periods and is freely movable across wallets and contracts for free-trade and usage in Decentralized Finance protocols, NFTs, as collateral for lending & borrowing and everything else possible with a token.
### SWKAVA is immutable
SWKAVA treats everyone equal. Nobody can be whitelisted or blacklisted. SWKAVA is fair, uncensorable, unstoppable and sufficiently decentralized.
### Get those Yields
With SWKAVA, you can not just earn KAVA, but a plethora of reward tokens like BTC, ETH, USDC, SWKAVA, WKAVA, OSMO, ATOM, even NFTs and more!
### More than covered
With the advanced tokenomic design, each SWKAVA is always backed implicity by atleast 1 KAVA, at all points.

## Tokenomics
### Fees
- There are NO team allocations
- There is NO fees to stake KAVA
- There is NO commission or performance fee

### Yield Distribution
- All the KAVA earned from the staked KAVA is funneled back to farmers.

## Wait, what!? Farmers?
SWKAVA utlizes an innovative design, first of its kind in the industry. Instead of delivering the yield to KAVA depositors, the multi-token yield is rewarded to the Liquidity Providers of a special SWKAVA/WKAVA "stable" pair.

### Liquidity Pool
The SWKAVA/WKAVA liquidity resides on a special pool, also known as a StableSwap 2pool, made famous by Curve Finance.

## ABcDeFX: The SWKAVA Exchange
ABcDeFX is home to the main Liquidity pool composed of WKAVA + SWKAVA tokens. This DEX has one special pair - The WKAVA/SWKAVA pool.

### Based on Curve.fi V2
- Near-zero slippage trades
- Almost absent price impact
- Audited by numerous independent people
- Battle-tested with hundreds of billions
- Liquidity Providers earn Trade-fees
- Keeps 1 SWKAVA at par with 1 KAVA
- Composable and easy to build upon by other Kava Projects
- Tokenized Liquidity Positions
- Auto-compounding trade-fee APR
- LP tokens usable freely by people and protocols
- Immutable. Uncensorable. Unstoppable.

### Single-sided liquidity
Our design embraces single-token liquidity addition to streamline the process for all of our Kava users. Liquidity can be added in either of the following patterns:
- In only KAVA
- In only WKAVA
- In only SWKAVA
- Any anount of KAVA/WKAVA or SWKAVA

There is NO compulsion for adding liquidity in a 50-50 proportion. Users are free to provide tokens in any ratio to mint liquidity tokens.

## The SWKAVA/WKAVA farm Rewards
The SWKAVA liquidity farm is capable of delivering multiple rewards to its depositors. Rewards are generally paid out in KAVA, SWKAVA and other additional tokens via Bribes.

### Epochs
Each new Epoch, the Protocol batches KAVA rewards earned from its position over the last Epoch to be distributed to the farmers in the current epoch. The Epoch rewards are distributed each second and claimable each second and accrue unless claimed. All rewards can be claimed anytime without any conditions.

### Duration
Initially, we will start with a weekly Epoch, and add all the KAVA earned by the protocol in the previous week as rewards for the stakers of the new week.
- Duration of an Epoch can be altered by a Governance Proposal by any SWKAVA holder or farmer.

### Epoch lag
Inspired from Convex Finance, we have modelled our reward scheme to benefit new users using the retroactive earnings from our last Epoch's stake. This novel approach helps us detach from the restrained "Fixed-APR" models of staking and introduce a more dynamic and moving rate of returns!

Whenever someone unstakes, the APR for others who stay gets boosted as unstaking increases the APR proportional to the unstaked amount, as rewards are still the same but people who share it are lesser.


### KAVA (WKAVA) Rewards
As long as the TWAP price of SWKAVA in the last epoch is above 0.99 KAVA, the rewards will be paid in KAVA (as WKAVA).

### SWKAVA Rewards
In epochs where TWAP is beneath 0.99, the KAVA rewards are first used to buyback SWKAVA, and then that SWKAVA is paid out as rewards.

## Minting, Collateral Backing, Supply & Market forces
The maximum supply of SWKAVA can theoretically be as much as the supply of KAVA itself. Initially there will be a supply of 0 SWKAVA, and it will increase by the exact amount of KAVA that is deposited into the protocol.

### Minting SWKAVA
SWKAVA tokens will forever be mintable at a price of 1 KAVA per SWKAVA.
- There will never be any fees for converting KAVA to SWKAVA.

### Smart-Router
Smart router is an intelligent, chain-aware smart contract that provides a multitude of benefits and convenience to its user. It also protects our users against any potential MEV attacks.

#### Buying SWKAVA
Our platform will not always mint new SWKAVA for KAVA deposits. Instead our platform will provide the best value to the user by combining market-buying of SWKAVA using KAVA and direct minting.
- For example, if Price of SWKAVA is 0.995 KAVA, the smart-router would use the deposit to first buy SWKAVA from the ABcDeFX as long as its Price-Impact does not move the price of SWKAVA above 1 KAVA. Beyond that point, our smart-router would mint SWKAVA 1:1 for KAVA using the remainder.

#### Staking SWKAVA/WKAVA Liquidity Tokens
The smart router is really smart. Users just need to send it some KAVA, and it will automatially funnel it through the a mixture of routes and optimize it for the highest benefit. Then it will automatically convert this into the SWKAVA/WKAVA LP tokens, and finally stake it into the multi-reward farm, on behalf of the user!

This design of our Smart Router expands upon our JIT ("just-in-time") routing model found in many of our Granaries at Kompound Protocol.
### Trading the SWKAVA
The main pair at ABcDeFX will be home to the biggest SWKAVA/WKAVA liquidity pool, which can be utilized by people to buy or sell SWKAVA for KAVA.

## The Peg
There is no hard "peg" for SWKAVA, but a target-price of 1 SWKAVA = 1 KAVA. At all points, irrespective of the price, we will always have a minimum of 1 KAVA backing each and every SWKAVA issued by the protocol. At all points, lightweight re-pegging forces remain active to counter each and every miniscule price movement beneath 1.

### Buyback threshold (BT)
The price of SWKAVA below which moderate re-pegging forces become active is the BT, or Buyback threshold. This is initially setup at 0.99 KAVA per SWKAVA, and can be reconfigured by a governance proposal, voted upon only by SWKAVA holders and farmers.

### Extreme Emergency Threshold (EET)
The Price of SWKAVA under which the strong re-pegging forces become active is defined as the EET. It uses our Smart Router for MEV-proofing.

### Above the peg?
In rare situations, there is a chance that price of SWKAVA goes above 1 KAVA. In such a case, we encourage everyone to repeatedly mint SWKAVA for 1 KAVA and sell it for a price of more than 1 to realize a profit by arbitration, and help us keep the price in a tight range around 1 KAVA.

## But, can SWKAVA de-peg?
Yes, there is indeed a possibility where SWKAVA can lose its peg. This could happen when a large amount of SWKAVA supply gets sold on the market suddenly.

### Now, lets see the impossibility of this
- Assume, there is 2 million KAVA and 2 million SWKAVA in the liquidity pool, and half of it belongs to just one person, Alice. If Alice removes her LP, she will get 1M KAVA & 1M SWKAVA, and the pool will have 1M KAVA + 1M SWKAVA. Now if Alice wants to sell 1M SWKAVA (that is 50% of the supply, which is a super-extreme case), the pool will still give her 930K KAVA in return. Despite this trade, the Price will only move to 0.93 KAVA per SWKAVA.
- Our novel ABcDeFX StableSwap approach makes even huge trades have negligible impacts on price of SWKAVA. Learn more about this design from Miguel M. here: [miguelmota.com/blog/understanding-stableswap-curve](https://miguelmota.com/blog/understanding-stableswap-curve/)
- In contrast, a similar trade on a traditional DEX like uniswap would have given Alice just 500K, and moved the price of SWKAVA to 0.25 KAVA, for a -75% impact. With our ABcDeFX StableSwap model, we can absorb this trade with just a -7% price change to 0.93 KAVA.

### Restoring the Peg
There are 3 main mechanisms that enable the protocol to restore the peg on its own.

#### 1. Rechanneled Buy-pressure
Any new user who wants to stake KAVA in the Lockless Protocol will have their KAVA redirected into buying it from the open market from the ABcDeFXchange via the Smart Router.
- Benefit to User:
	- Get more than 1 SWKAVA for each KAVA deposited, which can be guaranteed to be converted to more KAVA in future
	- Automatic Leverage to higher exposure to Staked KAVA, meaning more Yield for a lower investment.
- Benefit to Protocol:
	- Price of SWKAVA moves back towards 1 KAVA, helping in restoring the peg

#### 2. Buy-pressure from Epoch Rewards
Whenever the TWAP (Time-weighted Average Price) of SWKAVA is below 0.99 KAVA (The BT), the KAVA rewards earned in the previous epoch by the Protocol are used to buyback SWKAVA from the main pool to help restore the peg.
- Benefit to User:
	- Get more yield and higher APR becuase of higher number of SWKAVA tokens compared to KAVA rewards.
- Benefit to Protocol:
	- Price of SWKAVA moves back towards 1 KAVA, helping in restoring the peg.
	- Still be able to reward the user with exposure to yield of Staked KAVA.

#### 3. Buyback and Burn
This is the strongest insurane against a de-peg. This can be initialized when the price of SWKAVA falls below the EET Price of 0.911 KAVA. EET Price is changeable via SWKAVA Governance portal by only SWKAVA holders and farmers.

Features of EET are:
- The Protocol unstakes a part of its KAVA in order to initiate a buyback and BURN of SWKAVA.
- This is the only mechanism which reduces the supply of SWKAVA.
- EET results in over-collateralization of SWKAVA as supply reduction of SWKAVA is greater than the reduction in Protocol's staked KAVA.
- Super-high, although temporary, Boost in yields for new depositors in the coming Epoch.
- Pre-emptive effect of front-running the buyback could restore the peg on its own, without the need of an actual buyback.
- Uses our Smart Router for MEV-proofing.
- Price of SWKAVA gets restored to 1 KAVA.
- Excess SWKAVA sent to treasury as "De-peg Gains".

## For Validators
Validators are the ultimate beneficiaries of this Product. They get bestowed with an almost-eternal delegation if they run their operations smoothly.

### Bribes
Validators can Bribe the protocol with tokens, NFTs or other "kind" to drive the Protocol's Staked KAVA towards them.
- These Bribes would be delivered to our stakers natively via our Farm, alongside the ongoing KAVA, SWKAVA & other rewards to boost the yield of our farmers even more.
- Distribution will be done via airdrops in case of non-fungible assets.

### Stake weight allocation
In absence of Bribes, merit of validators will be decided each Epoch based on Performance of Nodes, Commission rates and their involvement in helping Kava ecosystem to grow.

## Governing SWKAVA
SWKAVA holders and farmers can create and vote on all governance matters.

### Right to vote
Contractual holders, multisig members, DAOs, simple holders and farmers, all have the right to delegate their votes to a representative of their choice.

## Governing Kava
By virtue of a stake in Kava, Lockless Protocol has the right to vote on all on-chain Governance Proposals of the Kava Blockchain.

### Right to vote
Each governance proposal at Kava will be mirrored automatically at the SWKAVA Governance Portal, which can be voted by SWKAVA holders & farmers.

## Further reading
We aspire to launch the Lockless Protocol in early October on the Kava blockchain.

For more updates, we implore you to join our Discord community :)
### [discord.gg/QpyfMarNrV](https://discord.gg/QpyfMarNrV)

# 🦾, 🚀
***Powered by Guru Network***