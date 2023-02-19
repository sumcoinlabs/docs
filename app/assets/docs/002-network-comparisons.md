# Comparison with other blockchain networks

Sumcoin is best compared with its sibling - Bitcoin; however in the following table we'll show how it bodes against something vastly different like Ethereum. Sumcoin was invented as response to increasing doubts on Bitcoin's PoW consensus model with regards to its increasing centralization and conflict of interests between miners. Sumcoin can be understood as a Proof-of-Stake clone of Bitcoin, though that is an oversimplification as Sumcoin differs vastly - especially when it comes to economics and incentives of the system.
Major differences between the two are the fee market, ie. the absence of it in Sumcoin and Sumcoin's dedication to continual token distribution via PoW block rewards while the Bitcoin's distribution rate (also PoW block rewards) is reduced geometrically every four years until it becomes zero.

## Consensus algorithm

Sumcoin is secured by Proof-of-Stake consensus. Proof-of-Work uses energy as a scarce resource as means of selecting a block producer, while Proof-of-Stake uses time as a scare resource measured in "coin age". Once a transaction has reached an age of thirty days, these coins become eligible for participation in consensus. Mature UTXOs are used as proof of stake and are presented as evidence throught the "coinstake" transaction of a new block. [Reference client](https://github.com/sumcoinlabs/sumcoin) will try to find a new block once every second. If block is accepted by the network, a reward will be given to the minter. After ninety (90) days, a transaction reaches its maximum maturity and minting probability is at its highest. This minting can be done by simple, very low energy computers, such as a raspberry pi, making the process energy efficient when compared to Proof-of-Work power consumption.

Another benefit of Sumcoin's Proof-of-Stake mechanism is its monetary cost of attack. With Proof-of-Work, and individual can attempt to generate and verify faulty blocks without holding the Proof-of-Work coin or even a majority of the coin supply. Sumcoin requires the  malicious individual to hold Sumcoin with a coin age of a one day minimum, as well as being required to hold a majority sum of the Sumcoin supply, increasing their risk massively. This makes such an attack economically unviable. The requirement of those verifying the blockchain to hold a portion of the supply means investors are protected from malicious outside sources who hold no coins.  Those who hold Sumcoin and use the network, share interest in the security of the chain.

## Distribution

Sumcoin was initially distributed via PoW block rewards. At the time of writing there are 200,000,000 SUM mined through POW with no annual inflation of of any kind.
There is a final number of Sumcoins that can be mined, which is 200 Million coins.  As of 2023, no further Sumcoins will come into supply and validation of Transactions are strictly handled by Proof-of-Stake (POS).


## Fee market

The fee market provides a mechanism to decide which transactions have priority over the others, and to create economic incentives for the transaction validators who usually claim the fees as rewards. Transaction fees are claimed by the block miner in both Bitcoin and Ethereum economic systems. This provides the miners the incentive to validate and include transactions in the blocks they mine. If Alice wants her transaction to be included in the next block, she should set transaction fee higher and pay more then other network users, ie. outbid them. It is presumed that miners, as rational subjects, will first include transactions which carry the most Bitcoin value. If Alice pays a transaction fee which is under the average fee at the time she might wait for several blocks (or hundreds of blocks) to see her transaction included and confirmed. So, it is obvious that the fee market serves as the incentive for miners to process and include the transactions in the blocks they mine.
With Bitcoin's block size limit set to 1MB there exists an artificial upward pressure on the price of transaction fees - incentivizing miners to validate the transactions. This is especially important as Bitcoin's economy is expected to run on transaction fees alone when the block subsidies eventually stop.

Sumcoin's fees are fixed at 0.01 SUM per kb and are burned. This is equivalent to paying the transaction fee to each Sumcoin holder in proportion to their Sumcoin holdings since the fee decreases the total supply of Sumcoins. This property eliminates the need for a fee market on Sumcoin's network and allows every transaction to get included in the very next block. Sumcoin retains the 1MB block size limit as it is based on the Bitcoin code, but it has no intricate need to keep it. The block size limit will definitely be increased as Sumcoin's network grows in usage. Sumcoin developers have already hinted that Sumcoin will feature a dynamic block size in the near future.
Due to these economic properties of Sumcoin a question arises: Why do Sumcoin miners bother processing the transactions?

From a spectator looking at this from a Bitcoin oriented perspective the answer is that Sumcoin block miners want to process transactions so they allow Sumcoins to be burned - thus making their own stake in the network more valuable.
However when the intricacies of PoS are learned it is understood that with Sumcoin minters (PoS miners) include transactions because it doesn't cost much to include them, while producing empty blocks reduces the value of the blockchain, and therefore of their stake. The burned fees are not really an argument as the effect on their holdings is negligible.
Bitcoin miners always start off mining an empty block, otherwise they lose the time it takes to validate the transactions and signatures, as time is money on the Bitcoin network. Only after they have validated the txns to include and have computed the merkle root, they start mining blocks with txns.
While for PoS, the time advantage is negligible as you can still use the stake hash of a few seconds ago.

## Block size limit and block time spacing

Bitcoin features the 1MB block size limits which serves to place the upward pressure on the transaction fee price, Sumcoin copies this parameter from the Bitcoin but it's economic model does not depend on scarcity of the block space.
While block generation is a stochastic process, each chain is targeted to generate blocks based on a real time interval. Bitcoin generates a block every 10 Minutes, akin to Sumcoin PoS block generation, while Ethereum generates a block every 12 seconds.  Sumcoin PoW block generation is coupled to PoS block generation as well as PoW hash power and is therefore difficult to approximate, but the total block time of Sumcoin can be empirically estimated to be around 30 Seconds. Considering this and the block size limit of 1MB, Bitcoin has a transaction per second (TPS) of about 7 tps, Sumcoin has an estimated 133 tps, and Ethereum has about 25 tps.

<table>
<thead>
<tr>
<th>Features</th>
<th>Bitcoin</th>
<th>Sumcoin</th>
<th>Ethereum</th>
</tr>
</thead>
<tbody>
<tr>
<td>Main use-case:</td>
<td>p2p financial transactions / store of value</td>
<td>p2p financial transactions / store of value</td>
<td>Turing complete smart contracts</td>
</tr>
<tr>
<td>Consensus algorithm:</td>
<td>PoW</td>
<td>PoS</td>
<td>PoW</td>
</tr>
<tr>
<td>Active since:</td>
<td>2009</td>
<td>2018</td>
<td>2015</td>
</tr>
</tr>
<tr>
<td>Distribution method:</td>
<td>PoW block reward</td>
<td>PoW block reward / PoS block reward</td>
<td>Initial Coin Offering / PoW block reward / POS</td>
</tr>
<tr>
<td>Distribution:</td>
<td>Limited, until 21M tokens exist in the system.</td>
<td>Limited, 200M</td>
<td>Unlimited.</td>
</tr>
</tr>
<tr>
<td>Transaction fee:</td>
<td>Fee market (~390 satoshis/byte)</td>
<td>Static 0.01 SUM/kb (~0.2 Btc satoshis/byte)</td>
<td>Fee market (~23 Gwei/byte)</td>
</tr>
<tr>
<td>Estimated transaction bandwidth:</td>
<td>7 tx/sec</td>
<td>133 tx/sec</td>
<td>25 tx/sec</td>
</tr>
<tr>
<td>Block time:</td>
<td>10 Minutes</td>
<td>30 Seconds</td>
<td>12 seconds</td>
</tr>
<tr>
<td>Block size:</td>
<td>1MB</td>
<td>1MB</td>
<td>Dynamic</td>
</tr>
<tr>
<td>Extra transaction data size limit:</td>
<td>80 Byte<br />(OP_RETURN)</td>
<td>256 Byte<br />(OP_RETURN)</td>
<td>Dynamic<br />(5 gas / byte)</td>
</tr>
<tr>
<td>Topology:</td>
<td>Public blockchain</td>
<td>Public blockchain</td>
<td>Public blockchain</td>
</tr>
</tbody>
</table>
Table 1. Comparison of Crypto currency attributes
(prices of transactions at the time of writing)

---
