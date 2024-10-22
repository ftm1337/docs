---

title: Integrate eLOCKS in your DApp
grand_parent:
parent: 🔐 eLOCKS
has_children:
nav_order:

---

# Integration Guide
## For Contracts / Solidity
this is an example tx https://ftmscan.com/tx/0x5ebc0ac47e99f39929f1a1ac10a36b652b56381afcebc6b89674c63abf186d33
from your side, you would call this on the eLOCKS Contract
```js
//solidity
struct Referral { address agent; uint percent; } // percent is 1000 max = 100%
LockerRoom.createLockWithReferral( lp, amt, expiry, ref )
// ( 0xLpAddr, 1337e18, 1765000000, {agent:0xYourAddr, percent:250}); (250=25%,max is 1000=100%) } )
returns( address _locker, uint _nftid )
```
you can use any of these
```js
function createLock(IPair _lp, uint _amt, uint _exp) external returns(IEqualocker _locker, uint _ID) ;
function createLockFor(IPair _lp, uint _amt, uint _exp, address _to) external returns(IEqualocker _locker, uint _ID);﻿
function createLockWithReferral(IPair _lp, uint _amt, uint _exp, IEqualocker.Referral memory _ref) external ;
function createLockWithReferralFor(IPair _lp, uint _amt, uint _exp, address _to, IEqualocker.Referral memory _ref) external returns(IEqualocker _locker, uint _ID) ;
```

## For UI / web3 libraries (ethers.js, web3.js, viem.js, web3.py)

**eLOCKS** is the NFT contract itself, and issues individual **Lockers**, one each per NFT, owned by that nft's owner (nft is transferable).

- this address is the actual Locker that will hold the liquidity. reward claims should happen on this.
> `createLock` returns `(_locker, _nftid)`

- To claim rewrds (if whitelisted)
> `Locker.claimRewards()`

- To claim fees (if not wl)
> `Locker.claimFees()`

- To check claimable rewards (EQUAL/other farm rewards if any), we have
> `function claimableRewards() public view returns(uint[] memory)`

- To check claimable fees (the 2 tokens of the pool)
> `function claimableFees() public view returns(uint _cf0, uint _cf1)`

- To get the Locker address of a NFT id, do
> `LockerRoom.lockers(ID)`

- To get total locked in a locker,
> `Locker.totalSupply()`
(these are LP tokens, can be in gauge or not)

- To unlock a lock after expiry,
> `Locker.unlockLiquidity()`



it would be the same process in your node webapp, here using ethers v5
```js
LockerRoom = new ethers.Contract(eLOCKSaddress,["function createLockWithRefferal(address,uint,uint,{agent:address,percent:uint})" external returns(address,uint)],signer);
let _tr = await LockerRoom.createLockWithReferral( lpaddr, amount, expiry, {agent:0xBasedTreasury, percent:0.003e18});
let _tx = await _tr.wait();
console.log("New lock": _tx.data); //contains your new LOCKER's address and its NFT/locker ID
```

- (0.003e18 meaning 0.3% of trade fees will go to you, rest to user)
- max you can take 98.7% of the trade fees (percent:0.98663e18).
- once the lock is created, the referral stuff cannot be changed, its immutable.
- We recommend explicitly showing the Referral Fees you are going to take before a user makes their elock on your site for full transparency.
