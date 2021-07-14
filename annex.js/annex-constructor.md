# Annex Constructor

Creates an instance of the Annex.js SDK.

* `[provider]` \(Provider \| string\) Optional Ethereum network provider. Defaults to Ethers.js fallback mainnet provider.
* `[options]` \(object\) Optional provider options.
* `RETURN` \(object\) Returns an instance of the Annex.js SDK.

```text
var annex = new Annex(window.ethereum); // web browser

var annex = new Annex('http://127.0.0.1:8545'); // HTTP provider

var annex = new Annex(); // Uses Ethers.js fallback mainnet (for testing only)

var annex = new Annex('ropsten'); // Uses Ethers.js fallback (for testing only)

// Init with private key (server side)
var annex = new Annex('https://mainnet.infura.io/v3/_your_project_id_', {
  privateKey: '0x_your_private_key_', // preferably with environment variable
});

// Init with HD mnemonic (server side)
var annex = new Annex('mainnet' {
  mnemonic: 'clutch captain shoe...', // preferably with environment variable
});
```

