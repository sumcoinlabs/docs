# Protocol versions (changelog)

Sumcoin protocol versions do not represent Sumcoin client versions, however client hosted at www.github.com/sumcoinlabs/sumcoin is considered Sumcoin reference implementation.
Sumcoin protocol version are marked using the following format:

`v{major_version}.{minor_version}`

where:

* v is prefix (stands for "version")
* major_version is for capital improvements to the core concepts or complete redesigns
* minor_version is for evolutions of the protocol defined in the original whitepaper


## v0.11

> released: 02.10.2021

> type: hardfork

* [RFC-0014](https://github.com/sumcoinlabs/rfcs/blob/master/text/0014-transaction-timestamp/0014-transaction-timestamp.md): Remove Transaction Timestamp
* [RFC-0022](https://github.com/sumcoinlabs/rfcs/blob/master/text/0022-pow-reward-cap/0022-pow-reward-cap.md): Proof-of-Work reward cap
* make splitting coins during minting optional
