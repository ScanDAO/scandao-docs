# Stake Your SCAN \(3, 3\)

Sometimes, the ScanDAO website might not be accessible due to hosting issues. Fear not, you can still interact with the ScanDAO contracts to perform certain actions such as staking. In this guide, we will show you how to stake SCAN tokens via [BSCscan](https://bscscan.com/).

If you have never staked SCAN before, there are two steps involved:

1. Approve the staking contract to spend your SCAN tokens.
2. Stake your SCAN tokens.

If you have staked SCAN before, there is only one step to perform: Stake your SCAN tokens.

## How to Approve SCAN Spending via BSCscan

1. Go to the [Write Contract section of the SCAN token contract](https://bscscan.com/address/0xaf2cC765A04a3A4B554f368796Cec2B7eAF44746).
2. Check and ensure your selected network is "BSC Mainnet" in your wallet. Then press **Connect to Web3** to connect your wallet if you haven't done so.
3. Once it is connected, select the third option _approve_.
4. On the _spender \(address\)_ field, we would fill in the [staking contract address](../contracts/staking.md#staking). Enter this value: **0xC8C436271f9A6F10a5B80c8b8eD7D0E8f37a612d**
5. On the _amount \(uint256\)_ field, fill in the amount of SCAN you would like the staking contract to spend on your behalf, and multiply it by 1e9. Alternatively, you can use [this calculator](https://docs.google.com/spreadsheets/d/1vm48OCBnVh8uah0-3Xa7HqFwmfxgcrMIWPrOllSFIvA/edit?usp=sharing) to perform the conversion for you. If you don't want to repeat this step whenever you want to stake, you can choose a very large value. Let's say you want to allow the contract to spend up to 1e9 SCAN on your behalf, you would enter: **1000000000000000000**
6. Click **Write**.
7. Sign the transaction on Metamask and wait for it to complete.

## How to Stake SCAN via BSCscan

1. Go to the [Write Contract section of the staking contract](https://bscscan.com/address/0xaf2cC765A04a3A4B554f368796Cec2B7eAF44746#writeContract).
2. Check and ensure your selected network is "BSC Mainnet" in your wallet. Then press **Connect to Web3** to connect your wallet if you haven't done so.
3. Once it is connected, select the _stake_ option.
4. On the _\_amount \(uint256\)_ field, fill in the amount you wish to stake, and multiply it by 1e9. Alternatively, you can use [this calculator](https://docs.google.com/spreadsheets/d/1vm48OCBnVh8uah0-3Xa7HqFwmfxgcrMIWPrOllSFIvA/edit?usp=sharing) to perform the conversion for you. For example, if you want to stake 1 SCAN, fill in the value: **1000000000**
5. Click **Write**.
6. Sign the transaction on Metamask and wait for it to complete.
