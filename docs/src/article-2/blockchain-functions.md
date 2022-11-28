# How The Blockchain Functions
----------------------------

Now that we understand some of the key characteristics of a blockchain, lets dive into how the blockchain itself works.

## The Blocks
**Transactions** that occur will be added to a pending **transactions** list. These **transactions** are picked up by a **miner** and placed into the **block** of data the **miner** is **mining** for. This **block** will also contain other data such as the **date and time** it is being mined, what the **hash of the previous block** was, as well as an **ID** usually representative of which **block** it is in the **chain**. If a **pending transaction** has not been added to a **block** for a specific length of time, it will be forced to be added to the next **block** or the **block** will not be valid. A **block** can store far more data than I listed here, but these are the core assets nearly always within a **block**. There are various complex algorithms required to '**find/mine**' a **block**, meaning that **miners** need to spend considerable processing power before being able to find a **block**, thus regulating the pace at which **blocks** are found and added to the **chain**, which in turn allows enough time for other **miners** and members to validate **blocks** that are being added.

## The Chain
Now that we understand what a **block** is and what it can hold as well as that it is **mined** by **miners**, lets look at how the **chain** of **blocks** itself, functions. **Blocks** are connected to the previous **block** through data such as the **ID** and the **previous hash** stored within the **block** itself. Due to data such as this and the **date/time** being stored in these **blocks**, it is very hard to alter **blocks** since it is set in stone which **block** came after the other. Each block therefore "*strengthens the verification of the previous block and hence the entire blockchain. This renders the blockchain tamper-evident, delivering the key strength of immutability*".<sup>[\[7\]](https://www.ibm.com/topics/what-is-blockchain)</sup> As such, we have a chain of blocks that contain transactions that can be trusted by all members of the network.