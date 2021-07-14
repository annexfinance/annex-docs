# Claim ANN

Every Annex user accrues ANN for each block they are supplying to or borrowing from the protocol. Users may call the Comptroller's `claimAnnex` method at any time to transfer ANN accrued to their address.

**Comptroller**

```text
// Claim all the ANN accrued by holder in all markets
function claimAnnex(address holder) public

// Claim all the ANN accrued by holder in specific markets
function claimAnnex(address holder, SToken[] memory aTokens) public

// Claim all the ANN accrued by specific holders in specific markets for their supplies and/or borrows
function claimAnnex(address[] memory holders, SToken[] memory aTokens, bool borrowers, bool suppliers) public
```

**Solidity**

```text
Comptroller troll = Comptroller(0xABCD...);
troll.claimAnnex(0x1234...);
```

**Web3 1.2.6**

```javascript
const comptroller = new web3.eth.Contract(comptrollerAbi, comptrollerAddress);
await comptroller.methods.claimAnnex("0x1234...").send({ from: sender });
```

