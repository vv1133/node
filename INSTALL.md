---
## Mysterium VPN node (Any OS with Docker)
https://hub.docker.com/r/mysteriumnetwork/mysterium-node/
### Installation
```bash
sudo apt-get install docker.io
sudo docker run --cap-add NET_ADMIN --net host --publish "1194:1194" -e "NODE=123456" --name mysterium-node -d mysteriumnetwork/mysterium-node:{VERSION}
```
### Running
```bash
sudo docker start mysterium-node
sudo docker stop mysterium-node
```
### Debugging
```bash
sudo docker logs -f mysterium-node
```


## Mysterium VPN node (Debian && Ubuntu) - tested on Ubuntu 14.04
### Download
 * https://github.com/MysteriumNetwork/node/releases/download/{VERSION}/mysterium-node_linux_amd64.deb
 * https://github.com/MysteriumNetwork/node/releases/download/{VERSION}/mysterium-node_linux_i386.deb
 * https://github.com/MysteriumNetwork/node/releases/download/{VERSION}/mysterium-node_linux_armhf.deb
### Installation
```bash
wget https://github.com/MysteriumNetwork/node/releases/download/{VERSION}/mysterium-node_linux_amd64.deb
sudo dpkg --install --force-depends mysterium-node_linux_amd64.deb
sudo apt-get install --fix-broken
```
### Running
```bash
sudo service mysterium-node start
sudo service mysterium-node status
```
### Debugging
```bash
sudo tail -f /var/log/mysterium-node/*
sudo mysterium_server --config-dir=/etc/mysterium-node --runtime-dir=/tmp --node=123456
```


## Mysterium VPN client (Debian && Ubuntu) - tested on Ubuntu 14.04
### Download
 * https://github.com/MysteriumNetwork/node/releases/download/{VERSION}/mysterium-client_linux_amd64.deb
 * https://github.com/MysteriumNetwork/node/releases/download/{VERSION}/mysterium-client_linux_i386.deb
 * https://github.com/MysteriumNetwork/node/releases/download/{VERSION}/mysterium-client_linux_armhf.deb

### Installation
```bash
wget https://github.com/MysteriumNetwork/node/releases/download/{VERSION}/mysterium-client_linux_amd64.deb
sudo dpkg --install --force-depends mysterium-client_linux_amd64.deb
sudo apt-get install --fix-broken
```
### Running
```bash
sudo service mysterium-client start
sudo service mysterium-client status
```
### Debugging
```bash
sudo tail -f /var/log/mysterium-client/*
sudo mysterium_client --runtime-dir=/tmp --node=123456
```


## Mysterium VPN node (standalone Linux binaries)
### Download
 * https://github.com/MysteriumNetwork/node/releases/download/{VERSION}/mysterium_server_linux_amd64
 * https://github.com/MysteriumNetwork/node/releases/download/{VERSION}/mysterium_server_linux_386
 * https://github.com/MysteriumNetwork/node/releases/download/{VERSION}/mysterium_server_linux_arm
### Running
```bash
mysterium_server --help
sudo mysterium_server --config-dir=/etc/mysterium-node --node=123456
```


## Mysterium VPN client (standalone Linux binaries)
### Download
 * https://github.com/MysteriumNetwork/node/releases/download/{VERSION}/mysterium_client_linux_amd64
 * https://github.com/MysteriumNetwork/node/releases/download/{VERSION}/mysterium_client_linux_386
 * https://github.com/MysteriumNetwork/node/releases/download/{VERSION}/mysterium_client_linux_arm
### Running
```bash
mysterium_client --help
sudo mysterium_client --node=123456
```


## Mysterium VPN client (standalone Apple Mac/OSX/Darwin binaries)
 * https://github.com/MysteriumNetwork/node/releases/download/{VERSION}/mysterium_client_osx_amd64
 * https://github.com/MysteriumNetwork/node/releases/download/{VERSION}/mysterium_client_osx_386


## Build from source code
 * https://github.com/MysteriumNetwork/node/archive/{VERSION}.tar.gz
 * https://github.com/MysteriumNetwork/node/archive/{VERSION}.zip
