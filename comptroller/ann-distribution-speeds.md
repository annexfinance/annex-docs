# ANN Distribution Speeds

## ANN Speed

The "ANN speed" unique to each market is an unsigned integer that specifies the amount of ANN that is distributed, per block, to suppliers and borrowers in each market. This number can be changed for individual markets by calling the `_setAnnexSpeed` method through a successful Annex Governance proposal.

The following is the formula for calculating the rate that ANN is distributed to each supported market.

```text
utility = aTokenTotalBorrows * assetPrice

utilityFraction = utility / sumOfAllAnnexdMarketUtilities

marketAnnexSpeed = annexRate * utilityFraction
```

## ANN Distributed Per Block \(All Markets\)

The Comptroller contract’s `annexRate` is an unsigned integer that indicates the rate at which the protocol distributes ANN to markets’ suppliers or borrowers, every Ethereum block. The value is the amount of ANN \(in wei\), per block, allocated for the markets. Note that not every market has ANN distributed to its participants \(see Market Metadata\).

The annexRate indicates how much ANN goes to the suppliers or borrowers, so doubling this number shows how much ANN goes to all suppliers and borrowers combined. The code examples implement reading the amount of ANN distributed, per Ethereum block, to all markets.

**Comptroller**

```text
uint public annexRate;
```

**Solidity**

```text
Comptroller troll = Comptroller(0xABCD...);

// ANN issued per block to suppliers OR borrowers * (1 * 10 ^ 18)
uint annexRate = troll.annexRate();

// Approximate ANN issued per day to suppliers OR borrowers * (1 * 10 ^ 18)
uint annexRatePerDay = annexRate * 4 * 60 * 24;

// Approximate ANN issued per day to suppliers AND borrowers * (1 * 10 ^ 18)
uint annexRatePerDayTotal = annexRatePerDay * 2;
```

**Web3 1.2.6**

```javascript
const comptroller = new web3.eth.Contract(comptrollerAbi, comptrollerAddress);

let annexRate = await comptroller.methods.annexRate().call();
annexRate = annexRate / 1e18;

// ANN issued to suppliers OR borrowers
const annexRatePerDay = annexRate * 4 * 60 * 24;

// ANN issued to suppliers AND borrowers
const annexRatePerDayTotal = annexRatePerDay * 2;
```

## ANN Distributed Per Block \(Single Market\)

The Comptroller contract has a mapping called `annexSpeeds`. It maps aToken addresses to an integer of each market’s ANN distribution per Ethereum block. The integer indicates the rate at which the protocol distributes ANN to markets’ suppliers or borrowers. The value is the amount of ANN \(in wei\), per block, allocated for the market. Note that not every market has ANN distributed to its participants \(see Market Metadata\).

The speed indicates how much ANN goes to the suppliers or the borrowers, so doubling this number shows how much ANN goes to market suppliers and borrowers combined. The code examples implement reading the amount of ANN distributed, per Ethereum block, to a single market.

**Comptroller**

```text
mapping(address => uint) public annexSpeeds;
```

**Solidity**

```text
Comptroller troll = Comptroller(0x123...);
address aToken = 0xabc...;

// ANN issued per block to suppliers OR borrowers * (1 * 10 ^ 18)
uint annexSpeed = troll.annexSpeeds(aToken);

// Approximate ANN issued per day to suppliers OR borrowers * (1 * 10 ^ 18)
uint annexSpeedPerDay = annexSpeed * 4 * 60 * 24;

// Approximate ANN issued per day to suppliers AND borrowers * (1 * 10 ^ 18)
uint annexSpeedPerDayTotal = annexSpeedPerDay * 2;
```

**Web3 1.2.6**

```javascript
const aTokenAddress = '0xabc...';

const comptroller = new web3.eth.Contract(comptrollerAbi, comptrollerAddress);

let annexSpeed = await comptroller.methods.annexSpeeds(aTokenAddress).call();
annexSpeed = annexSpeed / 1e18;

// ANN issued to suppliers OR borrowers
const annexSpeedPerDay = annexSpeed * 4 * 60 * 24;

// ANN issued to suppliers AND borrowers
const annexSpeedPerDayTotal = annexSpeedPerDay * 2;
```

