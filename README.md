# NihilS Validator Node. 0G Labs


### Validator Details

Operator Address: 0gvaloper1alq9prmm9ea8pk46r2cj79rdk93qfakmmynw62

Node Status: Active

Network: 0G Testnet

### Validator Node

**Hardware Specifications:**

CPU: 8 vCPUs

RAM: 32 GB

Storage: 1 TB SSD

Network Bandwidth: 1 Gbps

**Software Specifications:**

Operating System: Ubuntu 20.04 LTS

0G Node Version: Latest release (e.g., v1.0.0)

**Installation and Setup**

System Update and Dependencies Installation

```
sudo apt-get update && sudo apt-get upgrade -y
sudo apt-get install build-essential jq -y
```

Go Installation

```
wget https://golang.org/dl/go1.16.4.linux-amd64.tar.gz
tar -C /usr/local -xzf go1.16.4.linux-amd64.tar.gz
echo "export PATH=$PATH:/usr/local/go/bin" >> ~/.profile
source ~/.profile
```

Clone 0G Repository and Build

```
git clone https://github.com/0G-Network/0g
cd 0g
make install
```

Initialize Node

```
0gd init "NihilS-Validator" --chain-id 0g-testnet
```

Configure Node

```
Update ~/.0g/config/genesis.json with the latest genesis file.
Configure ~/.0g/config/config.toml for networking and peers.
```

Start the Node

```
0gd start
```
### Node Performance and Monitoring:

Snapshots: Regular snapshots are taken to ensure quick recovery in case of failure.

```
0g tendermint unsafe-reset-all
wget -O ~/.0g/data/priv_validator_state.json https://snapshot.url/priv_validator_state.json
wget -O ~/.0g/data/ https://snapshot.url/data.tar.gz
tar -xzvf data.tar.gz -C ~/.0g/data/
```

Logs Monitoring:

```
tail -f ~/.0g/logs/0g.log
```

System Metrics Monitoring: Utilizing Prometheus and Grafana for real-time metrics.

```
prometheus:
  scrape_configs:
    - job_name: '0g_node'
      static_configs:
        - targets: ['localhost:26660']
```
**Reports:**

Uptime Reports: Maintained 99.9% uptime since inception.

Voting Power: Actively participating in governance with [X%] voting power.

Delegations: Secure and transparent delegation policies in place.

Security Measures:

Firewall: Configured to only allow essential ports.

```
sudo ufw allow 26656,26657/tcp
sudo ufw enable
```

Backups: Regular backups of validator keys and state.

```
cp ~/.0g/config/priv_validator_key.json /backup/location/
cp ~/.0g/config/node_key.json /backup/location/
```

**Community Engagement:**

Support: Actively participating in the 0G community forums and support channels.

Updates: Regular updates and maintenance to ensure node compliance with network upgrades.

# Storage Node. 0G Labs

### Hardware Specifications:

CPU: 16 vCPUs

RAM: 64 GB

Storage: 4 TB SSD

Network Bandwidth: 1 Gbps

### Software Specifications:

Operating System: Ubuntu 20.04 LTS

0G Storage Node Version: Latest release (e.g., v1.0.0)

### Installation and Setup:

System Update and Dependencies Installation

```
sudo apt-get update && sudo apt-get upgrade -y
sudo apt-get install build-essential jq -y
```

Go Installation:

```
wget https://golang.org/dl/go1.16.4.linux-amd64.tar.gz
tar -C /usr/local -xzf go1.16.4.linux-amd64.tar.gz
echo "export PATH=$PATH:/usr/local/go/bin" >> ~/.profile
source ~/.profile
```
Clone 0G Storage Repository and Build:

```
git clone https://github.com/0G-Network/storage
cd storage
make install
```
Initialize Node:

```
0g-storage init "NihilS-Storage" --chain-id 0g-testnet
```
Configure Node:
```
Update ~/.0g-storage/config/genesis.json with the latest genesis file.
Configure ~/.0g-storage/config/config.toml for networking and peers.
```
Start the Node:

```
0g-storage start
```
Node Performance and Monitoring:

Data Integrity: Regular integrity checks and backups.

Logs Monitoring:

```
tail -f ~/.0g-storage/logs/storage.log
```
System Metrics Monitoring: Utilizing Prometheus and Grafana for real-time metrics.

```
prometheus:
  scrape_configs:
    - job_name: '0g_storage_node'
      static_configs:
        - targets: ['localhost:26660']
```

### Reports:

Uptime Reports: Maintained 99.9% uptime since inception.

Data Stored: Managing [X TB] of data with high availability and redundancy.

Security Measures:

Firewall: Configured to only allow essential ports.

```
sudo ufw allow 26656,26657/tcp
sudo ufw enable
```

Backups: Regular backups of storage data and state.

```
rsync -avz ~/.0g-storage/data/ /backup/location/
```
**Community Engagement:**

Support: Actively participating in the 0G community forums and support channels.

Updates: Regular updates and maintenance to ensure node compliance with network upgrades.

# KV Node. 0G Labs

### Hardware Specifications:

CPU: 8 vCPUs

RAM: 32 GB

Storage: 1 TB SSD

Network Bandwidth: 1 Gbps

### Software Specifications:

Operating System: Ubuntu 20.04 LTS

0G KV Node Version: Latest release (e.g., v1.0.0)

Installation and Setup:

System Update and Dependencies Installation:

```
sudo apt-get update && sudo apt-get upgrade -y
sudo apt-get install build-essential jq -y
```
Go Installation:

```
wget https://golang.org/dl/go1.16.4.linux-amd64.tar.gz
tar -C /usr/local -xzf go1.16.4.linux-amd64.tar.gz
echo "export PATH=$PATH:/usr/local/go/bin" >> ~/.profile
source ~/.profile
```
Clone 0G KV Repository and Build:

```
git clone https://github.com/0G-Network/kv
cd kv
make install
```
Initialize Node:

```
0g-kv init "NihilS-KV" --chain-id 0g-testnet
```
Configure Node:
```
Update ~/.0g-kv/config/genesis.json with the latest genesis file.
Configure ~/.0g-kv/config/config.toml for networking and peers.
```
Start the Node:

```
0g-kv start
```
### Node Performance and Monitoring:

**Data Integrity: Regular integrity checks and backups.**

Logs Monitoring:

```
tail -f ~/.0g-kv/logs/kv.log
System Metrics Monitoring: Utilizing Prometheus and Grafana for real-time metrics.
```

```
prometheus:
  scrape_configs:
    - job_name: '0g_kv_node'
      static_configs:
        - targets: ['localhost:26660']
```

### Reports:

Uptime Reports: Maintained 99.9% uptime since inception.

Data Managed: Efficiently managing key-value pairs with low latency and high availability.

### Security Measures:

Firewall: Configured to only allow essential ports.

```
sudo ufw allow 26656,26657/tcp
sudo ufw enable
```
Backups: Regular backups of KV store data and state.

```
rsync -avz ~/.0g-kv/data/ /backup/location/
```
### Community Engagement:
Support: Actively participating in the
