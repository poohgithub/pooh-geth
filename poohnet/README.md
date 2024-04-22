## Overview
### Network ID
The network id is only set in these files.
- Mainnet: 12300 (set in ./poohnet/config/el/genesis.json)
- Mainnet for merge: 12300 (set in ./poohnet/config/el/genesis_merge.json)
- Testnet: 12301 (set in ./poohnet/config/el/genesis_testnet.json)
- Localnet: 12302 (set in ./poohnet/config/el/genesis_local.json)

## Run Testnet

### stop & remote docker
```
docker ps
CONTAINER ID   IMAGE                        COMMAND                  CREATED       STATUS          PORTS                                                                                                                                                                                          NAMES
2a9587c59d4c   linked0/poohnet-pow:latest   "geth --datadir=/dat…"   7 weeks ago   Up 32 minutes   0.0.0.0:6060->6060/tcp, :::6060->6060/tcp, 0.0.0.0:8545->8545/tcp, :::8545->8545/tcp, 0.0.0.0:30303->30303/tcp, :::30303->30303/tcp, 8546/tcp, 0.0.0.0:30303->30303/udp, :::30303->30303/udp   pow-node```
```

CONTAINER ID를 확인하고 중단 시킴
```
docker stop 2a9587c59d4c
```

CONTAINER ID를 확인하고 제거하기 
```
docker rm 2a9587c59d4c
```

### go to poohnet folder
```
cd poohnet
```

### init node
노드가 하나인 테스트넷을 실행시킬때
```
./init testnet 1
```

`Password:` 프롬프트에 대해서는 로컬시스템 사용자 계정 암호를 입력

### run node
```
./enode testnet enode1
```

## Run with local binary
다음은 로컬에서 빌드한 바이너리를 이용해서 노드를 띄우는 경우

### compile
```
./compile
```

### init node
`poohnet` 폴더로 이용
```
cd poohnet
```
노드가 하나인 테스트넷을 실행시킬때
```
./init testnet 1
```

### run node
init은 위의 [Run Testnet](#run-testnet) 참고
```
./enode-cmd
```