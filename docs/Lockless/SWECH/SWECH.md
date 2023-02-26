---

title: SWECH
grand_parent:
parent: Lockless
has_children:
nav_order:

---

*Note: This documentation might be slightly outdated*

----

# swECH
> *Liquid Staking for Echelon*

## Why do we need SWECH?
Everyone loves to stake ECH as it provides a handsome yield! Aren't we right, stakers? ;)

### The Lockup
But this process ties up the depositor with an inability to unstake their ECH quickly. They get locked for 21-days into their position and cannot unfreeze their ECH. The market is generally too volatile and requires traders to be on their toes and ready to move their assets in tandem with the motions of the market, but bonding their tokens for a long time leaves them helpless against the tempestous market action.

### The exit lane
If the trend of market turns bearish, savvy traders would want to exit their positions as soon as possible. In preparation for such an event, most traders do not like to stake/bond/lock their tokens to stay liquid 24x7 round the clock, waiting to counter any potential downturns.

### Over-speeding penalty
But this strategy is extremely poor in terms of capital-efficiency. These traders sacrifice all the juicy yield Echelon has to offer! And these opportunity costs come at the benefit of a "potential but unlikely" scenario of a huge market downturn. The penalty for this over-cautiousness is harsh - it separates you from your darling APY.

## What does SWECH do?
What if there was a middle ground? What if we could come close to the lovely APR, without putting ourselves into a lockup?

### The Key: S-wECH
SWECH offers just this. SWECH unlocks the power of your locked ECH. It makes the value of your Bonded ECH tradable 24x7.

## What is SWECH?
SWECH is Staked Echelon, wrapped as an ERC20. Swech is not a fork. Swech is an original work of the Guru Network.

Let's see what sets it apart:
### No Locks & No Bondage
SWECH has no lockups, no bonding periods and is freely movable across wallets and contracts for free-trade and usage in Decentralized Finance protocols, NFTs, as collateral for lending & borrowing and everything else possible with a token.
### SWECH is immutable
Swech treats everyone equal. Nobody can be whitelisted or blacklisted. SWECH is fair, uncensorable, unstoppable and sufficiently decentralized.
### Get those Yields
With SWECH, you can not just earn ECH, but a plethora of reward tokens like BTC, ETH, USDC, SWECH, WECH, OSMO, ATOM, even NFTs and more!
### More than covered
With the advanced tokenomic design, each SWECH is always backed implicity by atleast 1 ECH, at all points.

## Tokenomics
### Fees
- There are NO team allocations
- There is NO fees to stake ECH
- There is NO commission or performance fee

### Yield Distribution
- All the ECH earned from the staked ECH is funneled back to farmers.

## Wait, what!? Farmers?
Swech utlizes an innovative design, first of its kind in the industry. Instead of delivering the yield to ECH depositors, the multi-token yield is rewarded to the Liquidity Providers of a special SWECH/WECH "stable" pair.

### Liquidity Pool
The SWECH/WECH liquidity resides on a special pool, also known as a StableSwap 2pool, made famous by Curve Finance.

## Swech-Ex: The Swech Exchange
Swech-Ex is home to the main Liquidity pool composed of WECH + SWECH tokens. This DEX has only one pair - The WECH/SWECH pool.

### Based on Curve.fi V2
- Near-zero slippage trades
- Almost absent price impact
- Audited by numerous independent people
- Battle-tested with hundreds of billions
- Liquidity Providers earn Trade-fees
- Keeps 1 SWECH at par with 1 ECH
- Composable and easy to build upon by other Echelon Projects
- Tokenized Liquidity Positions
- Auto-compounding trade-fee APR
- LP tokens usable freely by people and protocols
- Immutable. Uncensorable. Unstoppable.

### Single-sided liquidity
Our design embraces single-token liquidity addition to streamline the process for all of our Echelon users. Liquidity can be added in either of the following patterns:
- In only ECH
- In only WECH
- In only SWECH
- Any anount of ECH/WECH or SWECH

There is NO compulsion for adding liquidity in a 50-50 proportion. Users are free to provide tokens in any ratio to mint liquidity tokens.

## The SWECH/WECH farm Rewards
The Swech liquidity farm is capable of delivering multiple rewards to its depositors. Rewards are generally paid out in ECH, SWECH and other additional tokens via Bribes.

