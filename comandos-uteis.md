# Comandos uteis

## Modelo

### Inicializando uma rede com arquivo Genesis personalizado
geth --datadir "<<caminho para o diretorio onde você vai armazenar os dados do seu blockchain>>" --networkid="<<um numero qualquer para ser ID>>" --identity "<<um nome qualquer para ser uma idenficacao>>" init "<<caminho para o seu arquivo genesis>>/genesis.json"

### Subindo um nó da rede recem criada na sua maquina
geth --datadir "<<caminho para o diretorio onde você vai armazenar os dados do seu blockchain>>" --networkid="<<um numero qualquer para ser ID>>" --ws --wsaddr "<<endereço IP da sua maquina que seja acessível externamente>>" --identity "<<um nome qualquer para ser uma idenficacao>>" --rpc --rpcaddr "<<endereço IP da sua maquina que seja acessível externamente>>" --rpccorsdomain "*" --wsapi "admin,db,eth,debug,miner,net,shh,txpool,personal,web3" --rpcapi "admin,db,eth,debug,miner,net,shh,txpool,personal,web3"

## Exemplos

### Inicializando uma rede com arquivo Genesis personalizado
geth --datadir "/Users/jeffprestes/teste_ethereum_4" --networkid="15397" --identity "jeffcoin" init "/Users/jeffprestes/teste_ethereum_4/genesis.json"

### Subindo um nó da rede recem criada na sua maquina
geth --datadir "/Users/jeffprestes/teste_ethereum_3" --networkid="15397" --ws --wsaddr "127.0.0.1" --identity "jeffcoin" --rpc --rpcaddr "127.0.0.1" --rpccorsdomain "*" --wsapi "admin,db,eth,debug,miner,net,shh,txpool,personal,web3" --rpcapi "admin,db,eth,debug,miner,net,shh,txpool,personal,web3"
