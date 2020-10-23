# coinpay-api

This project for multi-cryptocurrency integration api.

# construction of project

* Service brokers for each cryptocurrency.
* Main web project for api interface and wallet dashboard ( admin panel + user dashboard )

# Deployment of full nodes and sync with ledgers

- BTC ( Bitcoin )
  
  Download bitcoin core from bitcoin.org
  
  * Please visit https://bitcoin.org/en/download and download Bitcoin Core ( for GUI )
  
  * Please refer to following commandlines ( for Linux terminal )
  
      
    ** Add repository and install bitcoind ** 
    
    - sudo apt-get install build-essential
    - sudo apt-get install libtool autotools-dev autoconf
    - sudo apt-get install libssl-dev
    - sudo apt-get install libboost-all-dev
    - sudo add-apt-repository ppa:bitcoin/bitcoin
    - sudo apt-get update
    - sudo apt-get install bitcoind
    - mkdir ~/.bitcoin/ && cd ~/.bitcoin/
    - nano bitcoin.conf
    
    ** Add config to bitcoin.conf file ** 

    - rpcuser=username
    - rpcpassword=password
    - testnet=1
    - rpcport=8332
    - rpcallowip=127.0.0.1
    - rpcallowip=195.154.11.93
    - server=1
   
    ** Start bitcoind ** 

    bitcoind --daemon

    ** Test bitcoind is running and working **

    bitcoin-cli getinfo
    
    & needed at least 320GB for download all blocks and sync ledger

- LTC ( Litecoin )
  
  Download litecoin core 
  
  * Please visit https://litecoin.org/ and download Litecoin Core ( for GUI )
  
  * Please refer to following commandlines ( for Linux terminal )
  
    ** On the Ubuntu Linux console, use the following commands to install the BerkleyDB package **
  
    - add-apt-repository ppa:bitcoin/bitcoin
    - apt-get update
    - apt-get install libdb4.8-dev libdb4.8++-dev
    
    ** Use the following commands to install the required libraries and the required packages **
    
    - apt-get install libboost-all-dev libzmq3-dev libminiupnpc-dev
    - apt-get install curl git build-essential libtool autotools-dev
    - apt-get install automake pkg-config bsdmainutils python3
    - apt-get install software-properties-common libssl-dev libevent-dev
    
    ** Create a directory to the node software and download the Litecoin package **
    
    - mkdir /downloads
    - cd /downloads
    - git clone https://github.com/litecoin-project/litecoin.git
    
    ** Compile and install the Litecoin node software **
    
    - cd litecoin
    - ./autogen.sh
    - ./configure
    - make
    - make install
    
    ** Create a Litecoin configuration file and choose a username and a password **
    
    - mkdir ~/.litecoin
    - vi $HOME/.litecoin/litecoin.conf
    - rpcuser=virtualcoin2018
    - rpcpassword=kamisama123
    
    ** Start the Litecoin node daemon using the following command **
    
    - litecoind -daemon
    
    ** Here is a list of useful commands **
    
    - litecoin-cli getinfo
    - litecoin-cli getblockchaininfo
    - litecoin-cli getnetworkinfo
    - litecoin-cli getwalletinfo
    - litecoin-cli getpeerinfo
    
- XRP ( Ripple )

  Please refer to https://xrpl.org/get-started.html
  
- ETH ( Ethereum )
  
  Download mist brower for ( GUI ) and geth ( go Ethereum )
  
  ** To enable our launchpad repository run **

  - sudo add-apt-repository -y ppa:ethereum/ethereum

  ** Then install the stable version of go-ethereum **

  - sudo apt-get update

  - sudo apt-get install ethereum
