---
description: >-
  Annex Auction is a suite of open-source smart contracts created to ease the
  process of launching a new project on the AnnexSwap exchange.
---

# Auction Technical Guide

Annex Auction is a suite of open-source smart contracts created to ease the process of launching a new project on the AnnexSwap exchange. Annex Auction aims to drive new capital and trade to the exchange by increasing the attractiveness of AnnexSwap as a place for token creators and communities to launch new project tokens.

## Benefit of Auction

The key benefit of Annex Auction is that it provides Initial Liquidity Providers for new listing tokens with low prices and keeps the auction token price higher than the listing price. Annex supports several types of auctions based on auctioneer requirements to incentivize more new tokens listings. ANN will be an auction payment currency and 100 ANN required to create a new auction therefore it will incentivize ANN tokens usage and circulating supply.

### Advantage of Batch Auction

The biggest advantage is certainly that buyers don't have to wait for a certain time to submit orders, but that they can submit orders at any time. This makes the system much more convenient for users. Dutch auctions have a very high activity right before the auction is closing. If pieces of the infrastructure are not working reliably during this time period, then prices can fall further than expected, causing a loss for the auctioneer. Also, high gas prices during this short time period can be a hindering factor for buyers to quickly join the auction. Dutch auctions calculate their price based on the block time. This pricing is hard to predict for all participants, as the mining is a stochastic process Additionally, the unpredictability for the mining time of the next block Dutch auctions are causing a gas price bidding war to close the auction. In contrast, in a batch auction, different buyers will bid against other bidders in the mem-pool. Especially, once EIP-1559 is implemented and the mining of a transaction is guaranteed for the next block, then bidders have to compete on bidding limit-prices instead of the gas-prices to get included into the auction.

### Instructions

Install dependencies

```text
git clone https://github.com/annexfinance/annex-auction.git
cd annex-auction
yarn
yarn build
```

Running tests:

```text
yarn deploy --network $NETWORK
```

Verify on etherscan:

```text
npx hardhat etherscan-verify --license None --network rinkeby
```



