# Technical Detailsss

#### Technical Detailsssss <a href="#_dcj9jzmncgc" id="_dcj9jzmncgc"></a>

So how does all this work? The GotchiVault consists of two smart contracts: (1) an ERC20 contract for the vGHST token, derived from QiDao’s camTokens; and (2) a “vault” for depositing Aavegotchisssss.

The GochiVault contracts are truly “money legos” contracts, with the majority of the code being derived from established, audited protocols.

The contracts themselves are a [TransparentUpgradeableProxy from OpenZeppelin](https://docs.openzeppelin.com/upgrades-plugins/1.x/writing-upgradeable). This means that the contract can be upgraded by the “owner”, which has advantages and disadvantages. This allows for user security, as it means that new features can be implemented and any bugs can be fixed quickly and the new implementation re-deployed without users having to migrate. But like any upgradeable contract, it introduces a risk that the contract owner can insert malicious code in the future. That is why the contract is managed by a multi-sig wallet of 6 trusted Aavegotchi community members, several of whom are experienced software developers. In the future, the contract ownership could be transferred directly to VLT holders (see roadmap and tokenomics).

![](.gitbook/assets/0)

The **vGHST** code is derived from [OpenZeppelin’s ERC20 templates](https://docs.openzeppelin.com/contracts/2.x/api/token/erc20), and [QiDao’s camToken ](https://0xlaozi.medium.com/qidao-announces-compounding-aave-market-tokens-8bfd366e2631)code (this code allows the token, in our case vGHST, to represent a share of the underlying pool of an asset, in our case **GHST**. Thus, as the contract accrues **GHST** from fees and **FRENS** staking, the amount of **GHST** backing a single token of **vGHST** continues to go up).

At the core of the Aavegotchi staking is a double mapping which tracks who deposited each Aavegotchi to the contract.

![](.gitbook/assets/1)

This means that every token ID of every [ERC721](https://eips.ethereum.org/EIPS/eip-721) address maps to a single address – the person who deposited the token (this structure allows for staking of Realm parcels, not just Aavegotchis, should that become beneficial in the future). This allows us to give control of the Aavegotchi only to the depositor:

![](.gitbook/assets/2)

Most of the remaining functionality are simply wrapper functions allowing the contract to interact in limited fashion with the Aavegotchi protocol.

![](.gitbook/assets/3)

Regarding Snapshot voting, the Vault Managers can vote on behalf of the contract using a unique cross-chain contract implementation. We have deployed contracts to the same address on Ethereum mainnet and on Polygon network. The main net contract is an EIP-1271-compliant signature verifier. This means that when a vote is submitted on behalf of the Vault contract, **Snapshot** looks to the mainnet contract to verify that the sender is approved to vote. But **Snapshot** looks to the assets held in the Polygon contract to determine voting power.
