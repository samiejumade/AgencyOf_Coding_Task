### Blockchain.js

* **newBlock** (proof, previousHash) => block
  Generate a new block given the already calculated proof and the previous Hash and returns the obtained block
* **newTransaction** (sender, receiver, amount) => transaction
  Generate a new transaction and adds it to the currentTransactions array which will be added in the next new block
* **mine** (miner) => block
  Mines a new block, assigns it to the miner and generate the associated block

### Network.js

* **registerNode** (address) => boolean
  Enable the insertion of new nodes and returns if the address has been added (cannot add twice the same address)
* **nodeExists** (address) => boolean
  Fetches in the nodes array if the provided node already exists and returns this information

**$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$**
 the checkChain function you have implemented fulfills the requirements.

It checks if the current chain is valid by iterating over each block in the chain and performing two checks:

It checks if the previousHash of the current block matches the hash of the previous block. If it doesn't, the function returns an empty array, indicating that the chain is not valid.

It checks if the proof of the current block matches the calculated hash of the current block. If it doesn't, the function returns an empty array, indicating that the chain is not valid.

If the function iterates over all the blocks without finding any discrepancies, it returns the chain, indicating that the chain is valid.

So, the function correctly checks the validity of the chain and returns either the chain (if it's valid) or an empty array (if it's not).