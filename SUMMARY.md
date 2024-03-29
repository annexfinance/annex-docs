# Table of contents

* [Annex Finance Documentation](README.md)
* [Getting Started](getting-started/README.md)
  * [Guides](getting-started/guides.md)
  * [Networks](getting-started/networks.md)
  * [Protocol Math](getting-started/protocol-math/README.md)
    * [aToken and Underlying Decimals](getting-started/protocol-math/atoken-and-underlying-decimals.md)
    * [Interpreting Exchange Rates](getting-started/protocol-math/interpreting-exchange-rates.md)
    * [Calculating Accrued Interest](getting-started/protocol-math/calculating-accrued-interest.md)
    * [Calculating the APY Using Rate Per Block](getting-started/protocol-math/calculating-the-apy-using-rate-per-block.md)
  * [Gas Costs](getting-started/gas-costs.md)
* [ATokens](atokens/README.md)
  * [Mint](atokens/mint.md)
  * [Redeem](atokens/redeem.md)
  * [Redeem Underlying](atokens/redeem-underlying.md)
  * [Borrow](atokens/borrow.md)
  * [Repay Borrow](atokens/repay-borrow.md)
  * [Repay Borrow Behalf](atokens/repay-borrow-behalf.md)
  * [Transfer](atokens/transfer.md)
  * [Liquidate Borrow](atokens/liquidate-borrow.md)
  * [Key Events](atokens/key-events.md)
  * [Error Codes](atokens/error-codes.md)
  * [Failure Info](atokens/failure-info.md)
  * [Exchange Rate](atokens/exchange-rate.md)
  * [Get Cash](atokens/get-cash.md)
  * [Total Borrow](atokens/total-borrow.md)
  * [Borrow Balance](atokens/borrow-balance.md)
  * [Borrow Rate](atokens/borrow-rate.md)
  * [Total Supply](atokens/total-supply.md)
  * [Underlying Balance](atokens/underlying-balance.md)
  * [Supply Rate](atokens/supply-rate.md)
  * [Total Reserves](atokens/total-reserves.md)
  * [Reserve Factor](atokens/reserve-factor.md)
* [Comptroller](comptroller/README.md)
  * [Enter Markets](comptroller/enter-markets.md)
  * [Exit Market](comptroller/exit-market.md)
  * [Get Assets In](comptroller/get-assets-in.md)
  * [Collateral Factor](comptroller/collateral-factor.md)
  * [Get Account Liquidity](comptroller/get-account-liquidity.md)
  * [Close Factor](comptroller/close-factor.md)
  * [Liquidation Incentive](comptroller/liquidation-incentive.md)
  * [Key Events](comptroller/key-events.md)
  * [Error Codes](comptroller/error-codes.md)
  * [Failure Info](comptroller/failure-info.md)
  * [ANN Distribution Speeds](comptroller/ann-distribution-speeds.md)
  * [Claim ANN](comptroller/claim-ann.md)
  * [Market Metadata](comptroller/market-metadata.md)
* [Governance](governance/README.md)
  * [Delegate](governance/delegate.md)
  * [Delegate By Signature](governance/delegate-by-signature.md)
  * [Get Current Votes](governance/get-current-votes.md)
  * [Get Prior Votes](governance/get-prior-votes.md)
  * [Key Events](governance/key-events.md)
  * [Governor Alpha](governance/governor-alpha.md)
  * [Quorum Votes](governance/quorum-votes.md)
  * [Proposal Threshold](governance/proposal-threshold.md)
  * [Proposal Max Operations](governance/proposal-max-operations.md)
  * [Voting Delay](governance/voting-delay.md)
  * [Voting Period](governance/voting-period.md)
  * [Propose](governance/propose.md)
  * [Queue](governance/queue.md)
  * [Execute](governance/execute.md)
  * [Cancel](governance/cancel.md)
  * [Get Actions](governance/get-actions.md)
  * [Get Receipt](governance/get-receipt.md)
  * [State](governance/state.md)
  * [Cast Vote](governance/cast-vote.md)
  * [Cast Vote By Signature](governance/cast-vote-by-signature.md)
  * [Timelock](governance/timelock.md)
  * [Pause Guardian](governance/pause-guardian.md)