### Epochs
Each new Epoch, the Protocol batches ECH rewards earned from its position over the last Epoch to be distributed to the farmers in the current epoch. The Epoch rewards are distributed each second and claimable each second and accrue unless claimed. All rewards can be claimed anytime without any conditions.

### Duration
Initially, we will start with a weekly Epoch, and add all the ECH earned by the protocol in the previous week as rewards for the stakers of the new week.
- Duration of an Epoch can be altered by a Governance Proposal by any SWECH holder or farmer.

### Epoch lag
Inspired from Convex Finance, we have modelled our reward scheme to benefit new users using the retroactive earnings from our last Epoch's stake. This novel approach helps us detach from the restrained "Fixed-APR" models of staking and introduce a more dynamic and moving rate of returns!

Whenever someone unstakes, the APR for others who stay gets boosted as unstaking increases the APR proportional to the unstaked amount, as rewards are still the same but people who share it are lesser.


### ECH (WECH) Rewards
As long as the TWAP price of SWECH in the last epoch is above 0.99 ECH, the rewards will be paid in ECH (as WECH).

### SWECH Rewards
In epochs where TWAP is beneath 0.99, the ECH rewards are first used to buyback SWECH, and then that SWECH is paid out as rewards.

## Minting, Collateral Backing, Supply & Market forces
The maximum supply of SWECH can theoretically be as much as the supply of ECH itself. Initially there will be a supply of 0 SWECH, and it will increase by the exact amount of ECH that is deposited into the protocol.

### Minting SWECH
SWECH tokens will forever be mintable at a price of 1 ECH per SWECH.
- There will never be any fees for converting ECH to SWECH.

### Smart-Router
Smart router is an intelligent, chain-aware smart contract that provides a multitude of benefits and convenience to its user. It also protects our users against any potential MEV attacks.

#### Buying SWECH
Our platform will not always mint new SWECH for ECH deposits. Instead our platform will provide the best value to the user by combining market-buying of SWECH using ECH and direct minting.
- For example, if Price of SWECH is 0.995 ECH, the smart-router would use the deposit to first buy SWECH from the Swech-Ex as long as its Price-Impact does not move the price of SWECH above 1 ECH. Beyond that point, our smart-router would mint SWECH 1:1 for ECH using the remainder.

#### Staking SWECH/WECH Liquidity Tokens
The smart router is really smart. Users just need to send it some ECH, and it will automatially funnel it through the a mixture of routes and optimize it for the highest benefit. Then it will automatically convert this into the SWECH/WECH LP tokens, and finally stake it into the multi-reward farm, on behalf of the user!

This design of our Smart Router expands upon our JIT ("just-in-time") routing model found in many of our Granaries at Kompound Protocol.
### Trading the SWECH
The main pair at Swech-Ex will be home to the biggest SWECH/WECH liquidity pool, which can be utilized by people to buy or sell SWECH for ECH.

## The Peg
There is no hard "peg" for SWECH, but a target-price of 1 SWECH = 1 ECH. At all points, irrespective of the price, we will always have a minimum of 1 ECH backing each and every SWECH issued by the protocol. At all points, lightweight re-pegging forces remain active to counter each and every miniscule price movement beneath 1.

### Buyback threshold (BT)
The price of SWECH below which moderate re-pegging forces become active is the BT, or Buyback threshold. This is initially setup at 0.99 ECH per SWECH, and can be reconfigured by a governance proposal, voted upon only by SWECH holders and farmers.

### Extreme Emergency Threshold (EET)
The Price of SWECH under which the strong re-pegging forces become active is defined as the EET. It uses our Smart Router for MEV-proofing.

### Above the peg?
In rare situations, there is a chance that price of SWECH goes above 1 ECH. In such a case, we encourage everyone to repeatedly mint SWECH for 1 ECH and sell it for a price of more than 1 to realize a profit by arbitration, and help us keep the price in a tight range around 1 ECH.

## But, can SWECH de-peg?
Yes, there is indeed a possibility where SWECH can lose its peg. This could happen when a large amount of SWECH supply gets sold on the market suddenly.

