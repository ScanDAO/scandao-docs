# Stake Your SCAN \(3, 3\)

Staking allows you to earn SCAN passively via auto-compounding. By staking your SCAN with ScanDAO, you receive DAL \(staked SCAN\) in return at a 1:1 ratio. After that, your DAL balance will increase automatically on every epoch based on the current APY.

Check out this video on how to get SCAN and stake it on ScanDAO:

{% embed url="https://www.youtube.com/watch?v=aXAE1ikVMpM" caption="How to get SCAN and stake it on ScanDAO" %}

## How to Buy SCAN

{% hint style="warning" %}
There are several venues to purchase SCAN: [Sushiswap](https://app.sushi.com/swap), [Uniswap](https://app.uniswap.org/#/swap), or DEX aggregators such as [matcha](https://matcha.xyz/). Make sure to **check the slippage first** before buying SCAN, as some venue offers worse rate than the others due to low liquidity.
{% endhint %}

1. Go to [this Sushiswap swap page](https://app.sushi.com/swap?outputCurrency=0x383518188c0c6d7730d91b2c03a03c837814a899). We use Sushiswap as an example here. It is recommended to compare the exchange rate across different DEXes to ensure you are getting the best price.

2. Make sure the output currency is SCAN. You can also copy and paste the [SCAN contract address](../contracts/tokens.md#scan) into the output currency field to ensure you are swapping for the right token.

![Paste SCAN contract address](../.gitbook/assets/scan_contract.png)

3. You can select any input currency based on your available wallet balance. It is recommended to use BUSD as the input currency to minimize the slippage.

![Make sure the output currency is SCAN](../.gitbook/assets/buy_scan.png)

4. Select the amount of SCAN you want to swap for. Then click "Approve" and sign the transaction.

5. After the "Approve" transaction has been processed successfully, click "Swap" and sign the transaction.

6. You should see SCAN in your wallet balance now after the swap transaction is successful. If you cannot find it in your wallet, add [SCAN contract address](../contracts/tokens.md#scan) to your wallet.

{% hint style="info" %}
The "Approve" transaction is only needed when you swap SCAN for the first time; subsequent swapping only requires you to perform the "Swap" transaction.
{% endhint %}

## How to Stake

1. Go to the [Stake page of the ScanDAO website](https://app.scandao.com/#/). Select the "Stake" tab.
2. Enter the amount of SCAN that you would like to stake in the input field. If you would like to stake all your SCAN, press the "Max" button and the input field will be populated with all your available SCAN balance.
3. Click "Approve" and sign the transaction.
4. After the "Approve" transaction has been processed successfully, click "Stake" and sign the transaction. Voila, you have staked your SCAN!

## How to Unstake

1. Go to the [Stake page of the ScanDAO website](https://app.scandao.com/#/). Select the "Unstake" tab.
2. Enter the amount of DAL that you would like to unstake in the input field. If you would like to unstake all your DAL, press the "Max" button and the input field will be populated with all your available DAL balance.
3. Click "Approve" and sign the transaction.
4. After the "Approve" transaction has been processed successfully, click "Unstake" and sign the transaction.

_Note: The "Approve" transaction is only needed when staking/unstaking for the first time; subsequent staking/unstaking only requires you to perform the "Stake" or "Unstake" transaction._

## Reading the Info

![The staking page](../.gitbook/assets/staking_page_index.png)

**APY** tells you the annualized rate of return based on the reward yield. It takes into account the effect of compounding since DAL rebases exponentially.

**TVL** measures the dollar amount of all the staked SCAN in ScanDAO.

**Current Index** allows you to track your gain from staking. The index started from 1 at epoch 0, and increases every epoch. If you staked at genesis \(epoch 0\) and never unstaked any SCAN, your balance today would be X times greater, where X is the current index. You can use the index to track your position by marking down the index number when you stake and unstake. You divide the index number when you unstake by the index number when you stake to get the ratio by which your DAL balance has increased.

**Your Balance** tells you how many unstaked SCAN are in your wallet. This is the maximum amount that you can stake.

**Your Staked Balance** tells you how many staked SCAN are in your wallet. This is the maximum amount that you can unstake.

**Next Rebase** tells you the remaining time until the next rebase.

**Reward Yield** tells you how much your DAL balance will increase when the next epoch begins. For example, if you stake 100 SCAN and the upcoming rebase is 0.5427%, your DAL balance would increase from 100 to 100.5427.

**ROI \(5-Day Rate\)** estimates how much your DAL balance will increase after 5 days, if the reward yield stays the same during this period. For example, if you stake 100 SCAN and the rate is 8.4577%, your DAL balance would increase from 100 to 108.4577 after 5 days.

