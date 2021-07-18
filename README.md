# Public RPC Asset Management

<div class="bg-gray-dark">
<img src="https://github.com/Ether1Project/Ether-1-Branding/raw/master/PNG%20Logos/ethoProtocolBlack.png" width="200" />
</div>

## Overview

This repo will help manage all public contributions to Etho Protocol public RPC services on the [Etho Protocol Network](https://docs.ethoprotocol.com/ethofs/ethofs-introduction).

## Installation Instructions

1) Install Etho Protocol Node (Geth) From [Latest Releases ](https://github.com/Ether1Project/Ether1/releases/tag/V1.5.0).
2) Install Example System Service Below
3) Open Pull-Request In This Repo & Add Your Public IP Address to ipaddresses.json

## Example System Service
```
[Unit]
Description=Etho Protocol RPC Node

[Service]
Type=simple

User=ethonode
Group=ethonode

ExecStart=/usr/sbin/geth --rpc --rpcaddr 127.0.0.1 --rpcport 8545 --rpcapi "web3,eth,net,utils" --rpccorsdomain "*" --rpcvhosts "*"

Restart=always

[Install]
WantedBy=default.target
```
