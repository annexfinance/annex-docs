# Cast Vote

Submit a vote on a Annex Governance proposal.

* `proposalId` \(string\) The ID of the proposal to vote on. This is an auto-incrementing integer in the Governor Alpha contract.
* `support` \(boolean\) A boolean of true for 'yes' or false for 'no' on the proposal vote.
* `[options]` \(CallOptions\) Options to set for a transaction and Ethers.js method overrides.
* `RETURN` \(object\) Returns an Ethers.js transaction object of the vote transaction.

```text
const annex = new Annex(window.ethereum);

(async function() {
  const castVoteTx = await annex.castVote(12, true);
  console.log('Ethers.js transaction object', castVoteTx);
})().catch(console.error);
```

