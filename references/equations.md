# Equations

## Staking

$$
deposit = withdrawal
$$

Swaps between SCAN and DAL during staking and unstaking are always honored 1:1. The amount of SCAN deposited into the staking contract will always result in the same amount of DAL. And the amount of DAL withdrawn from the staking contract will always result in the same amount of SCAN.

$$
rebase = 1 - ( scanDeposits / DALOutstanding )
$$

The treasury deposits SCAN into the distributor. The distributor then deposits SCAN into the staking contract, creating an imbalance between SCAN and DAL. DAL is rebased to correct this imbalance between SCAN deposited and DAL outstanding. The rebase brings DAL outstanding back up to parity so that 1 DAL equals 1 staked SCAN.

## Bonding

$$
bond Price = 1 + Premium
$$

SCAN has an intrinsic value of 1 BUSD, which is roughly equivalent to $1. In order to make a profit from bonding, ScanDAO charges a premium for each bond.

$$
Premium = debt Ratio * BCV
$$

The premium is derived from the debt ratio of the system and a scaling variable called [BCV](https://docs.scandao.com/references/glossary#bcv). BCV allows us to control the rate at which bond prices increase.

The premium determines profit due to the protocol and in turn, stakers. This is because new SCAN is minted from the profit and subsequently distributed among all stakers.

$$
debt Ratio = bondsOutstanding/scanSupply
$$

The debt ratio is the total of all SCAN promised to bonders divided by the total supply of SCAN. This allows us to measure the debt of the system.

$$
bondPayout_{reserveBond} = marketValue_{asset}\ /\ bondPrice
$$

Bond payout determines the number of SCAN sold to a bonder. For [reserve bonds](https://docs.scandao.com/references/glossary#reserve-bonds), the market value of the assets supplied by the bonder is used to determine the bond payout. For example, if a user supplies 1000 BUSD and the bond price is 250 BUSD, the user will be entitled 4 SCAN.

$$
bondPayout_{lpBond} = marketValue_{lpToken}\ /\ bondPrice
$$

For [liquidity bonds](https://docs.scandao.com/references/glossary#liquidity-bonds), the market value of the LP tokens supplied by the bonder is used to determine the bond payout. For example, if a user supplies 0.001 SCAN-BUSD LP token which is valued at 1000 BUSD at the time of bonding, and the bond price is 250 BUSD, the user will be entitled 4 SCAN.

## SCAN Supply

$$
SCAN_{supplyGrowth} = SCAN_{stakers} + SCAN_{bonders} + SCAN_{DAO} + SCAN_{pscanExercise}
$$

SCAN supply does not have a hard cap. Its supply increases when:

* SCAN is minted and distributed to the stakers.
* SCAN is minted for the bonder. This happens whenever someone purchases a bond.
* SCAN is minted for the DAO. This happens whenever someone purchases a bond. The DAO gets the same number of SCAN as the bonder.
* SCAN is minted for the team, investors, advisors, or the DAO. This happens whenever

  the aforementioned party exercises their pSCAN.

$$
SCAN_{stakers} = SCAN_{totalSupply} * rewardRate
$$

At the end of each epoch, the treasury mints SCAN at a set [reward rate](https://docs.scandao.com/references/glossary#reward-rate). These SCAN will be distributed to all the stakers in the protocol. You can track the latest reward rate on the [ScanDAO Policy dashboard](https://dune.xyz/shadow/ScanDAO-Policy).

$$
SCAN_{bonders} = bondPayout
$$

Whenever someone purchases a bond, a set number of SCAN is minted. These SCAN will not be released to the bonder all at once - they are vested to the bonder linearly over time. The bond payout uses a different formula for different types of bonds. Check the [bonding section above](equations.md#bonding) to see how it is calculated.

$$
SCAN_{DAO} = SCAN_{bonders}
$$

The DAO receives the same amount of SCAN as the bonder. This represents the DAO profit.

$$
SCAN_{pscanExercise} = pSCAN + BUSD
$$

The individual would supply 1 pSCAN along with 1 BUSD to mint 1 SCAN. The pSCAN is subsequently burned.

## Backing per SCAN

$$
SCAN_{backing} = treasuryBalance_{stablecoin} + treasuryBalance_{otherAssets}
$$

Every SCAN in circulation is backed by the ScanDAO treasury. The assets in the treasury can be divided into two categories: stablecoin and non-stablecoin.

$$
treasuryBalance_{stablecoin} = RFV_{reserveBond} + RFV_{lpBond}
$$

The stablecoin balance in the treasury grows when bonds are sold. [RFV](https://docs.scandao.com/references/glossary#rfv) is calculated differently for different bond types.

$$
RFV_{reserveBond} = assetSupplied
$$

For reserve bonds such as BUSD bond, the RFV simply equals to the amount of the underlying asset supplied by the bonder.

$$
RFV_{lpBond} = 2sqrt(constantProduct) * (\%\ ownership\ of\ the\ pool)
$$

For LP bonds such as SCAN-BUSD bond, the RFV is calculated differently because the protocol needs to mark down its value. Why? The LP token pair consists of SCAN, and each SCAN in circulation will be backed by these LP tokens - there is a cyclical dependency. To safely guarantee all circulating SCAN are backed, the protocol marks down the value of these LP tokens, hence the name _risk-free_ value \(RFV\).

