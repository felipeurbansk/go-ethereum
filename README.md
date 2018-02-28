## Go Ethereum

Implementação oficial do protocolo Ethereum feito em Go personalizado para o evento 7Masters da [iMasters](https://imasters.com.br) em 28/02/2018

## Obtendo os executáveis a partir do fonte

Para pré-requisitos e instruções detalhadas para compilação por favor leia as 
[Instruções de instalação](https://github.com/ethereum/go-ethereum/wiki/Building-Ethereum)
na wiki.

Compilar o geth requer o Go (version 1.7 ou superior) e um compilador a C.
Uma vez que você possua as dependências, execute: 

    make geth

ou, para compilar todos coleção de utilitários:

    make all

## Executáveis

O projeto go-ethereum vém com diversos wrappers/executáveis encontrados no diretório `cmd`.

## Para subir uma rede personalizada

Depois de compilar veja detalhes dos parametros a serem utilizados com o `geth` em  
[Comandos Úteis](https://github.com/jeffprestes/go-ethereum/blob/7masters/comandos-uteis.md)
e o arquivo genesis modelo esta neste [endereço](https://github.com/jeffprestes/go-ethereum/blob/7masters/genesis-file-template.json).


## Licença

The go-ethereum library (i.e. all code outside of the `cmd` directory) is licensed under the
[GNU Lesser General Public License v3.0](https://www.gnu.org/licenses/lgpl-3.0.en.html), also
included in our repository in the `COPYING.LESSER` file.

The go-ethereum binaries (i.e. all code inside of the `cmd` directory) is licensed under the
[GNU General Public License v3.0](https://www.gnu.org/licenses/gpl-3.0.en.html), also included
in our repository in the `COPYING` file.
