# aToken

Makes a request to the STokenService API. The aToken API retrieves information about aToken contract interaction. For more details, see the Annex API documentation.

* `options` \(object\) A JavaScript object of API request parameters.
* `RETURN` \(object\) Returns the HTTP response body or error.

```text
(async function() {
  const sEthData = await Annex.api.aToken({
    "addresses": Annex.util.getAddress(Annex.aBNB)
  });

  console.log('sEthData', sEthData); // JavaScript Object
})().catch(console.error);
```

