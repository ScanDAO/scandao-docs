# DAO

## DAO

The DAO contract is an address guarded by a simple gnosis safe implementation.
The DAO address holds all the DAO funds accumulated over time. For instance the
DAO receives SCAN from every bond sold by the protocol. The DAO address also
holds funds from strategic investments. Below are listed DAO addresses

- [0x245c...988B](https://bscscan.com/address/0xe546da3B567E312d3Fb45266694fa3B628F5F5C4)

The DAO contract is guarded by a 3 of 5 multisig. That means any transaction for
making DAO changes must be approved by at least 3 signers, of which we have 5
signers in total. The operation security for our DAO is thus protected from a
single actor going rogue, because it takes a quorum of 3 to authorize any
transaction like engaging in DAO swaps. The 5 signing addresses for the DAO are
listed below.

Note that all signers can be verified on
[GnosisSafe](https://gnosis-safe.io/app/#/safes/0xe546da3B567E312d3Fb45266694fa3B628F5F5C4/settings/owners).
