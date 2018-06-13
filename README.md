![CRYPTORIYA](logo.png "Cryptoriya")

# Cryptoriya smart contract

* _Standard_        : [ERC20](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-20.md)
* _[Name](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-20.md#name)_            : Cryptoriya
* _[Ticker](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-20.md#symbol)_          : CIYA
* _[Decimals](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-20.md#decimals)_        : 18
* _Emission_        : Mintable
* _Crowdsales_      : 2
* _Fiat dependency_ : No
* _Tokens locked_   : Yes

## Smart-contracts description

Contract mint bounty and founders tokens after main sale stage finished. 
Crowdsale contracts have special function to retrieve transferred in errors tokens.
Also crowdsale contracts have special function to direct mint tokens in wei value (featue implemneted to support external pay gateway).

### Contracts contains
1. _CryptoriyaToken_ - Token contract
2. _Presale_ - Presale contract
3. _Mainsale_ - ICO contract
4. _Configurator_ - contract with main configuration for production

### How to manage contract
To start working with contract you should follow next steps:
1. Compile it in Remix with enamble optimization flag and compiler 0.4.18
2. Deploy bytecode with MyEtherWallet. Gas 5100000 (actually 5073514).
3. Call 'deploy' function on addres from (3). Gas 4000000 (actually 3979551). 

Contract manager must call finishMinting after each crowdsale milestone!
To support external mint service manager should specify address by calling _setDirectMintAgent_. After that specified address can direct mint CIYA tokens by calling _directMint_.

### How to invest
To purchase tokens investor should send ETH (more than minimum 0.1 ETH) to corresponding crowdsale contract.
Recommended GAS: 250000, GAS PRICE - 21 Gwei.

### Wallets with ERC20 support
1. MyEtherWallet - https://www.myetherwallet.com/
2. Parity 
3. Mist/Ethereum wallet

EXODUS not support ERC20, but have way to export key into MyEtherWallet - http://support.exodus.io/article/128-how-do-i-receive-unsupported-erc20-tokens

Investor must not use other wallets, coinmarkets or stocks. Can lose money.

## Token counts

Maximum tokens can mint - 100 000 000 CIYA 
* on all crowdsales : 70% or 70 000 000 CIYA 
* on presale : 15% or 15 000 000 CIYA 
* on mainsale : 55% or 55 000 000 CIYA
* to founders : 14% or 14 000 000 CIYA
* to bounty : 5% or 5 000 000 CIYA
* to advisors : 7% or 7 000 000 CIYA
* to partner : 4% or 4 000 000 CIYA


### Links
1. _Token_ - https://etherscan.io/token/0xf75fbfa2f681860b9a6d19fc3ff3d34cb322e2d6
2. _Presale_ - https://etherscan.io/address/0x937ee62efc6a3b3f498ef59bca5e9f59cf4166ca
3. _Mainsale_ - https://etherscan.io/address/0xdece7451ebee92bc6a4b97f358bb5f6e87ee102d

### Crowdsale stages

#### Presale
* _Hardcap_                    : 3500 ETH
* _Price_                      : 4000 CIYA
* _Period_                     : 35 days
* _Start_                      : 15.05.2018 09:00 GMT
* _Master wallet_              : 0x45f28cbf4d54e08fe184f0ecb79b7f3ca43528be 
* _Slave wallet_               : 0x5e7b27d4d82ea95140b9d7031d140513526a6661
* _Master wallet percent_      : 50%
* _Slave wallet percent_       : 50%
* _Contract owner_             : 0x9e54a49c37854006e3be246d978f5c20e1dbe8a4

#### ICO
* _Hardcap_                    : 25 000 ETH
* _Period_                     : 45 days
* _Start_                      : 01.07.2018 09:00 GMT
* _Master wallet_              : 0x45f28cbf4d54e08fe184f0ecb79b7f3ca43528be
* _Slave wallet_               : 0x5e7b27d4d82ea95140b9d7031d140513526a6661
* _Master wallet percent_      : 50%
* _Slave wallet percent_       : 50%
* _Contract owner_             : 0x9e54a49c37854006e3be246d978f5c20e1dbe8a4

