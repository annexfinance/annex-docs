# Claim ANN

Create a transaction to claim accrued ANN tokens for the user.

* `[options]` \(CallOptions\) Options to set for a transaction and Ethers.js method overrides.
* `RETURN` \(object\) Returns an Ethers.js transaction object of the vote transaction.

```text
const annex = new Annex(window.ethereum);

(async function() {

  console.log('Claiming ANN...');
  const trx = await compound.claimAnnex();
  console.log('Ethers.js transaction object', trx);

})().catch(console.error);
```

