Simple Blockchain

This code was put together to demonstrate the basic innerworkings of a blockchain system similar to bitcoin's.

To run this program, navigate to the project folder and run the command "mvn exec java". 

This project models a simple (non-distributed) blockchain, with auto-generated transactions set to a fixed amount. Within the program, Merkle Trees are contrustructed from these transactions by a mining node. The mining node attempts to find a nonce that can be appended to the Merkle Root of the tree and SHA-256 hashed to be less than a set difficulty level (itentionally set low since this project is just for demostration). When found, a block is created and added to the blockchain with the transactions used to generate the Merkle Tree, with the Merkle Root of the tree being used as the block identifier (stored within the block's header). The Merkle Root of the previous block is also stored in the block's header as a reference, allowing for quick and simple validataion of the entire chain. The next steps to this project would be the distribution of the mining node code (likely via docker) as well as a registration node, and the introduction of a wallet application for non-mining nodes to create transactions. This project was created for Introduction to Blockchain at University of Chicago.
