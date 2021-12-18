# FAQ

## Why do we need ScanDAO in the first place?

Dollar-pegged stablecoins have become an essential part of crypto due to their
lack of volatility as compared to tokens such as Bitcoin and Ether. Users are
comfortable with transacting using stablecoins knowing that they hold the same
amount of purchasing power today vs. tomorrow. But this is a fallacy. The dollar
is controlled by the US government and the Federal Reserve. This means a
depreciation of dollar also means a depreciation of these stablecoins.

ScanDAO aims to solve this by creating a free-floating reserve currency, SCAN,
that is backed by a basket of assets. By focusing on supply growth rather than price
appreciation, ScanDAO hopes that SCAN can function as a currency that is able
to hold its purchasing power regardless of market volatility.

## Is SCAN a stable coin?

No, SCAN is not a stable coin. Rather, SCAN aspires to become an algorithmic reserve currency backed by other decentralized assets. Similar to the idea of the gold standard, SCAN provides free floating value its users can always fall back on, simply because of the fractional treasury reserves SCAN draws its intrinsic value from.

## SCAN is backed, not pegged.

Each SCAN is backed by 1 BUSD, not pegged to it. Because the treasury backs every SCAN with at least 1 BUSD, the protocol would buy back and burn SCAN when it trades below 1 BUSD. This has the effect of pushing SCAN price back up to 1 BUSD. SCAN could always trade above 1 BUSD because there is no upper limit imposed by the protocol. Think pegged == 1, while backed &gt;= 1.

You might say that the SCAN floor price or intrinsic value is 1 BUSD. We believe that the actual price will always be 1 BUSD + premium, but in the end that is up to the market to decide.

## How does it work?

