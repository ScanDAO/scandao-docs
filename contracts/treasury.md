# Treasury

## SCAN / BUSD LP

- [0x34d7...ef7c](https://bscscan.com/address/0xbD4e58e19c96CC9889375DC5A9Cc0309E430627D)

## Treasury

The treasury contract is a simple vault implementation holding all the funds
collected by the protocol. If for instance a user purchases a BUSD bond, the
bonded BUSD is fully taken in by the treasury in return of the market equivalent
of SCAN bonded for. New SCAN will be minted based on the RFV of the treasury
assets. Below are listed treasury contracts by version, where the latest version
represents the currently active contract.

- [0x886C...399D](https://bscscan.com/address/0xeeA3b1b175b9B18Abe2eb7Acd8C810468e0fF7B1)

The treasury contract is guarded by a 3 of 5 multisig. That means any
transaction for the treasury must be approved by at least 3 signers, of which we
have 5 signers in total. The operation security for our treasury assets is thus
protected from a single actor going rogue, because it takes a quorum of 3 to
authorize any transaction like moving funds in and out. The 5 signing addresses
for our treasury are listed below.

Note that the DAO and the Treasury signers are the same, since the DAO is the
manager of the Treasury contract.
