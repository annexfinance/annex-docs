# GovernanceService

Note: This service is experimental (alpha) and subject to change.

The Governance Service includes three endpoints to retrieve information about ANN accounts, governance proposals, and proposal vote receipts. You can use the APIs below to pull data about the Annex governance system:

```
  // Retreives a list of governance proposals
  fetch("https://api.annex.finance/api/governance/proposals");

  // Retreives a list of governance proposal vote receipts
  fetch("https://api.annex.finance/api/governance/proposal_vote_receipts");

  // Retreives a list of ANN accounts
  fetch("https://api.annex.finance/api/governance/accounts");
```

{% content-ref url="get-governance-proposals.md" %}
[get-governance-proposals.md](get-governance-proposals.md)
{% endcontent-ref %}

{% content-ref url="get-governance-proposal_vote_receipts.md" %}
[get-governance-proposal\_vote\_receipts.md](get-governance-proposal\_vote\_receipts.md)
{% endcontent-ref %}

{% content-ref url="get-governance-accounts.md" %}
[get-governance-accounts.md](get-governance-accounts.md)
{% endcontent-ref %}
