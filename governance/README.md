# Governance

The Annex protocol is governed and upgraded by ANN token-holders, using three distinct components; the ANN token, governance module \(Governor Alpha\), and Timelock. Together, these contracts allow the community to propose, vote, and implement changes through the administrative functions of a aToken or the Comptroller. Proposals can include changes like adjusting an interest rate model, to adding support for a new asset.

Any address with more than 65,000 ANN delegated to it may propose governance actions, which are executable code. When a proposal is created, the community can submit their votes during a 3 day voting period. If a majority, and at least 130,000 votes are cast for the proposal, it is queued in the Timelock, and can be implemented after 2 days.

![Governance Diagram](https://annex.finance/images/gov_diagram.png)

## ANN

ANN is an [ERC-20](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-20.md) token that allows the owner to delegate voting rights to any address, including their own address. Changes to the owner’s token balance automatically adjust the voting rights of the delegate.

