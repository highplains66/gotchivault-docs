# Core features

### Features of the Gotchi Vault <a href="#_5qtvy945nhwp" id="_5qtvy945nhwp"></a>

The Gotchi Vault consists of two smart contracts that allow the Vault Managers to safely manage your assets. With Gotchi Vault, you can maximize the return on (1) your GHST, and (2) your Aavegotchis.

#### GHST staking <a href="#_4qwstq4sjziu" id="_4qwstq4sjziu"></a>

Because[ Aavegotchi.com](http://aavegotchi.com) isn’t splashy/loud about its APY, many new users are surprised to hear that seasoned veterans are earning 40%+ on their GHST just by staking the GHST for [FRENS](https://wiki.aavegotchi.com/en/glossary#frens), and cashing in those FRENS for raffle tickets. New users are often overwhelmed by the mechanics of knowing how much to stake, when to cash in, when to enter into raffles, which raffle to enter, etc. Additionally, users with small-to-moderate amounts of GHST may get rekt by the [Chainlink VRF](https://wiki.aavegotchi.com/en/glossary#chainlink-vrf) gods; the smaller the number of tickets you enter, the greater impact statistical variants in the VRF can have on your ROI. And with a small amount of GHST at their disposal, users often are forced to pick a single investment decision, which may ultimately be sub-optimal.

With Gotchi Vault, you and hundreds of other community members deposit your GHST into the contract and receive back a corresponding amount of **vGHST**, a new token that represents a share of all the GHST held by the contract. Once you deposit your GHST, everything else is handled by the Vault Managers entirely on-chain, in a way that ensures that no one can compromise your funds. This bears repeating: **once you deposit your GHST into the Vault, no one can ever withdraw your funds except for you, not even the Vault Managers.**

So what CAN the Vault Managers do with your GHST? The Vault Managers only have the ability to stake and unstake your GHST in the Aavegotchi single-asset FRENS pool. The Vault Managers do have complete control over how/when to spend those FRENS, which raffle tickets to purchase, whether to sell those raffle tickets, which raffles to enter, and how much to sell raffle winnings for. The Vault Managers will ensure that these funds are spent in a diversified manner to optimize yield (see below for technical details on how vGHST functions).

#### Aavegotchi/ERC721 staking <a href="#_1o9gylriaxml" id="_1o9gylriaxml"></a>

Aavegotchi users may not always have time to pet their Aavegotchi, and they may not have the resources or technical no-how to set up their own petting bot. Users may miss a [Snapshot vote](https://wiki.aavegotchi.com/en/dao#voting), or may not have the time to read up on a [SigProp or CoreProp proposal](https://wiki.aavegotchi.com/en/dao#type-of-proposals) before voting. As a result, users’ Aavegotchis may fall behind in their kinship or XP accrual. And with Gotchiverse Aavegotchi rentals coming soon, this is a whole other aspect of asset management an Aavegotchi owner needs to be familiar with to fully optimize their yield.

With Gotchi Vault, the Vault Managers take care of all of that, again in a decentralized, protected, and on-chain way. Using redundant petting methods (we use a combination of [Gotchi.World](https://www.gotchi.world) and our own petting bot running on a secure server), we can ensure that your Aavegotchis never miss a pet, and maximize their kinship. And because our contract is [EIP-1271-compliant](https://eips.ethereum.org/EIPS/eip-1271) (see technical details below), the Vault Managers can vote _**on behalf of the contract itself**_, meaning that all the Gotchis residing in the contract will be eligible for all future SigProp and CoreProp XP drops.

Just like with GHST staking, once your Aavegotchi is deposited into the Vault only you can withdraw that Aavegotchi. The Vault Managers can’t trade it, list it for sale, or transfer it. Once an Aavegotchi is in the Vault, a user can always withdraw the Aavegotchi if they want to play in a minigame, or run around the Gotchiverse.

We don’t have all the details yet on how Aavegotchi rentals / farming splits will work once the Gotchiverse is live, but you can rest assured that once the code is published, the Gotchi Vault will implement similar redundant, secure, and permissionless methods to ensure that your Aavegotchi is optimally being rented out for farming, to maximize yield.

Regarding rentals, we are actively seeking out beneficial partnerships with external guilds to maximize rental yield. We recently announced an [inaugural partnership](https://www.cgu.io/post/cgu-have-partnered-with-gotchi-vault) with [Crypto Gaming United](https://www.cgu.io); as part of this partnership, we have committed 1,000 of the Vault’s Aavegotchis for their exclusive use. This will be hugely beneficial for both the Aavegotchi depositors, vGHST holders, and CGU. We are excited about this and future partnerships!
