# Services

**Chain ID**: nolus-rila | **Latest Version Tag**: v0.1.43 | **Wasm**: ON


## Public endpoints

* api: [https://api.nolus.botga.gq](https://api.nolus.botga.gq)
* rpc: [https://rpc.nolus.botga.gq](https://rpc.nolus.botga.gq)
* grpc: [https://grpc.nolus.botga.gq](https://grpc.nolus.botga.gq)
* grpc-web: [https://grpc-web.nolus.botga.gq](https://grpc.nolus.botga.gq)

# Snapshot

## Instructions

### Stop the service and reset the data

```bash
sudo systemctl stop nolusd
cp $HOME/.nolus/data/priv_validator_state.json $HOME/.nolus/priv_validator_state.json.backup
rm -rf $HOME/.nolus/data
```

### Download latest snapshot

```bash
curl -L http://snapshot.nolus.botga.gq/nolus/nolus-snapshot.tar.lz4 | tar -Ilz4 -xf - -C $HOME/.nolus
mv $HOME/.nolus/priv_validator_state.json.backup $HOME/.nolus/data/priv_validator_state.json
```

### Restart the service and check the log

```bash
sudo systemctl start nolusd && sudo journalctl -u nolusd -f --no-hostname -o cat
```