* [API](api/README.md)
  * [STokenService](api/stokenservice/README.md)
    * [GET: /atoken](api/stokenservice/get-atoken.md)
  * [MarketHistoryService](api/markethistoryservice/README.md)
    * [GET: /market\_history/graph](api/markethistoryservice/get-graph.md)
  * [ProposalService](api/proposal-service/README.md)
    * [GET: /proposals](api/proposal-service/get-proposals.md)
    * [GET: /proposals/:id](api/proposal-service/get-proposals-by-id.md)
    * [GET: /proposals/statistics](api/proposal-service/get-proposals-statistics.md)
  * [VoterService](api/voter-service/README.md)
    * [GET: /voters/accounts](api/voter-service/get-voters-accounts.md)
    * [GET: /voters/accounts/:address](api/voter-service/get-voters-accounts-address.md)
    * [GET: /voters/history/:address](api/voter-service/get-voters-history-address.md)
    * [GET: /voters/:proposalId](api/voter-service/get-voters-proposalid.md)
  * [GovernanceService](api/governanceservice/README.md)
    * [GET: /governance/annex](api/governanceservice/get-governance-annex.md)
    * [GET: /governance/proposals](api/governanceservice/get-governance-proposals.md)
    * [GET: /governance/proposal\_vote\_receipts](api/governanceservice/get-governance-proposal_vote_receipts.md)
    * [GET: /governance/accounts](api/governanceservice/get-governance-accounts.md)
  * [Shared Data Types](api/shared-data-types.md)
* [Annex.js](annex.js/README.md)
  * [Annex Constructor](annex.js/annex-constructor.md)
  * [API Methods](annex.js/api-methods/README.md)
    * [Account](annex.js/api-methods/account.md)
    * [aToken](annex.js/api-methods/atoken.md)
    * [Market History](annex.js/api-methods/market-history.md)
    * [Governance](annex.js/api-methods/governance.md)
  * [aToken Methods](annex.js/atoken-methods/README.md)
    * [Supply](annex.js/atoken-methods/supply.md)
    * [Redeem](annex.js/atoken-methods/redeem.md)
    * [Borrow](annex.js/atoken-methods/borrow.md)
    * [Repay Borrow](annex.js/atoken-methods/repay-borrow.md)
  * [ANN Methods](annex.js/ann-methods/README.md)
    * [To Checksum Address](annex.js/ann-methods/to-checksum-address.md)
    * [Get ANN Balance](annex.js/ann-methods/get-ann-balance.md)
    * [Get ANN Accrued](annex.js/ann-methods/get-ann-accrued.md)
    * [Claim ANN](annex.js/ann-methods/claim-ann.md)
    * [Delegate](annex.js/ann-methods/delegate.md)
    * [Delegate By Sig](annex.js/ann-methods/delegate-by-sig.md)
    * [Create Delegate Signature](annex.js/ann-methods/create-delegate-signature.md)
  * [Comptroller Methods](annex.js/comptroller-methods/README.md)
    * [Enter Markets](annex.js/comptroller-methods/enter-markets.md)
    * [Exit Market](annex.js/comptroller-methods/exit-market.md)
  * [Ethereum Methods](annex.js/ethereum-methods/README.md)
    * [Read](annex.js/ethereum-methods/read.md)
    * [Trx](annex.js/ethereum-methods/trx.md)
    * [Get Balance](annex.js/ethereum-methods/get-balance.md)
  * [Governance Methods](annex.js/governance-methods/README.md)
    * [Cast Vote](annex.js/governance-methods/cast-vote.md)
    * [Cast Vote By Sig](annex.js/governance-methods/cast-vote-by-sig.md)
    * [Create Vote Signature](annex.js/governance-methods/create-vote-signature.md)
  * [Price Feed Methods](annex.js/price-feed-methods/README.md)
    * [Get Price](annex.js/price-feed-methods/get-price.md)
  * [Utility Methods](annex.js/utility-methods/README.md)
    * [Get Address](annex.js/utility-methods/get-address.md)
    * [Get ABI](annex.js/utility-methods/get-abi.md)
    * [Get Network Name With Chain ID](annex.js/utility-methods/get-network-name-with-chain-id.md)
* [Auction](auction/README.md)
  * [User Guide](auction/user-guide/README.md)
    * [Create Auction](auction/user-guide/auction-user-guide.md)
    * [Create Bid](auction/user-guide/create-bid.md)
    * [Settle Auction](auction/user-guide/settle-auction-1.md)
    * [Claim Auction](auction/user-guide/claim-auction.md)
    * [Cancel Auction Bid](auction/user-guide/cancel-auction-bid.md)
    * [Auction Types](auction/user-guide/auction-types/README.md)
      * [Live Auction](auction/user-guide/auction-types/live-auction.md)
      * [Upcoming Auction](auction/user-guide/auction-types/upcoming-auction.md)
      * [Past Auction](auction/user-guide/auction-types/past-auction.md)
  * [Auction Technical Guide](auction/auction-technical-guide.md)
* [Security](security/README.md)
  * [Formal Verification](security/formal-verification.md)
  * [Bug Bounty Program](security/bug-bounty-program.md)

