# How The Blockchain Functions
----------------------------

Now that we understand some of the key characteristics of a blockchain, lets dive into how the blockchain itself works.

## Block Chain Basics
- a blockchain consists of connected blocks
- every block contains specific information (usually transaction related) as well as a reference to the previous block (usually a hash)
- blocks can be validated and added to the chain through completing complex algorithms (proof of work)
- no central network for data; the entire blockchain is stored on every node (a group of computers usually), known as peer-to-peer network

## The Blocks
**Transactions** that occur will be added to a pending **transactions** list. These **transactions** are picked up by a **miner** and placed into the **block** of data the **miner** is **mining** for. This **block** will also contain other data such as the **date and time** it is being mined, what the **hash of the previous block** was, as well as an **ID** usually representative of which **block** it is in the **chain**. If a **pending transaction** has not been added to a **block** for a specific length of time, it will be forced to be added to the next **block** or the **block** will not be valid. A **block** can store far more data than I listed here, but these are the core assets nearly always within a **block**. There are various complex algorithms required to '**find/mine**' a **block**, meaning that **miners** need to spend considerable processing power before being able to find a **block**, thus regulating the pace at which **blocks** are found and added to the **chain**, which in turn allows enough time for other **miners** and members to validate **blocks** that are being added. Below is a brief explanation of hash functions.

### Hash Functions
A hash function is *"a mathematical algorithm that maps data of arbitrary size to a bit string of a fixed size and is a one-way function, that is, a function which is practically infeasible to invert"*.

Knowing the hash function, it is easy to verify that the data maps to a given hash value, thus hash strings of blocks in a blockchain can be easily checked to see if they map to the correct data that that block should contain. The reverse however, is hard to do, hence why hash functions are perfect for usage in blockchains.

Encryption is simply a function that takes in a value and applies a secret key (a parameter) to return an encrypted value. Using that same secret key will decrypt the encrypted value back to the original value.

Hashing can not be reversed to reveal the original value, however, it always produces the same hash value if the same input is provided. The more complex a hashing algorithm, the lower the probability of more than one input providing the same hash (something you absolutely do not want in production). This is also known as **collision**. Most production-ready hashes such as SHA are essentially collision resistant.

## The Chain
Now that we understand what a **block** is and what it can hold as well as that it is **mined** by **miners**, lets look at how the **chain** of **blocks** itself, functions. **Blocks** are connected to the previous **block** through data such as the **ID** and the **previous hash** stored within the **block** itself. Due to data such as this and the **date/time** being stored in these **blocks**, it is very hard to alter **blocks** since it is set in stone which **block** came after the other. Each block therefore "*strengthens the verification of the previous block and hence the entire blockchain. This renders the blockchain tamper-evident, delivering the key strength of immutability*".<sup>[\[7\]](https://www.ibm.com/topics/what-is-blockchain)</sup> As such, we have a chain of blocks that contain transactions that can be trusted by all members of the network.

## The Mining
Even though the value of cryptocurrencies is related to the usage of that currency in every day life as well as it's supply, the incentive for miners to solve the math problems required by a particular blockchain also determines this value. Usually blocks need to be aproved by other miners, thus the more people mining in a blockchain, the more secure it becomes.

Usually, blocks in a blockchain require the hashes to start with specific values, such as several 0s. You need to include the data of the transactions plus a custom added value to alter the hash to produce the 0s at the start. For example, *Bitcoin* currently needs '19' 0s at the start of a block for that block to be valuable. The more 0s needed at the start, the harder the block is to mine.

### The Zeroes

The number of miners partaking in a blockchain directly determines how many zeroes are required in the hashed value of a block. This is because a blockchain wants to keep a systematic rate of new blocks being added to the chain for security reasons (roughly a block every 10/15 minutes is a good rate). The reason for this is so that every block can be checked in due time while still not taking too long to verify existing transactions and add another block to the chain to keep the cryptocurrency end-users happy. Furthermore, it is important to note that in real blockchains, usually each block concatenate several transactions (around 2500 per block) for efficiency reasons.