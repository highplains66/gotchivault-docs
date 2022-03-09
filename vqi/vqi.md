# vQi

vQi is tokenized maximally boosted eQi, based on OpenZeppelin's ERC20 upgradeable smart contract templates. Users deposit Qi into the vQi smart contract, which mints vQi at a rate of 1:1. The deposited Qi is immediately locked up for the maximum 4 year boost. This means that all Qi in the vQi contract receives the maximum airdrops, and the maximum voting power.&#x20;

![Representation of vQi minting](https://lh4.googleusercontent.com/2zre64Ax723SuSovkIL92maR4vEgNklenTjFArNU1f07vKFVaZZN8-mg-PLnf66iquY8cT3Aqk5Ae3Fc\_1ftXLRQ6bZYgW8Ts-y8xTXk0Blbbm3VX9cQuRFROX2LH8eJMt3\_WkUg)

All airdrops received by the vQi smart contract will be passed along proportionally to all holders of vQi every week (see below for one caveat). This means that we will have separated the two valuable characteristics of Qi: the vQi smart contract retains the voting power (and will be used exclusively to vote for vGHST vaults), but the weekly yield is forwarded along to vQi holders. vQi holders now get the best possible airdrop yield (locked up for 4 years), but they have a transferable token (vQi) that they can move around or sell if they want to exit their position within the first four years. This is roughly what Convex and TetuQi do, although we are passing all the Qi rewards directly to vQi holders in the form of Qi.

The Vault Managers have the ability to withdraw the weekly Qi rewards the vQi contract will receive from QiDao every week.  We will take a snapshot of all vQi holders each week when QiDao takes its snapshot, and another snapshot when the Qi rewards are distributed.  To be eligible for any given week's Qi rewards, users will have to maintain their balance of vQi between the initial and second snapshots.

At this point, it should be apparent that vQi is inherently superior to Qi in every way (i.e., 4x weekly yield) except it has no voting power (which is retained by the vQi smart contract). So how will vQi have liquidity if people want to exit their position? Through protocol-owned-liquidity.

Whereas Convex and TetuQi must constantly incentivize LP holders to provide liquidity (and risk those LP holders dumping their LP tokens), vQi will initially provide its own liquidity (to be supplemented in the coming weeks by an additional project we're not ready to disclose). Every week, 10% of the Qi yield earned by the vQi contracts will be set aside and used to buy Qi-vQi LP tokens. (We anticipate moving to an Ohm-style bonding mechanism in the future to buy LP tokens from the public at a premium in exchange for vQi).&#x20;

It's important to note that because some vQi will be locked in the Qi-vQi LP, that vQi will NOT receive weekly Qi rewards.  This vQi's rewards will be distributed to the remainder of the vQi holders.  This means that as more liquidity is added to the LP, everyone else's vQi APR goes up.

So what should the price of vQi end up being? It should peg roughly to the price of Qi.  Because you can always mint new vQi directly from the vQi contract at a 1:1 rate, the price of vQi should never be greater than the price of Qi – that would create an immediate arbitrage opportunity.  So the price of vQi will always be less than or equal to the price of Qi.  How much less?  As explained below, it should be close to the price of Qi, as the vQi APR will constantly increase, and users are incentivized to buy vQi from the market as long as the price is less than the price of Qi. &#x20;

E.g., imagine a user has 1 Qi and wants to get vQi to benefit from the higher APR; assume the price of Qi is $1 and the price of vQi is $0.95.  The user could mint 1 vQi directly from the vQi contract, and he’d get 1 vQi for his 1 Qi.  Or he could buy vQi from the LP and get \~ 1.05 vQi for his 1 Qi.  So as long as the price of vQi in the LP is far enough under the price of Qi to make up for LP fees + slippage, users will buy vQi from the LP.  So we can expect vQi to always be \~1% below the price of Qi.

You can mint vQi at [https://www.gotchivault.com/vqi](https://www.gotchivault.com/vqi)

The vQi smart contract is available [https://polygonscan.com/address/0xB424dfDf817FaF38FF7acF6F2eFd2f2a843d1ACA](https://polygonscan.com/address/0xB424dfDf817FaF38FF7acF6F2eFd2f2a843d1ACA)
