# README

## Overview
This Java program interacts with an LACNet Ethereum-based blockchain network using Web3j. It connects to the network, creates and signs a transaction with ```Falcon-512 Post-Quantum Private Key``` and sends it to a smart contract. Additionally, it verifies the transaction's success and decodes any potential revert reasons.

## Features
- Connects to a private Ethereum network via Web3j.
- Loads user credentials from a private key.
- Constructs a transaction to interact with a smart contract.
- Signs and sends the transaction.
- Verifies transaction success or failure.
- Decodes revert reasons for failed transactions.

## Requirements
- Java 8 or later
- Web3j library
- Bouncy Castle Crypto Library
- An Ethereum-compatible private network node
- A smart contract deployed on the network

## Installation
1. Clone this repository:
   ```sh
   git clone https://github.com/your-repository.git
   cd your-repository
   ```
2. Add dependencies to your project:
   ```xml
   <dependencies>
       <dependency>
           <groupId>org.web3j</groupId>
           <artifactId>core</artifactId>
           <version>4.8.7</version>
       </dependency>
       <dependency>
           <groupId>org.bouncycastle</groupId>
           <artifactId>bcprov-jdk15on</artifactId>
           <version>1.70</version>
       </dependency>
   </dependencies>
   ```

## Configuration
Replace the following placeholders with your actual values:
```properties
NODE_IP={{YOUR_NODE_IP}}
PRIVATE_KEY={{YOUR_PRIVATE_KEY}}
CONTRACT_ADDRESS={{YOUR_CONTRACT_ADDRESS}}
NODE_ADDRESS={{YOUR_NODE_ADDRESS}}
```

## Usage
1. Compile and run the program:
   ```sh
   javac -cp .:path-to-web3j-core.jar:path-to-bcprov-jdk15on.jar Main.java
   java -cp .:path-to-web3j-core.jar:path-to-bcprov-jdk15on.jar com.lacnet.Main
   ```
2. The program will output:
   - The transaction hash upon success.
   - An error message if the transaction fails.

## Troubleshooting
- Ensure the node URL is correct and accessible.
- Check that the private key matches an account with sufficient funds.
- Make sure the smart contract address is correct.
- If a transaction fails, check the revert reason for more details.

## License
This project is licensed under the MIT License.




