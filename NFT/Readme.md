# Tutorial Understanding:
1. In this tutorial we understand how to mint NFT using the tools that are provided by Moralis.

2. Moralis offers an integration iwth IPFS which is a solution for decentralized storage.

3. We need to have an active ethereum address to send transactions to the blockchain.

4. We can find the NFT on Opensea once minted through the app.

# Initial Steps
1. Requires python3, if you don't have it there are multiple resources online on how to install it according to your platform.
2. Set a virtual environment with `Python3 -m venv venv`
3. Initialize your virtual environment with `source venv/bin/activate` (For Mac and Linux).
4. Intall the dependencies with `pip install -r requirements.txt`

![NFT minting app image](app/app%20image.png)

# Indulging in the code
1. A simple flask app consisting index.html (with all the elements we need for the dapp such as interaction buttons to interact with metamask), importantly consists the file element, with which we can upload and mint the NFT with our logic.

2. The logic.js file also includes the metadata of the NFT(name, descriptions, etc.), the code required to communicate with the IPFS. 
A new moralis file object is created and saved easily through a moralis server or IPFS, in a decentralized way. We receive the hash of the file which helps to identify that there are no duplicates in the network. 
The mintToken function is called which is given in the smart contract (present in the contract_base folder).

3. The transaction contains the encoded function call as a parameter and is sent to the blockchain. When we get the transaction hash back we know that the transaction has been processed and then we can print to the user the transaction Id and that means that the NFT has been printed.

