# Get ANN Accrued

Get the amount of ANN tokens accrued but not yet claimed by an address.

* `_address` \(string\) The address in which to find the ANN accrued.
* `[_provider]` \(Provider \| string\) An Ethers.js provider or valid network name string.
* `RETURN` \(string\) Returns a string of the numeric accruement of ANN. The value is scaled up by 18 decimal places.

```text
(async function () {
  const acc = await Annex.annex.getAnnexAccrued('0x4Ddc2D193948926D02f9B1fE9e1daa0718270ED5');
  console.log('Accrued', acc);
})().catch(console.error);
```

