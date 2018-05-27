# Comandos uteis

## Modelo

### Inicializando uma rede com arquivo Genesis personalizado
geth --datadir "<<caminho para o diretorio onde você vai armazenar os dados do seu blockchain>>" --networkid="<<um numero qualquer para ser ID>>" --identity "<<um nome qualquer para ser uma idenficacao>>" init "<<caminho para o seu arquivo genesis>>/genesis.json"

### Subindo um nó da rede recem criada na sua maquina
geth --datadir "<<caminho para o diretorio onde você vai armazenar os dados do seu blockchain>>" --networkid="<<um numero qualquer para ser ID>>" --ws --wsaddr "<<endereço IP da sua maquina que seja acessível externamente>>" --identity "<<um nome qualquer para ser uma idenficacao>>" --rpc --rpcaddr "<<endereço IP da sua maquina que seja acessível externamente>>" --rpccorsdomain "*" --wsapi "admin,db,eth,debug,miner,net,shh,txpool,personal,web3" --rpcapi "admin,db,eth,debug,miner,net,shh,txpool,personal,web3"

## Exemplos

### Inicializando uma rede com arquivo Genesis personalizado
geth --datadir "/Users/jeffprestes/ethereum7masters" --networkid="1337" --identity "jeffcoin" init "/Users/jeffprestes/ethereum7masters/genesis.json"

### Subindo um nó da rede recem criada na sua maquina
geth --datadir "/Users/jeffprestes/ethereum7masters" --networkid="1337" --ws --wsaddr "127.0.0.1" --identity "jeffcoin" --rpc --rpcaddr "127.0.0.1" --rpccorsdomain "*" --wsapi "admin,db,eth,debug,miner,net,shh,txpool,personal,web3" --rpcapi "admin,db,eth,debug,miner,net,shh,txpool,personal,web3" --ipcpath "/Users/jeffprestes/Library/Ethereum/geth.ipc" --vmdebug 
console


### Subindo um nó da rede recem criada na sua maquina com a conta principal desbloqueada
geth --datadir "/Users/jeffprestes/ethereum7masters" --networkid="1337" --ws --wsaddr "127.0.0.1" --identity "jeffcoin" --rpc --rpcaddr "127.0.0.1" --rpccorsdomain "*" --wsapi "admin,db,eth,debug,miner,net,shh,txpool,personal,web3" --rpcapi "admin,db,eth,debug,miner,net,shh,txpool,personal,web3" --ipcpath "/Users/jeffprestes/Library/Ethereum/geth.ipc" --vmdebug --unlock "0x3096dc394a540d8f856c6840f84fe1d511c05d30" --password "/Users/jeffprestes/ethereum7masters/0x3096dc-senha.txt"


### Conectando ao nó via console
geth attach ipc:///Users/jeffprestes/Library/Ethereum/geth.ipc

### Subindo um nó em segundo plano no Linux
nohup geth --ws --wsaddr "159.65.43.266" --rpc --rpcaddr "159.65.43.266" --rpccorsdomain "*" --wsapi "admin,db,eth,debug,miner,net,shh,txpool,personal,web3" --rpcapi "admin,db,eth,debug,miner,net,shh,txpool,personal,web3" --cache=2048 --vmdebug 2> geth.log &

nohup geth --rpc --rpcaddr "159.65.43.266" --rpcapi "eth,web3" --cache=2048 --vmdebug 2> geth.log &

nohup geth --cache=2048 2> geth.log &

nohup geth --rpc --rpcaddr "127.0.0.1" --rpcport "8946" --rpcapi "eth,web3,personal" --cache=2048 2> geth.log &