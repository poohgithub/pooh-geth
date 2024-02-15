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

### run node
```
./enode pow el1
```

## Run Local Net

### compile
```
./compile
```

### run node
init은 위의 [Run Testnet](#run-testnet) 참고
```
./enode-config
```