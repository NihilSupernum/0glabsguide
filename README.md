# NihilS Validator Node. Vana


### How to Run a DLP Validator

Welcome to running a Data Liquidity Pool (DLP) validator! This guide will help you get started with validating user data for specific DLPs.

#### Getting Started

1. **Join Discord**: Please join in [Discord](https://discord.com/invite/withvana) to get an overview of all existing DLPs and how to access them.

2. **Minimum Requirements**:
   - **Hardware**: 1 CPU, 8GB RAM, 10GB free disk space.
   - **Cloud Providers**: You can run validators on cloud platforms like GCP, AWS, or Azure.

#### Steps to Run a Validator

1. **Choose a DLP**: Select the DLP you want to validate for.

2. **Validator Registration**:
   - Register as a validator through the DLP's smart contract.
   - Ensure you meet the minimum staking requirements for the DLP.

3. **Approval Process**: Wait for your registration request to be approved by the DLP.

4. **Node Deployment**:
   - Deploy the validator node specific to the chosen DLP.
   - Confirm that your validator is running correctly. Check your logs for validation like this:

![image](https://github.com/user-attachments/assets/420fee50-ae5e-453d-b2c5-1b0f3d4f4385)




5. **Track Your Stats**: Congratulations, your validator is up and running! Monitor your stats and trust score on-chain.

#### Deploy Validators

Once your validator is built, you can deploy it to form a peer-to-peer network within the DLP. Ensure each node has a static IP for easier communication. Each node must also have a wallet to register with the DLP and start serving proof-of-contribution requests.

#### Smart Contract Deployment

1. **Clone and Modify**: Clone the DLP smart contract template and modify it according to your DLP's specific needs.

2. **Deployment**: Follow the README instructions to deploy the modified smart contract to the network.

#### Validator Registration

The DLP smart contract manages validator registrations, allowing them to maintain network integrity and earn rewards for contributions. To register a new node, create a wallet and call the registration function in the DLP smart contract.

#### Scoring Process

Validators earn rewards for validating uploaded files based on data metrics relevant to the DLP. Rewards are distributed every 1800 blocks (~3 hours) using the Nagoya consensus process:

- **Consensus Process**: Validators score each other based on assessment quality and operational performance.
- **Emission Calculation**: Rewards are calculated based on validator rank and consensus scores, ensuring fair distribution aligned with contributions to the DLP.

By following these steps, you can effectively run a DLP validator and contribute to the integrity and security of the network. For further assistance, visit our Discord community in the #testnet-help channel.
