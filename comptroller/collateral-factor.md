# Collateral Factor

A aToken's collateral factor can range from 0-90%, and represents the proportionate increase in liquidity \(borrow limit\) that an account receives by minting the aToken.

Generally, large or liquid assets have high collateral factors, while small or illiquid assets have low collateral factors. If an asset has a 0% collateral factor, it can't be used as collateral \(or seized in liquidation\), though it can still be borrowed.

Collateral factors can be increased \(or decreased\) through Annex Governance, as market conditions change.

**Comptroller**

```text
function markets(address aTokenAddress) view returns (bool, uint, bool)
```

* `aTokenAddress`: The address of the aToken to check if listed and get the collateral factor for.
* `RETURN`: Tuple of values \(isListed, collateralFactorMantissa, isAnnexd\); isListed represents whether the comptroller recognizes this aToken; collateralFactorMantissa, scaled by 1e18, is multiplied by a supply balance to determine how much value can be borrowed. The isAnnexd boolean indicates whether or not suppliers and borrowers are distributed ANN tokens.

**Solidity**

```text
Comptroller troll = Comptroller(0xABCD...);
(bool isListed, uint collateralFactorMantissa, bool isAnnexd) = troll.markets(0x3FDA...);
```

**Web3 1.0**

```javascript
const troll = Comptroller.at(0xABCD...);
const result = await troll.methods.markets(0x3FDA...).call();
const {0: isListed, 1: collateralFactorMantissa, 2: isAnnexd} = result;
```

