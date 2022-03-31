# openSeaBot

## Installation
```
git clone https://github.com/ahmed-dev-tech/openSeaBot.git
cd ./openSeaBot
npm install
```

## Usage
You can also run this script by using `node main.js --<args>`

### Arguments
- mnemonic : The mnemonic of the wallet to use. Classic derivation path (trustwallet, metamask,etc)
- network : network to use. Only two options ("rinkeby" for testnet, "mainnet" for etherreum mainnet)
- infura : your infura api key ( https://ethereumico.io/knowledge-base/infura-api-key-guide/)
- buyeraddy : the ethereum address linked to the mnemonic above
- url : The link of the opensea asset you want to buy
- extragas (**optional**) : amount in gwei that will be added to the current gas price for the txn ( txn_gas_price = current_gas_price + extra_gas_price). Default is 0
- startTimeUTC (**optional**): The UTC time at which the asset should be bought ( format hh:mm:ss). Default is immediate buy

### Example for Mainnet
```
node main.js --network="mainnet" --extragas=260 --buyeraddy="wallet address(mainnet)" --infura="cd76ad14df5645bf8fff88c5b87811a9" --url="Opensea Mainnet url" --mnemonic="Metamask's mainnet mnemonics" --startTimeUTC="9:21:30"
```
### Example for testnet
```
node main.js --network="rinkeby" --extragas=260 --buyeraddy="wallet address(testnet)" --infura="cd76ad14df5645bf8fff88c5b87811a9" --url="Opensea testnet url" --mnemonic="Metamask's rinkeby mnemonics" --startTimeUTC="9:21:30"
```
