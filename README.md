# My Spice To "No Loss Auctions" (Interesting Twist)

My variant of a no-loss auction works by incorporating a unique tax mechanism on bid increments, ensuring that when a bidder is outbid, they receive a portion of the tax collected from the difference between their bid and the new higher bid. Here's a simplified explanation:

1. **Bidding Process:**
    - Participants place bids on an item, with each new bid required to be higher than the current highest bid.

2. **Tax Mechanism:**
    - When a new bid is placed that outbids the current highest bid, a predetermined tax percentage (in this case, 10%) is calculated based on the difference between the new bid and the current highest bid.

3. **Tax Distribution:**
    - The collected tax is then distributed according to specific percentages:
        - **2% is burned:** This amount is effectively removed from circulation, simulating a deflationary mechanism.
        - **2% goes to a DAO Wallet:** This portion is sent to a designated wallet, presumably for governance or community purposes within the ecosystem.
        - **3% goes back to the outbid bidder:** As a form of consolation or incentive for participation, the outbid bidder receives this portion of the tax, reducing their overall loss.
        - **2% goes to the Team Wallet:** This part is allocated to the team behind the auction, perhaps as a form of revenue or operational fund.
        - **1% goes to the Interactor Wallet:** This could be a reward mechanism for other participants or stakeholders in the ecosystem.

4. **Winning the Auction:**
    - The auction concludes when no new bids are placed within a certain timeframe after the latest bid, making the highest bidder the winner of the auction.

5. **Final Settlement:**
    - The winner pays their bid amount, and the item is transferred to them. The seller receives the final bid amount minus the tax portion distributed to the outbid bidder in the last bidding round.

This auction model incentivizes participation by offering a partial refund mechanism through the tax distribution to outbid bidders, ensuring they don't walk away empty-handed. It also incorporates a deflationary aspect (burning a portion of the tax) and provides revenue streams to the auction's governing body and team, as well as rewards to other participants or roles defined as "Interactors."



[![Mentioned in Awesome Foundry](https://awesome.re/mentioned-badge-flat.svg)](https://github.com/crisgarner/awesome-foundry)
# Foundry + Hardhat Diamonds

This is a mimimal template for [Diamonds](https://github.com/ethereum/EIPs/issues/2535) which allows facet selectors to be generated on the go in solidity tests!

## Installation

- Clone this repo
- Install dependencies

```bash
$ yarn && forge update
```

### Compile

```bash
$ npx hardhat compile
```

## Deployment

### Hardhat

```bash
$ npx hardhat run scripts/deploy.js
```

### Foundry

```bash
$ forge t
```

`Note`: A lot of improvements are still needed so contributions are welcome!!

Bonus: The [DiamondLoupefacet](contracts/facets/DiamondLoupeFacet.sol) uses an updated [LibDiamond](contracts/libraries//LibDiamond.sol) which utilises solidity custom errors to make debugging easier especially when upgrading diamonds. Take it for a spin!!

Need some more clarity? message me [on twitter](https://twitter.com/Timidan_x), Or join the [EIP-2535 Diamonds Discord server](https://discord.gg/kQewPw2)
