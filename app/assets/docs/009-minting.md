# Proof-of-Stake

>Sumcoin uses both the Proof-of-Work and Proof-of-Stake algorithms. The PoW algorithm is used to spread the distribution of new coins. 100% of all Sumcoins were created with PoW. Proof-of-Stake is then used to secure the network: The chain with longest PoS coin age wins in case of a blockchain split-up.

`Minting`, as it is called in Sumcoin to make a proof-of-stake block, is based on metrics of an unspent transaction.
If we take a look at the number one spot of the rich list, transaction c7293fc60c80bdcc374775d1f0734e0766465b905bae1a312fe487793be3b8f7 has among others the following characteristics:

* The transaction appeared in block 376161 at timestamp 1531750952 (Unix time).
* The transaction in the block has an offset of 383 bytes. It is the third transaction in the block. The size of the first two transactions in the block are respectively 78 and 224 bytes.
* The transaction timestamp is 1531750624. (As of Sumcoin 0.11, the block timestamp is to be used instead of the transaction timestamp)
* The second recipient (index 1) received 1786301.06651300 Sumcoins which, at the moment, is still unspent.

These metrics, along with two more data points serves as a basis to calculate a hash for POS minting:

* a future timestamp X (in Unix time notation) in which the stake could win;
* a block modifier that was set by the network 1830080 seconds (~21 days) earlier than X.

Every 6 hours the network calculates a new block modifier to be used for POS minting.

The win in proof-of-stake minting, the calculated hash is compared to the current difficulty minus the coinage. The chances of finding a stake therefor improves when either the coin age increases or when the difficulty of the network decreases.

## Sumcoin minting behavior

* The Minting process can only start after 1 day of coin-age.
* Minting coin age is maxed out after 90 days. Which means that after 90 days the only variable left in PoS is the current difficulty.
* Minting is predictable and not random. For a given transaction, you can calculate the maximum network PoS difficulty over time for your transaction to be able to mint a PoS block.
* Whenever this PoS difficulty is higher than the current network PoS difficulty your Sumcoin client can mint a PoS block.
* PoS blocks can be rejected (orphans) if several people mint a PoS block within a given window (2 hours also called time-drift). Only one (the chain with longest coin age) will be accepted.
* Minting splits the transaction in two if coin age < 90 days.
* PoS block reward is the total tx fees for the solved block.
* A transaction that just staked has its coins locked for 100 confirmations (about 1.5 hours).
* Merging transactions, spending coins, etc. burns coinage (resets it to 0).
* The PoS reward is directly added to your transaction which staked (if this transaction is split in two because coinage < 90 days, the reward is equally distributed to both resulting transactions).

## Sumcoin v20.2 Proof-of-Stake protocol

![Sumcoin PoS diagram](../img/pos-diagram.svg)

## Qualities of Proof-of-Stake Consensus

### Efficient
Sumcoin's implementation of Proof-of-Stake mining is highly efficient, as the network's security does not rely on extensive energy consumption (also known as proof-of-energy-burn). Instead, users invest their coins and time to emulate the Proof-of-Work (PoW) process. This is achieved by launching the wallet app, sending coins to their address, and allowing them to remain idle until selected by the protocol to mint the next block. This energy and cost-efficient process is made possible by Sumcoin's adoption of Proof-of-Stake mining.

### Aligning interests
Proof-of-Stake mining involves coin owners producing new blocks, thereby creating a network in which the security providers and users are one and the same. This approach eliminates the existence of a distinct group of security providers whose sole interest lies in profit, with no direct connection to the network. Instead, all security providers are required to own a stake in the network through the ownership of Sumcoin. This shared financial investment in the long-term future of the network reduces the likelihood of conflicts arising between different factions with varying opinions on how the blockchain should evolve and develop. By linking security providers and network users, Proof-of-Stake mining contributes to a more unified and collaborative approach to blockchain development.

### User governance
Sumcoin is one of the first blockchain platforms that provide users with the power to produce blocks, thereby influencing and determining the network's future direction. This unique ability to participate in user governance is a natural extension of the Proof-of-Stake (PoS) consensus mechanism. Sumcoin's innovative approach enables users to govern the protocol rules directly, which is a groundbreaking development in the blockchain space. Unlike traditional centralized systems, where rules and governance are controlled by a small group of individuals, Sumcoin provides a more democratic and decentralized approach. With Sumcoin, users can play an active role in shaping the network's future by participating in user governance.

### Global network
Sumcoin's Proof-of-Stake consensus mechanism provides a significant advantage over other blockchain platforms, as it allows a larger number of users to participate in block creation without requiring large amounts of resources. By making the minting process more accessible, Sumcoin expands the number of people who can take part in block creation, which ultimately leads to a more decentralized network. Furthermore, this approach also means that security providers are no longer limited to geographical locations with cheap electricity. Since the cost of operating a Proof-of-Stake node is relatively low, anyone, anywhere in the world, can set up a minting node and participate in securing the network. This increased accessibility and global participation are critical factors that enable Sumcoin to achieve a high level of decentralization and global security.

### Network security is price independent
Proof-of-stake minting in Sumcoin provides a unique incentive structure for network security. Unlike proof-of-work, minters are not solely dependent on the market price of the native token to ensure profitability. Compensation is provided to incentivize consistent network security, but since the minting process is so inexpensive, minters can voluntarily operate nodes without compensation if they choose. This creates a more decentralized and secure network, as the stakeholder community is directly invested in the success of the blockchain. Additionally, minters have a voice in the future development of the network through the ability to choose which version of the protocol to run. This flexibility, along with the ability to secure their overall investment, are two reasons stakeholders may choose to run nodes for free. However, automatic compensation is still provided, making it even more beneficial to participate. Sumcoin has proven its resilience by maintaining network security during low demand periods, suggesting it can withstand any future market challenges.

### Higher Resistance to Censorship
The proof-of-stake mechanism used by Sumcoin enables a globally decentralized security network that makes it extremely difficult to censor and shut down. Similar to a bittorrent network, where many people around the world operate nodes holding a full copy of a file, pieces of the Sumcoin blockchain are held by nodes all around the world. This makes it very challenging for a single entity or government to target and shut down the network. As long as one node exists, the blockchain can continue to function and be accessed from anywhere in the world. This global network of security providers also ensures that the network is less susceptible to attacks or centralization by a single group or entity. This type of decentralized security is a crucial aspect of the value proposition offered by Sumcoin and other similar proof-of-stake networks.

Sumcoin's proof-of-stake mechanism allows for the decentralized operation of minting nodes from anywhere in the world, provided there is access to a computer, electricity, internet connection, and some Sumcoin. This geographical decentralization makes the Sumcoin network highly resilient to any attempts to shut it down, as it becomes increasingly difficult as the number of nodes grows. With a vast network of nodes, censoring Sumcoin would be almost impossible due to its robust, peer-to-peer structure. Each node operates as a peer, working together to process transactions and maintain the integrity of the network. This structure ensures the security and decentralization of the network, making it a trusted and reliable system for its users.

---
