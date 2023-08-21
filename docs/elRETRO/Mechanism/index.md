---

title: Mechanism
grand_parent:
parent: 🎮 elRETRO
has_children:
nav_order: 2

---

# Core mechanism

## Summary
- Users can convert their veNFT into elRETRO.
- elRETRO can be staked to earn MATIC.
- ielRETRO is a dedicated compounder for elRETRO.

## Minting elRETRO
Initially in the first week, each 1 RETRO inside a veNFT will be able to mint out 1 elRETRO (1:1 ratio).

### Minting-price Ratio & Rebases
As the epochs go by the rewards from rebasing will be added to the main veNFT of elRETRO protocol without minting any new elRETRO. This will cause the minting ratio to shift from 1:1 to 1:(1+R), R being the rebase factor.

> For example, if the rebase for 2nd epoch is 0.5%, then the mint ratio will increase to 1.005, which means it would take a veNFT with 1.005 RETRO inside it to mint 1 elRETRO token.

Due the fact that there are no negative rebases in veRETRO system, this minting-price ratio of elRETRO will keep on increasing forever, and it will keep on appreciating against plain RETRO in a veNFT.

## Usage of the veNFT
The main veNFT of the system will be simply used to maximize the returns from voting. Vote distribution will only consider the after-sale value (in MATIC) of the earnable Bribes & Voter fees to decide its vote.

All the earnings from Voting such as Bribes & Trade-fee will be sold in their entireity to purchase MATIC.

All 100% of the Votes will be used for this purpose and this purpose only. Even if we have a conflict of interests in the future, the votes will be allocated solely on the basis of maximum MATIC returns per vote.

{: .note}
Earned **RETRO tokens will Not be sold**, and instead be converted into locked positions and converted to elRETRO.

## Usage of the MATIC from Voting yield
- 13.37% of the MATIC will be used to acquire Protocol-owned Liquidity.
- 86.63% of the MATIC is used as follows:
	- 20% of MATIC is distributed to Stakers
	- 80% of MATIC is sent as Bribes to Retro voters


### Note:
> This was different prior to the First DAO proposal for elRETRO:
- 74.26% of the MATIC will be distributed to elRETRO stakers.
- 13.37% of the MATIC will be give to Retro Voters as a Bribe to gather votes for the vAMM-elRETRO/WMATIC pool.
- 13.37% of the MATIC will be used to acquire Protocol-owned Liquidity.

