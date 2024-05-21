# Services

**Chain ID**: initiation-1 | **Latest Version Tag**: v0.2.15 | **Wasm**: ON


## Public endpoints

* api: [https://api.initia.xhiro.my.id/](https://api.initia.xhiro.my.id/)
* rpc: [https://rpc.initia.xhiro.my.id/](https://rpc.initia.xhiro.my.id/)
* grpc: [https://grpc.initia.xhiro.my.id/](https://grpc.initia.xhiro.my.id/)

# Snapshot

## Instructions

### First, create a session

```bash
screen -R install
```

### Stop the service and reset the data

```bash
sudo systemctl stop initiad
cp $HOME/.initia/data/priv_validator_state.json $HOME/.initia/priv_validator_state.json.backup
rm -rf $HOME/.initia/data
```

### Download latest snapshot

```bash
curl https://snapshot.initia.xhiro.my.id/hiro-initia-testnet_latest.tar.lz4 | lz4 -dc - | tar -xf - -C $HOME/.initi
mv $HOME/.initia/priv_validator_state.json.backup $HOME/.initia/data/priv_validator_state.json
```

### Restart the service and check the log

```bash
sudo systemctl start initiad && sudo journalctl -u initiad -f --no-hostname -o cat
```
### Log out and log in session

```bash
to get out of
ctrl + a + d

to enter the session
screen -r name_session
```

