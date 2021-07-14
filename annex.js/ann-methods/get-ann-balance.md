# Get ANN Balance

Get the balance of ANN tokens held by an address.

* `_address` \(string\) The address in which to find the ANN balance.
* `[_provider]` \(Provider \| string\) An Ethers.js provider or valid network name string.
* `RETURN` \(string\) Returns a string of the numeric balance of ANN. The value is scaled up by 18 decimal places.

```text
(async function () {
  const bal = await Annex.annex.getAnnexBalance('0x2775b1c75658Be0F640272CCb8c72ac986009e38');
  console.log('Balance', bal);
})().catch(console.error);
```

