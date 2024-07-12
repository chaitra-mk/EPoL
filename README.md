# EPoL: An Efficient Consensus in Blockchain Using Machine Learning


Proof of Work (PoW) describes a consensus mechanism that requires a significant amount of computing effort from a network of devices, commonly known as mining. In a typical PoW system, miners compete to solve cryptographic puzzles, where the goal is to find a specific nonce value using the SHA-256 algorithm. This process is computationally intensive and requires significant energy expenditure, as miners must repeatedly hash different nonce values until the correct one is found. However, the energy consumed in this process could be directed towards more meaningful computational tasks. Machine learning models can be trained to solve real-world problems, and their integration into blockchain could enhance the system’s overall utility. This approach can also mitigate the issue of resource wastage associated with traditional PoW mechanisms.

In this project, we have implemented machine learning algorithms to select miners in the Ethereum network. By considering accuracy as a key parameter, we ensure that miners are chosen based on their contribution to solving practical problems. This not only promotes fairer competition but also aligns the computational efforts of miners with meaningful tasks, thereby enhancing the overall efficiency and utility of the blockchain system.

## Implementation

We have implemented a multi-node configuration of Ethereum by incorporating the Efficient Proof of Learning (EPoL) consensus mechanism. Specifically, we focused on the ethash files and used the Go programming language to develop our new consensus algorithm, EPoL. In this new approach, we replaced the code of the PoW consensus mechanism with our implementation, which involves training datasets using machine learning algorithms.

###Below are the steps to run EPoL setup on Ubuntu :

Step 1 : 
Download Ethereum Files from official website :


Step 2 :  Create a folder ethereum and nodes as subfolder in home directory where the ethreum files downloaded must be present.

<details>
<summary>Click to copy</summary>
```bash
mkdir ethereum
cd ethereum
mkdir node1 node2 node3 node4
</details>
Nodes must be created, each with a unique account hash and authentication (password), functioning as participants in the system. These nodes were connected to their respective accounts. To achieve this, we used "geth," an executable file generated , which facilitates the creation and running of Ethereum nodes. 


Next, we made a special file called a genesis file in a simple JSON format to initialize the blockchain. This file was created using "puppeth," a tool that helps manage private Ethereum networks. The genesis file includes the hash of the accounts and acts as an initializer for the blockchain. This file is linked to all nodes.

We then generated a "boot node" to aid in the effective communication of nodes. The bootnode generates a bootkey, which must be running in the background to help nodes stay connected in the network. With all preparations complete, we started the blockchain on each terminal representing each node, with each node using its communication channel (port). This process ensures our modified blockchain with the EPoL consensus mechanism starts up successfully.

With the preparations complete, we started the blockchain on each terminal representing a node. Each node uses its communication port to interact with the network, ensuring our modified blockchain with the EPoL consensus mechanism starts up successfully. This design ensures that the transition from PoW to EPoL is smooth, with all nodes functioning cohesively in the network.