### Now, lets see the impossibility of this
- Assume, there is 2 million ECH and 2 million SWECH in the liquidity pool, and half of it belongs to just one person, Alice. If Alice removes her LP, she will get 1M ECH & 1M SWECH, and the pool will have 1M ECH + 1M SWECH. Now if Alice wants to sell 1M SWECH (that is 50% of the supply, which is a super-extreme case), the pool will still give her 930K ECH in return. Despite this trade, the Price will only move to 0.93 ECH per SWECH.
- Our novel Swech-Ex StableSwap approach makes even huge trades have negligible impacts on price of SWECH. Learn more about this design from Miguel M. here: [miguelmota.com/blog/understanding-stableswap-curve](https://miguelmota.com/blog/understanding-stableswap-curve/)
- In contrast, a similar trade on a traditional DEX like uniswap would have given Alice just 500K, and moved the price of SWECH to 0.25 ECH, for a -75% impact. With our Swech-Ex StableSwap model, we can absorb this trade with just a -7% price change to 0.93 ECH.

### Restoring the Peg
There are 3 main mechanisms that enable the protocol to restore the peg on its own.

#### 1. Rechanneled Buy-pressure
Any new user who wants to stake ECH in the Swech Protocol will have their ECH redirected into buying it from the open market from the Swech-Exchange via the Smart Router.
- Benefit to User:
	- Get more than 1 SWECH for each ECH deposited, which can be guaranteed to be converted to more ECH in future
	- Automatic Leverage to higher exposure to Staked ECH, meaning more Yield for a lower investment.
- Benefit to Protocol:
	- Price of SWECH moves back towards 1 ECH, helping in restoring the peg

#### 2. Buy-pressure from Epoch Rewards
Whenever the TWAP (Time-weighted Average Price) of SWECH is below 0.99 ECH (The BT), the ECH rewards earned in the previous epoch by the Protocol are used to buyback SWECH from the main pool to help restore the peg.
- Benefit to User:
	- Get more yield and higher APR becuase of higher number of SWECH tokens compared to ECH rewards.
- Benefit to Protocol:
	- Price of SWECH moves back towards 1 ECH, helping in restoring the peg.
	- Still be able to reward the user with exposure to yield of Staked ECH.

#### 3. Buyback and Burn
This is the strongest insurane against a de-peg. This can be initialized when the price of SWECH falls below the EET Price of 0.911 ECH. EET Price is changeable via SWECH Governance portal by only SWECH holders and farmers.

Features of EET are:
- The Protocol unstakes a part of its ECH in order to initiate a buyback and BURN of SWECH.
- This is the only mechanism which reduces the supply of SWECH.
- EET results in over-collateralization of SWECH as supply reduction of SWECH is greater than the reduction in Protocol's staked ECH.
- Super-high, although temporary, Boost in yields for new depositors in the coming Epoch.
- Pre-emptive effect of front-running the buyback could restore the peg on its own, without the need of an actual buyback.
- Uses our Smart Router for MEV-proofing.
- Price of SWECH gets restored to 1 ECH.

## For Validators
Validators are the ultimate beneficiaries of this Product. They get bestowed with an almost-eternal delegation if they run their operations smoothly.

### Bribes
Validators can Bribe the protocol with tokens, NFTs or other "kind" to drive the Protocol's Staked ECH towards them.
- These Bribes would be delivered to our stakers natively via our Farm, alongside the ongoing ECH, SWECH & other rewards to boost the yield of our farmers even more.
- Distribution will be done via airdrops in case of non-fungible assets.

### Stake weight allocation
In absence of Bribes, merit of validators will be decided each Epoch based on Performance of Nodes, Commission rates and their involvement in helping Echelon ecosystem to grow.

## Governing Swech
SWECH holders and farmers can create and vote on all governance matters.

### Right to vote
Contractual holders, multisig members, DAOs, simple holders and farmers, all have the right to delegate their votes to a representative of their choice.

## Governing Echelon
By virtue of a stake in Echelon, Swech protocol has the right to vote on all on-chain Governance Proposals of the Echelon Blockchain.

### Right to vote
Each governance proposal at Echelon will be mirrored automatically at the Swech Governance Portal, which can be voted by SWECH holders & farmers.

## Further reading
We aspire to launch the Swech Protocol in early October on the Echelon blockchain.

For more updates, we implore you to join our Discord community :)
### [discord.gg/QpyfMarNrV](https://discord.gg/QpyfMarNrV)

# 🦾, 🚀
***Powered by Guru Network***