At a high level, ScanDAO consists of its protocol managed treasury, protocol owned liquidity \([POL](../references/glossary.md#pol)\), bond mechanism, and staking rewards that are designed to control supply expansion.

Bond sales generate profit for the protocol, and the treasury uses the profit to mint SCAN and distribute them to stakers. With [liquidity bonds](../references/glossary.md#liquidity-bonds), the protocol is able to accumulate its own liquidity. Check out the entry below on [the importance of POL](basics.md#why-is-pol-important).

## What is the deal with \(3,3\) and \(1,1\)?

\(3,3\) is the idea that, if everyone cooperated in ScanDAO, it would generate the greatest gain for everyone \(from a [game theory](https://en.wikipedia.org/wiki/Game_theory) standpoint\). Currently, there are three actions a user can take:

* Staking \(+2\)
* Bonding \(+1\)
* Selling \(-2\)

Staking and bonding are considered beneficial to the protocol, while selling is considered detrimental. Staking and selling will also cause a price move, while bonding does not \(we consider buying SCAN from the market as a prerequisite of staking, thus causing a price move\). If both actions are beneficial, the actor who moves price also gets half of the benefit \(+1\). If both actions are contradictory, the bad actor who moves price gets half of the benefit \(+1\), while the good actor who moves price gets half of the downside \(-1\). If both actions are detrimental, which implies both actors are selling, they both get half of the downside \(-1\).

Thus, given two actors, all scenarios of what they could do and the effect on the protocol are shown here:

![](../.gitbook/assets/game_theory.png)

* If we both stake \(3, 3\), it is the best thing for both of us and the protocol \(3 + 3 = 6\).
* If one of us stakes and the other one bonds, it is also great because staking takes SCAN off the market and put it into the protocol, while bonding provides liquidity and BUSD for the treasury \(3 + 1 = 4\).
* When one of us sells, it diminishes effort of the other one who stakes or bonds \(1 - 1 = 0\).
* When we both sell, it creates the worst outcome for both of us and the protocol \(-3 - 3 = -6\).

## Why is PCV important?

As the protocol controls the funds in its treasury, SCAN can only be minted or burned by the protocol. This also guarantees that the protocol can always back 1 SCAN with 1 BUSD. You can easily define the risk of your investment because you can be confident that the protocol will indefinitely buy SCAN below 1 BUSD with the treasury assets until no one is left to sell. You can't trust the FED but you can trust the code.

As the protocol accumulates more PCV, more runway is guaranteed for the stakers. This means the stakers can be confident that the current staking APY can be sustained for a longer term because more funds are available in the treasury.

## Why is POL important?

ScanDAO [owns most of its liquidity](https://dune.xyz/shadow/ScanDAO-%28SCAN%29) thanks to its bond mechanism. This has several benefits:

* ScanDAO does not have to pay out high farming rewards to incentivize liquidity

  providers a.k.a renting liquidity.

* ScanDAO guarantees the market that the liquidity is always there to facilitate

  sell or buy transaction.

* By being the largest LP \(liquidity provider\), it earns most of the LP fees which

  represents another source of income to the treasury.

* All POL can be used to back SCAN. The LP tokens are marked down to their risk-free

  value for this purpose.

## What will happen if there is a bank run on ScanDAO?

Fractional reserve banking works because depositors don’t withdraw their funds all at once. A depositor’s faith in the banking system rests on regulations and agencies like Federal Deposit Insurance Corporation \(FDIC\).

SCAN does not have FDIC insurance but it has an incentive structure that protects stakers. Let’s take a look at how it performs during a hypothetical bank run. In this scenario, we assume the majority of stakers would panic and unstake their tokens from ScanDAO - the staking percentage which stands at 92% now quickly collapses to 3.3%, leaving only 55,000 SCAN staked.

Next, we assume the Risk-Free Value \(RFV\) inflows to the treasury completely dry up. For context, RFV is currently growing at [about $1 million every 2 days](https://dune.xyz/queries/29153/58862). However, during a bank run this growth will likely stop.

Finally, we assume that those last standing stakers bought in at a price of $500 per SCAN. The initial investment of these stakers would be:

$$
\$500/SCAN * 55,000\ SCAN = \$27.5\ million
$$

As of September 15 2021, the total SCAN supply is 2,082,553 and the RFV is $47,041,833. Remember that 1 SCAN is backed by 1 USD \(BUSD\). By subtracting these two numbers, we know 44,959,280 SCAN will eventually get issued to the remaining stakers. In roughly a year, these stakers who are holding 55,000 SCAN will have:

$$
55,000 + 44,959,280 = 45,014,280\ SCAN
$$

$27.5 million investment made by these stakers will turn into about $45 million based on cash flow alone if they stay staked \(recall that 1 SCAN is backed by 1 USD\). In this bank run scenario, the stakers who stay staked not only get their money back, but also make some profit. Therefore, [\(3,3\)](basics.md#what-is-the-deal-with-3-3-and-1-1) isn’t just a popular meme, it is actually a dominant strategy.

The above scenario is unlikely to play out because when other people find out that extremely high rewards are being paid to the stakers, they will copy the strategy by buying and staking SCAN. This is also why the percentage of SCAN staked in ScanDAO has consistently remained over 90% since launch.

_Note: Most of the data referenced above are taken from_ [_this Dune Analytics page_](https://duneanalytics.com/shadow/ScanDAO-%28SCAN%29)_._

## Why is the market price of SCAN so volatile?

It is extremely important to understand how early in development the ScanDAO protocol is. A large amount of discussion has centered around the current price and expected a stable value moving forward. The reality is that these characteristics are not yet determined. The network is currently tuned for expansion of SCAN supply, which when paired with the staking, bonding, and yield mechanics of ScanDAO, result in a fair amount of volatility.

SCAN could trade at a very high price because the market is ready to pay a hefty premium to capture a percentage of the current market capitalization. However, the price of SCAN could also drop to a large degree if the market sentiment turns bearish. We would expect significant price volatility during our growth phase so please **do your own research** whether this project suits your goals.

## What is the point of buying it now when SCAN trades at a very high premium?

When you buy and stake SCAN, you capture a percentage of the supply \(market cap\) which will remain close to a constant. This is because your staked SCAN balance also increases along with the circulating supply. The implication is that if you buy SCAN when the market cap is low, you would be capturing a larger percentage of the market cap.

## What is a rebase?

Rebase is a mechanism by which your staked SCAN balance increases automatically. When new SCAN are minted by the protocol, a large portion of it goes to the stakers. Because stakers only see staked SCAN balance instead of SCAN, the protocol utilizes the rebase mechanism to increase the staked SCAN balance so that 1 staked SCAN is always redeemable for 1 SCAN.

## What is reward yield?

Reward yield is the percentage by which your staked SCAN balance increases on the next epoch. It is also known as _rebase rate_. You can find this number on the [ScanDAO staking page](https://app.scandao.com/#/stake).

## What is APY?

APY stands for annual percentage yield. It measures the real rate of return on your principal by taking into account the effect of compounding interest. In the case of ScanDAO, your staked SCAN represents your principal, and the compound interest is added periodically on every epoch \(2200 Ethereum blocks, or around 8 hours\) thanks to the rebase mechanism.

One interesting fact about APY is that your balance will grow not linearly but exponentially over time! Assuming a busdly compound interest of 2%, if you start with a balance of 1 SCAN on day 1, after a year, your balance will grow to about 1377. That is a lot!

![The power of compounding](../.gitbook/assets/apy.png)

## How is the APY calculated?

The APY is calculated from the reward yield \(a.k.a rebase rate\) using the following equation:

$$
APY = ( 1 + rewardYield )^{1095}
$$

It raises to the power of 1095 because a rebase happens 3 times busdly. Consider there are 365 days in a year, this would give a rebase frequency of 365 \* 3 = 1095.

Reward yield is determined by the following equation:

$$
rewardYield = SCAN_{distributed} / SCAN_{totalStaked}
$$

The number of SCAN distributed to the staking contract is calculated from SCAN total supply using the following equation:

$$
SCAN_{distributed} = SCAN_{totalSupply} \times rewardRate
$$

## Why does the price of SCAN become irrelevant in long term?

As illustrated above, your SCAN balance will grow exponentially over time thanks to the power of compounding. Let's say you buy an SCAN for $400 now and the market decides that in 1 year time, the intrinsic value of SCAN will be $2. Assuming a busdly compound interest rate of 2%, your balance would grow to about 1377 SCANs by the end of the year, which is worth around $2754. That is a cool $2354 profit! By now, you should understand that you are paying a premium for SCAN now in exchange for a long-term benefit. Thus, you should have a long time horizon to allow your SCAN balance to grow exponentially and make this a worthwhile investment.

## What will be SCAN's intrinsic value in the future?

There is no clear answer for this, but the intrinsic value can be determined by the treasury performance. For example, if the treasury could guarantee to back every SCAN with 100 BUSD, the intrinsic value will be 100 BUSD. It can also be decided by the DAO. For example, if the DAO decides to raise the price floor of SCAN, its intrinsic value will rise accordingly.

## How does the protocol manage to maintain the high staking APY?

Let’s say the protocol targets an APY range of 1,000% to 10,000%, this would translate to a *minimum* reward yield of about 0.2105%,
or a busdly growth of about 0.6328%. Please refer to the equation above to learn
[how APY is calculated from the reward yield](basics.md#how-is-the-apy-calculated).

If there are 100,000 of SCAN staked right now, the protocol would need to mint an
additional 632.8 SCAN to achieve this busdly growth. This is achievable if the protocol
can bring in at least $632.80 of busdly revenue from bond sales. Even if the protocol
doesn't bring in that much revenue, it can still sustain 1,000% APY for a considerable
amount of time (see the [runway chart](https://dune.xyz/queries/102766/207436)
for instance) due to the excess reserve in the treasury.

## Do I have to unstake and stake SCAN on every epoch to get my rebase rewards?

No. Once you have staked SCAN with ScanDAO, your staked SCAN balance will auto-compound on every epoch. That increase in balance represents your rebase rewards.

## How do I track my rebase rewards?

You can track your rebase rewards by calculating the increase in your staked SCAN balance.

1. Record down the Current Index value on the [staking page](https://app.scandao.com/#/) when you first stake your SCAN. Let's call this the Start Index.

![](../.gitbook/assets/index_old.png)

1. After staking for some time, if you want to determine by how much your balance has increased, check the Current Index value again. Let's call this the End Index.

![](../.gitbook/assets/index_new.png)

1. By dividing the End Index by Start Index, you would get the ratio by which your staked SCAN balance has increased.

$$
ratio = endIndex / startIndex
$$

1. In this example, the SCAN balance has grown by 1.5 times.

$$
ratio = 13.2\ /\ 8.8\newline = 1.5
$$
