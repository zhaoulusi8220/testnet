# Services

**Chain ID**: nolus-rila | **Latest Version Tag**: v0.1.43 | **Wasm**: ON


## Public endpoints

* api: [https://api.nolus.botga.gq](https://api.nolus.botga.gq)
* rpc: [https://rpc.nolus.botga.gq](https://rpc.nolus.botga.gq)
* grpc: [https://grpc.nolus.botga.gq](https://grpc.nolus.botga.gq)
* grpc-web: [https://grpc-web.nolus.botga.gq](https://grpc.nolus.botga.gq)

## Peering

**state-sync**

```text
d5519e378247dfb61dfe90652d1fe3e2b3005a5b@nolus-testnet.rpc.kjnodes.com:43656
```

**seed-node**

```text
3f472746f46493309650e5a033076689996c8881@nolus-testnet.rpc.kjnodes.com:43659
```

**addrbook**
```bash
curl -Ls https://snapshots.kjnodes.com/nolus-testnet/addrbook.json > $HOME/.nolus/config/addrbook.json
```

**live-peers** (4)
```bash
peers="d5519e378247dfb61dfe90652d1fe3e2b3005a5b@65.109.68.190:43656,87e0efe332fdc4b0c2a76d18761a936509762067@212.41.9.98:36656,3fc0879882601b7d80117f7db73ab9880898e0ea@168.119.89.31:45656,7a1fc4d1cc0ffec7db6a2a15496136e62561b162@161.97.146.108:26656"
sed -i -e "s|^persistent_peers *=.*|persistent_peers = \"$peers\"|" $HOME/.nolus/config/config.toml
```
