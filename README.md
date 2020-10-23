# coinpay-api

This project for multi-cryptocurrency integration api.

# construction of project

* Service brokers for each cryptocurrency.
* Main web project for api interface and wallet dashboard ( admin panel + user dashboard )

# Deployment of full nodes and sync with ledgers

- BTC
  
  Download bitcoin core from bitcoin.org
  
  * Please visit https://bitcoin.org/en/download and download Bitcoin Core ( for GUI )
  
  * Please refer to following commandlines ( for Linux terminal )
  
      
    ** Add repository and install bitcoind ** 
    
    sudo apt-get install build-essential
    sudo apt-get install libtool autotools-dev autoconf
    sudo apt-get install libssl-dev
    sudo apt-get install libboost-all-dev
    sudo add-apt-repository ppa:bitcoin/bitcoin
    sudo apt-get update
    sudo apt-get install bitcoind
    mkdir ~/.bitcoin/ && cd ~/.bitcoin/
    nano bitcoin.conf
    
    ** Add config to bitcoin.conf file ** 

    rpcuser=username
    rpcpassword=password
    testnet=1
    rpcport=8332
    rpcallowip=127.0.0.1
    rpcallowip=195.154.11.93
    server=1
