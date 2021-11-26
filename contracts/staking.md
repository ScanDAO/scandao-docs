# Staking

## Distributor

The distributor contract receives minted SCAN from the treasury in order to drip-feed rewards to stakers. The reward rate target as of time of writing is set to 3500, which translates to 0.35% of total supply, since the reward rate is defined in tens of thousands. Note that the reward rate determines the rebase rate and that the rebase rate determines the APY. Below are listed distributor contracts.

- [0xbe73...242f](https://bscscan.com/address/0xbe731507810C8747C3E01E62c676b1cA6F93242f)

## Staking

The staking contract works with a staking helper contract \([0xC8C4....612d](https://bscscan.com/address/0xC8C436271f9A6F10a5B80c8b8eD7D0E8f37a612d)\). The staking helper contract calls "stake" and then "claim" of the staking contract. When the "stake" function is called, DAL is put into a warmup phase and all the information about how much DAL a user has staked is stored in the staking contract. When the "claim" function is called, DAL is retrieved from the warmup and then sent to the user's wallet.
