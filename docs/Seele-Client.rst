Seele Client
============

Seele comes with a client which has support for all management APIs
described here.

Command Line Options
--------------------

Full Node Client
~~~~~~~~~~~~~~~~

::

   client -h
   NAME:
      client - interact with a full node process

   USAGE:
      client [global options] command [command options] [arguments...]

   AUTHOR:
      seeleteam <dev@seelenet.com>

   COMMANDS:
        call              call contract
        deckeyfile        Decrypt key file
        domain            system domain name commands
        dumpheap          dump heap for profiling, return the file path
        getbalance        get balance info
        getblock          get block by height or hash
        getblockheight    get block height
        getblocktxcount   get block transaction count by block height or block hash
        getdebtbyhash     get debt by debt hash
        getdebts          get pending debts
        getinfo           get node info
        getlogs           get logs
        getnonce          get account nonce
        getpendingtxs     get pending transactions
        getreceipt        get receipt by transaction hash
        getshardnum       get account shard number
        gettxbyhash       get transaction by transaction hash
        gettxinblock      get transaction by block height or block hash with index of the transaction in the block
        gettxpoolcontent  get transaction pool contents
        gettxpoolcount    get transaction pool transaction count
        htlc              Hash time lock contract commands
        key               generate key with or without shard number
        miner             miner commands
        p2p               p2p commands
        payload           generate the payload according to the abi file and method name and args
        savekey           save private key to a keystore file
        sendtx            send transaction to node
        sign              generate a signed transaction and print it out
        subchain          system sub chain commands
        help, h           Shows a list of commands or help for one command

   GLOBAL OPTIONS:
      --help, -h  show help

::

   client call -h
   NAME:
      client call - call contract

   USAGE:
      client call [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --to value                 to address
      --payload value            transaction payload info
      --height value             block height (default: -1)

::

   client deckeyfile -h
   NAME:
      client deckeyfile - Decrypt key file

   USAGE:
      client deckeyfile [command options] [arguments...]

   OPTIONS:
      --file value  key store file name (default: ".keystore")

::

   client domain -h
   NAME:
      client domain - system domain name commands

   USAGE:
      client domain command [command options] [arguments...]

   COMMANDS:
        owner     get the domain name owner
        register  register a domain name

   OPTIONS:
      --help, -h  show help

::

   client domain owner -h
   NAME:
      client domain owner - get the domain name owner

   USAGE:
      client domain owner [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --from value               key file of the sender
      --price value              transaction gas price in Fan (default: "10")
      --gas value                maximum gas for transaction (default: 200000)
      --name value               domain or subchain name
      --nonce value              transaction nonce (default: 0)

::

   client domain register -h
   NAME:
      client domain register - register a domain name

   USAGE:
      client domain register [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --from value               key file of the sender
      --price value              transaction gas price in Fan (default: "10")
      --gas value                maximum gas for transaction (default: 200000)
      --name value               domain or subchain name
      --nonce value              transaction nonce (default: 0)

::

   client dumpheap -h
   NAME:
      client dumpheap - dump heap for profiling, return the file path

   USAGE:
      client dumpheap [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --file value               heap dump file name, default heap.dump (default: "heap.dump")
      --gc                       GC before heap dump, default false

::

   client getbalance -h
   NAME:
      client getbalance - get balance info

   USAGE:
      client getbalance [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --account value            account address

::

   client getblock -h
   NAME:
      client getblock - get block by height or hash

   USAGE:
      client getblock [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --hash value               hash value in hex
      --height value             block height (default: -1)
      --fulltx, -f               whether print full transaction info

::

   client getblockheight -h
   NAME:
      client getblockheight - get block height

   USAGE:
      client getblockheight [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")

::

   client getblocktxcount -h
   NAME:
      client getblocktxcount - get block transaction count by block height or block hash

   USAGE:
      client getblocktxcount [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --hash value               hash value in hex
      --height value             block height (default: -1)

::

   client getdebtbyhash -h
   NAME:
      client getdebtbyhash - get debt by debt hash

   USAGE:
      client getdebtbyhash [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --hash value               hash value in hex

::

   client getdebts -h
   NAME:
      client getdebts - get pending debts

   USAGE:
      client getdebts [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")

::

   client getinfo -h
   NAME:
      client getinfo - get node info

   USAGE:
      client getinfo [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")

::

   client getlogs -h
   NAME:
      client getlogs - get logs

   USAGE:
      client getlogs [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --height value             block height (default: -1)
      --contract value           contract code in hex
      --topic value              topic

::

   client getnonce -h
   NAME:
      client getnonce - get account nonce

   USAGE:
      client getnonce [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --account value            account address

::

   client getpendingtxs -h
   NAME:
      client getpendingtxs - get pending transactions

   USAGE:
      client getpendingtxs [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")

::

   client getreceipt -h
   NAME:
      client getreceipt - get receipt by transaction hash

   USAGE:
      client getreceipt [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --hash value               hash value in hex
      --abi value                the abi file of contract

::

   client getshardnum -h
   NAME:
      client getshardnum - get account shard number

   USAGE:
      client getshardnum [command options] [arguments...]

   OPTIONS:
      --account value     account address
      --privatekey value  private key for account

::

   client gettxbyhash -h
   NAME:
      client gettxbyhash - get transaction by transaction hash

   USAGE:
      client gettxbyhash [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --hash value               hash value in hex

::

   client gettxinblock -h
   NAME:
      client gettxinblock - get transaction by block height or block hash with index of the transaction in the block

   USAGE:
      client gettxinblock [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --hash value               hash value in hex
      --height value             block height (default: -1)
      --index value              transaction index, start with 0 (default: 0)

::

   client gettxpoolcontent -h
   NAME:
      client gettxpoolcontent - get transaction pool contents

   USAGE:
      client gettxpoolcontent [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")

::

   client gettxpoolcount -h
   NAME:
      client gettxpoolcount - get transaction pool transaction count

   USAGE:
      client gettxpoolcount [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")

::

   client htlc -h
   NAME:
      client htlc - Hash time lock contract commands

   USAGE:
      client htlc command [command options] [arguments...]

   COMMANDS:
        create    create HTLC
        decode    decode HTLC contract information
        get       get HTLC information
        key       generate preimage key and key hash
        refund    refund from HTLC
        time      generate unix timestamp
        withdraw  withdraw from HTLC

   OPTIONS:
      --help, -h  show help

::

   client htlc create -h
   NAME:
      client htlc create - create HTLC

   USAGE:
      client htlc create [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --from value               key file of the sender
      --to value                 to address
      --amount value             amount value, unit is fan
      --price value              transaction gas price in Fan (default: "10")
      --gas value                maximum gas for transaction (default: 200000)
      --nonce value              transaction nonce (default: 0)
      --hash value               hash value in hex
      --time value               time lock in the HTLC (default: 0)

::

   client htlc decode -h
   NAME:
      client htlc decode - decode HTLC contract information

   USAGE:
      client htlc decode [command options] [arguments...]

   OPTIONS:
      --payload value  transaction payload info

::

   client htlc get -h
   NAME:
      client htlc get - get HTLC information

   USAGE:
      client htlc get [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --from value               key file of the sender
      --hash value               hash value in hex

::

   client htlc key -h
   NAME:
      client htlc key - generate preimage key and key hash

   USAGE:
      client htlc key [arguments...]

::

   client htlc refund -h
   NAME:
      client htlc refund - refund from HTLC

   USAGE:
      client htlc refund [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --from value               key file of the sender
      --price value              transaction gas price in Fan (default: "10")
      --gas value                maximum gas for transaction (default: 200000)
      --nonce value              transaction nonce (default: 0)
      --hash value               hash value in hex

::

   client htlc time -h
   NAME:
      client htlc time - generate unix timestamp

   USAGE:
      client htlc time [command options] [arguments...]

   OPTIONS:
      --time value  time lock in the HTLC (default: 0)

::

   client htlc withdraw -h
   NAME:
      client htlc withdraw - withdraw from HTLC

   USAGE:
      client htlc withdraw [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --from value               key file of the sender
      --price value              transaction gas price in Fan (default: "10")
      --gas value                maximum gas for transaction (default: 200000)
      --nonce value              transaction nonce (default: 0)
      --hash value               hash value in hex
      --preimage value           preimage of hash in the HTLC

::

   client key -h
   NAME:
      client key - generate key with or without shard number

   USAGE:
      client key [command options] [arguments...]

   OPTIONS:
      --shard value  shard number (default: 0)

::

   client miner -h
   NAME:
      client miner - miner commands

   USAGE:
      client miner command [command options] [arguments...]

   COMMANDS:
        getcoinbase    get miner coinbase
        getengineinfo  get miner engine information
        setcoinbase    set miner coinbase
        setthreads     set miner thread number
        start          start miner
        status         get miner status
        stop           stop miner

   OPTIONS:
      --help, -h  show help

::

   client miner getcoinbase -h
   NAME:
      client miner getcoinbase - get miner coinbase

   USAGE:
      client miner getcoinbase [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")

::

   client miner getengineinfo -h
   NAME:
      client miner getengineinfo - get miner engine information

   USAGE:
      client miner getengineinfo [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")

::

   client miner setcoinbase -h
   NAME:
      client miner setcoinbase - set miner coinbase

   USAGE:
      client miner setcoinbase [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --coinbase value           miner coinbase in hex

::

   client miner setthreads -h
   NAME:
      client miner setthreads - set miner thread number

   USAGE:
      client miner setthreads [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --threads value            miner threads (default: 0)

::

   client miner start -h
   NAME:
      client miner start - start miner

   USAGE:
      client miner start [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --threads value            miner threads (default: 0)

::

   client miner status -h
   NAME:
      client miner status - get miner status

   USAGE:
      client miner status [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")

::

   client miner stop -h
   NAME:
      client miner stop - stop miner

   USAGE:
      client miner stop [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")

::

   client p2p -h
   NAME:
      client p2p - p2p commands

   USAGE:
      client p2p command [command options] [arguments...]

   COMMANDS:
        netversion       get current net version
        networkid        get current network id
        peers            get p2p peer connections
        peersinfo        get p2p peers information
        protocolversion  get seele protocol version

   OPTIONS:
      --help, -h  show help

::

   client p2p netversion -h
   NAME:
      client p2p netversion - get current net version

   USAGE:
      client p2p netversion [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")

::

   client p2p networkid -h
   NAME:
      client p2p networkid - get current network id

   USAGE:
      client p2p networkid [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")

::

   client p2p peers -h
   NAME:
      client p2p peers - get p2p peer connections

   USAGE:
      client p2p peers [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")

::

   client p2p peersinfo -h
   NAME:
      client p2p peersinfo - get p2p peers information

   USAGE:
      client p2p peersinfo [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")

::

   client p2p protocolversion -h
   NAME:
      client p2p protocolversion - get seele protocol version

   USAGE:
      client p2p protocolversion [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")

::

   client payload -h
   NAME:
      client payload - generate the payload according to the abi file and method name and args

   USAGE:
      client payload [command options] [arguments...]

   OPTIONS:
      --abi value     the abi file of contract
      --method value  the method name of contract
      --args value    the parameters of contract method

::

   client savekey -h
   NAME:
      client savekey - save private key to a keystore file

   USAGE:
      client savekey [command options] [arguments...]

   OPTIONS:
      --privatekey value  private key for account
      --file value        key store file name (default: ".keystore")

::

   client sendtx -h
   NAME:
      client sendtx - send transaction to node

   USAGE:
      client sendtx [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --from value               key file of the sender
      --to value                 to address
      --amount value             amount value, unit is fan
      --price value              transaction gas price in Fan (default: "10")
      --gas value                maximum gas for transaction (default: 200000)
      --payload value            transaction payload info
      --nonce value              transaction nonce (default: 0)

::

   client sign -h
   NAME:
      client sign - generate a signed transaction and print it out

   USAGE:
      client sign [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --privatekey value         private key for account
      --to value                 to address
      --amount value             amount value, unit is fan
      --price value              transaction gas price in Fan (default: "10")
      --gas value                maximum gas for transaction (default: 200000)
      --payload value            transaction payload info
      --nonce value              transaction nonce (default: 0)

::

   client subchain -h
   NAME:
      client subchain - system sub chain commands

   USAGE:
      client subchain command [command options] [arguments...]

   COMMANDS:
        config    generate sub chain config file
        query     query sub chain
        register  register a sub chain

   OPTIONS:
      --help, -h  show help

::

   client subchain config -h
   NAME:
      client subchain config - generate sub chain config file

   USAGE:
      client subchain config [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --coinbase value           miner coinbase in hex
      --privatekey value         private key for account
      --name value               domain or subchain name
      --output value, -o value   subchain config file path
      --shard value              shard number (default: 0)
      --node value, -n value     subchain static node, for example:-n address:port -n address:prot

::

   client subchain query -h
   NAME:
      client subchain query - query sub chain

   USAGE:
      client subchain query [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --from value               key file of the sender
      --price value              transaction gas price in Fan (default: "10")
      --gas value                maximum gas for transaction (default: 200000)
      --nonce value              transaction nonce (default: 0)
      --name value               domain or subchain name

::

   client subchain register -h
   NAME:
      client subchain register - register a sub chain

   USAGE:
      client subchain register [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --from value               key file of the sender
      --price value              transaction gas price in Fan (default: "10")
      --gas value                maximum gas for transaction (default: 200000)
      --nonce value              transaction nonce (default: 0)
      --file value               subchain json file path

Light Node Client
~~~~~~~~~~~~~~~~~

::

   light -h
   NAME:
      light - interact with a light node process

   USAGE:
      light [global options] command [command options] [arguments...]

   AUTHOR:
      seeleteam <dev@seelenet.com>

   COMMANDS:
        deckeyfile        Decrypt key file
        getbalance        get balance info
        getblock          get block by height or hash
        getblockheight    get block height
        getblocktxcount   get block transaction count by block height or block hash
        getnonce          get account nonce
        getpendingtxs     get pending transactions
        getreceipt        get receipt by transaction hash
        getshardnum       get account shard number
        gettxbyhash       get transaction by transaction hash
        gettxinblock      get transaction by block height or block hash with index of the transaction in the block
        gettxpoolcontent  get transaction pool contents
        gettxpoolcount    get transaction pool transaction count
        key               generate key with or without shard number
        p2p               p2p commands
        payload           generate the payload according to the abi file and method name and args
        savekey           save private key to a keystore file
        sendtx            send transaction to node
        sign              generate a signed transaction and print it out
        help, h           Shows a list of commands or help for one command

   GLOBAL OPTIONS:
      --help, -h  show help

::

   light deckeyfile -h
   NAME:
      light deckeyfile - Decrypt key file

   USAGE:
      light deckeyfile [command options] [arguments...]

   OPTIONS:
      --file value  key store file name (default: ".keystore")

::

   light getbalance -h
   NAME:
      light getbalance - get balance info

   USAGE:
      light getbalance [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --account value            account address

::

   light getblock -h
   NAME:
      light getblock - get block by height or hash

   USAGE:
      light getblock [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --hash value               hash value in hex
      --height value             block height (default: -1)
      --fulltx, -f               whether print full transaction info

::

   light getblockheight -h
   NAME:
      light getblockheight - get block height

   USAGE:
      light getblockheight [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")

::

   light getblocktxcount -h
   NAME:
      light getblocktxcount - get block transaction count by block height or block hash

   USAGE:
      light getblocktxcount [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --hash value               hash value in hex
      --height value             block height (default: -1)

::

   light getnonce -h
   NAME:
      light getnonce - get account nonce

   USAGE:
      light getnonce [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --account value            account address

::

   light getpendingtxs -h
   NAME:
      light getpendingtxs - get pending transactions

   USAGE:
      light getpendingtxs [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")

::

   light getreceipt -h
   NAME:
      light getreceipt - get receipt by transaction hash

   USAGE:
      light getreceipt [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --hash value               hash value in hex
      --abi value                the abi file of contract

::

   light getshardnum -h
   NAME:
      light getshardnum - get account shard number

   USAGE:
      light getshardnum [command options] [arguments...]

   OPTIONS:
      --account value     account address
      --privatekey value  private key for account

::

   light gettxbyhash -h
   NAME:
      light gettxbyhash - get transaction by transaction hash

   USAGE:
      light gettxbyhash [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --hash value               hash value in hex

::

   light gettxinblock -h
   NAME:
      light gettxinblock - get transaction by block height or block hash with index of the transaction in the block

   USAGE:
      light gettxinblock [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --hash value               hash value in hex
      --height value             block height (default: -1)
      --index value              transaction index, start with 0 (default: 0)

::

   light gettxpoolcontent -h
   NAME:
      light gettxpoolcontent - get transaction pool contents

   USAGE:
      light gettxpoolcontent [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")

::

   light gettxpoolcount -h
   NAME:
      light gettxpoolcount - get transaction pool transaction count

   USAGE:
      light gettxpoolcount [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")

::

   light key -h
   NAME:
      light key - generate key with or without shard number

   USAGE:
      light key [command options] [arguments...]

   OPTIONS:
      --shard value  shard number (default: 0)

::

   light p2p -h
   NAME:
      light p2p - p2p commands

   USAGE:
      light p2p command [command options] [arguments...]

   COMMANDS:
        netversion       get current net version
        networkid        get current network id
        peers            get p2p peer connections
        peersinfo        get p2p peers information
        protocolversion  get seele protocol version

   OPTIONS:
      --help, -h  show help

::

   light p2p netversion -h
   NAME:
      light p2p netversion - get current net version

   USAGE:
      light p2p netversion [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")

::

   light p2p networkid -h
   NAME:
      light p2p networkid - get current network id

   USAGE:
      light p2p networkid [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")

::

   light p2p peers -h
   NAME:
      light p2p peers - get p2p peer connections

   USAGE:
      light p2p peers [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")

::

   light p2p peersinfo -h
   NAME:
      light p2p peersinfo - get p2p peers information

   USAGE:
      light p2p peersinfo [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")

::

   light p2p protocolversion -h
   NAME:
      light p2p protocolversion - get seele protocol version

   USAGE:
      light p2p protocolversion [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")

::

   light payload -h
   NAME:
      light payload - generate the payload according to the abi file and method name and args

   USAGE:
      light payload [command options] [arguments...]

   OPTIONS:
      --abi value     the abi file of contract
      --method value  the method name of contract
      --args value    the parameters of contract method

::

   light savekey -h
   NAME:
      light savekey - save private key to a keystore file

   USAGE:
      light savekey [command options] [arguments...]

   OPTIONS:
      --privatekey value  private key for account
      --file value        key store file name (default: ".keystore")

::

   light sendtx -h
   NAME:
      light sendtx - send transaction to node

   USAGE:
      light sendtx [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --from value               key file of the sender
      --to value                 to address
      --amount value             amount value, unit is fan
      --price value              transaction gas price in Fan (default: "10")
      --gas value                maximum gas for transaction (default: 200000)
      --payload value            transaction payload info
      --nonce value              transaction nonce (default: 0)

::

   light sign -h
   NAME:
      light sign - generate a signed transaction and print it out

   USAGE:
      light sign [command options] [arguments...]

   OPTIONS:
      --address value, -a value  address for client to request (default: "127.0.0.1:8027")
      --privatekey value         private key for account
      --to value                 to address
      --amount value             amount value, unit is fan
      --price value              transaction gas price in Fan (default: "10")
      --gas value                maximum gas for transaction (default: 200000)
      --payload value            transaction payload info
      --nonce value              transaction nonce (default: 0)

JSON-RPC Support
----------------

+--------------+------------+
| Type         | Supported? |
+==============+============+
| JSON-RPC 1.0 | ✓          |
+--------------+------------+
| JSON-RPC 2.0 | ✓          |
+--------------+------------+

JSON-RPC Port
-------------

Default port:

+--------+-------------+----------------+
| Client | Type        | Address        |
+========+=============+================+
| Go     | jsonrpc-2.0 | localhost:8027 |
+--------+-------------+----------------+

Client Command List
-------------------

+--------------------------------------------------------------+------+-------+
| Command                                                      | Full | Light |
+==============================================================+======+=======+
| `GetInfo <#getinfo>`__                                       | ✓    |       |
+--------------------------------------------------------------+------+-------+
| `GetBalance <#getbalance>`__                                 | ✓    | ✓     |
+--------------------------------------------------------------+------+-------+
| `AddTx <#addtx>`__                                           | ✓    | ✓     |
+--------------------------------------------------------------+------+-------+
| `GetAccountNonce <#getaccountnonce>`__                       | ✓    | ✓     |
+--------------------------------------------------------------+------+-------+
| `GetBlockHeight <#getblockheight>`__                         | ✓    | ✓     |
+--------------------------------------------------------------+------+-------+
| `GetBlock <#getblock>`__                                     | ✓    | ✓     |
+--------------------------------------------------------------+------+-------+
| `SaveKey <#savekey>`__                                       | ✓    | ✓     |
+--------------------------------------------------------------+------+-------+
| `GetAccountShardNum <#getaccountshardnum>`__                 | ✓    | ✓     |
+--------------------------------------------------------------+------+-------+
| `Call <#call>`__                                             | ✓    |       |
+--------------------------------------------------------------+------+-------+
| GetLogs (Being Written)                                      | ✓    |       |
+--------------------------------------------------------------+------+-------+
| `GetBlockTransactionCount <#getblocktransactioncount>`__     | ✓    | ✓     |
+--------------------------------------------------------------+------+-------+
| `GetTransactionByBlockIndex <#gettransactionbyblockindex>`__ | ✓    | ✓     |
+--------------------------------------------------------------+------+-------+
| `GetTransactionByHash <#gettransactionbyhash>`__             | ✓    | ✓     |
+--------------------------------------------------------------+------+-------+
| `GetReceiptByTxHash <#getreceiptbytxhash>`__                 | ✓    | ✓     |
+--------------------------------------------------------------+------+-------+
| `GetDebtByHash <#getdebtbyhash>`__                           | ✓    |       |
+--------------------------------------------------------------+------+-------+
| `GetPeersInfo <#getpeersinfo>`__                             | ✓    | ✓     |
+--------------------------------------------------------------+------+-------+
| `GetPeerCount <#getpeercount>`__                             | ✓    | ✓     |
+--------------------------------------------------------------+------+-------+
| `GetNetworkVersion <#getnetworkversion>`__                   | ✓    | ✓     |
+--------------------------------------------------------------+------+-------+
| `GetProtocolVersion <#getprotocolversion>`__                 | ✓    | ✓     |
+--------------------------------------------------------------+------+-------+
| `GetNetworkID <#getnetworkid>`__                             | ✓    | ✓     |
+--------------------------------------------------------------+------+-------+
| `Miner Start <#miner-start>`__                               | ✓    |       |
+--------------------------------------------------------------+------+-------+
| `Miner Stop <#miner-stop>`__                                 | ✓    |       |
+--------------------------------------------------------------+------+-------+
| `Miner Status <#miner-status>`__                             | ✓    |       |
+--------------------------------------------------------------+------+-------+
| `Miner GetCoinbase <#miner-getcoinbase>`__                   | ✓    |       |
+--------------------------------------------------------------+------+-------+
| `Miner SetThreads <#miner-setthreads>`__                     | ✓    |       |
+--------------------------------------------------------------+------+-------+
| `Miner SetCoinbase <#miner-setcoinbase>`__                   | ✓    |       |
+--------------------------------------------------------------+------+-------+
| `Miner GetEngineInfo <#miner-getengineinfo>`__               | ✓    |       |
+--------------------------------------------------------------+------+-------+
| `GetTxPoolContent <#gettxpoolcontent>`__                     | ✓    | ✓     |
+--------------------------------------------------------------+------+-------+
| `GetTxPoolTxCount <#gettxpooltxcount>`__                     | ✓    | ✓     |
+--------------------------------------------------------------+------+-------+
| `GetPendingTransactions <#getpendingtransactions>`__         | ✓    | ✓     |
+--------------------------------------------------------------+------+-------+
| `GetPendingDebts <#getpendingdebts>`__                       | ✓    |       |
+--------------------------------------------------------------+------+-------+
| `DumpHeap <#dumpheap>`__                                     | ✓    |       |
+--------------------------------------------------------------+------+-------+
| `Key <#key>`__                                               | ✓    | ✓     |
+--------------------------------------------------------------+------+-------+
| `Sign <#sign>`__                                             | ✓    | ✓     |
+--------------------------------------------------------------+------+-------+
| `GeneratePayload <#generatepayload>`__                       | ✓    | ✓     |
+--------------------------------------------------------------+------+-------+
| `CreateHTLC <#createhtlc>`__                                 | ✓    |       |
+--------------------------------------------------------------+------+-------+
| `DecodeHTLC <#decodehtlc>`__                                 | ✓    |       |
+--------------------------------------------------------------+------+-------+
| `GetHTLC <#gethtlc>`__                                       | ✓    |       |
+--------------------------------------------------------------+------+-------+
| `GenerateHTLCKey <#generatehtlckey>`__                       | ✓    |       |
+--------------------------------------------------------------+------+-------+
| `RefundFromHTLC <#refundfromhtlc>`__                         | ✓    |       |
+--------------------------------------------------------------+------+-------+
| `GenerateHTLCStamptime <#generatehtlcstamptime>`__           | ✓    |       |
+--------------------------------------------------------------+------+-------+
| `WithdrawFromHTLC <#withdrawfromhtlc>`__                     | ✓    |       |
+--------------------------------------------------------------+------+-------+
| `RegisterDomainName <#registerdomainname>`__                 | ✓    |       |
+--------------------------------------------------------------+------+-------+
| `GetDomainNameOwner <#getdomainnameowner>`__                 | ✓    |       |
+--------------------------------------------------------------+------+-------+
| GenSubChainCfgFile (Being Written)                           | ✓    |       |
+--------------------------------------------------------------+------+-------+
| QuerySubChain (Being Written)                                | ✓    |       |
+--------------------------------------------------------------+------+-------+
| RegisterSubChain (Being Written)                             | ✓    |       |
+--------------------------------------------------------------+------+-------+

GetInfo
~~~~~~~

This method returns node information.

+---------+-------------------------------------+
| Type    | Template                            |
+=========+=====================================+
| Console | ``client getinfo -a <rpc address>`` |
+---------+-------------------------------------+

Parameters
^^^^^^^^^^

-  ``address, a``:``string`` - address for client to request (default:
   “127.0.0.1:8027”)

Returns
^^^^^^^

-  ``Coinbase``:``string`` - node address
-  ``CurrentBlockHeight``:``uint64`` - current block height
-  ``HeaderHash``:``string`` - block hash
-  ``MinerStatus``:``string`` - miner status
-  ``Shard``:``uint64`` - shard number

Example
^^^^^^^

.. code:: js

   // Request
   client getinfo

   // Result
   {
       "Coinbase": "0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21",
       "CurrentBlockHeight": 1697,
       "HeaderHash": "0x0000008ad39a1f7c31f3aa730210170b95129ba9c3f15b2cc8fa3ec0f92015b6",
       "MinerStatus": "Running",
       "Shard": 1
   }

--------------

GetBalance
~~~~~~~~~~

This method returns the account balance. If the account flag is null,
the node address balance is returned.

+-----------------------------------+-----------------------------------+
| Type                              | Template                          |
+===================================+===================================+
| Console                           | ``client getbalance --account 0x< |
|                                   | public address> -a <rpc address>` |
|                                   | `                                 |
+-----------------------------------+-----------------------------------+

.. _parameters-1:

Parameters
^^^^^^^^^^

-  ``address, a``:``string`` - address for client to request (default:
   “127.0.0.1:8027”)
-  ``account``:``string`` - wallet address

.. _returns-1:

Returns
^^^^^^^

-  ``Account``:``string`` - account
-  ``Balance``:``big.Int`` - account balance

.. _example-1:

Example
^^^^^^^

.. code:: js

   // Request
   client getbalance --account 0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21

   // Result
   {
       "Account": "0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21",
       "Balance": 261899990000
   }

--------------

AddTx
~~~~~

This method submits a transaction to the node.

+-----------------------------------+-----------------------------------+
| Type                              | Template                          |
+===================================+===================================+
| Console                           | ``client sendtx --amount 10000 -- |
|                                   | fee 1 --from keyfile --to <string |
|                                   | > -a <rpc address>``              |
+-----------------------------------+-----------------------------------+

.. _parameters-2:

Parameters
^^^^^^^^^^

-  ``address, a``:``string`` - address for client to request (default:
   “127.0.0.1:8027”)
-  ``from``:``string`` - transaction ‘from’ address
-  ``to``:``string`` - transaction ‘to’ address
-  ``amount``:``uint64`` - transaction amount
-  ``price``:``uint64`` - transaction gas price in Fan (default: “10”)
-  ``gas``:``uint64`` - maximum gas for transaction (default: 200000)
-  ``payload``:``string`` - transaction payload
-  ``nonce``:``int`` - transaction nonce

.. _returns-2:

Returns
^^^^^^^

-  ``Hash``:``string`` - transaction hash
-  ``From``:``string`` - transaction ‘from’ address
-  ``To``:``string`` - transaction ‘to’ address
-  ``Amount``:``uint64`` - transaction amount
-  ``AccountNonce``:``int`` - transaction nonce
-  ``GasPrice``:``uint64`` - transaction gasprice
-  ``GasLimit``:``uint64`` - transaction gaslimit
-  ``Timestamp``:``uint64`` - Time stamp
-  ``Payload``:``string`` - transaction payload
-  ``Sig``:``string`` - transaction signature

.. _example-2:

Example
^^^^^^^

.. code:: js

   // Request
   client sendtx --amount 10000 --price 1 --gas 2 --from .keystore-shard-1-0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21 --to 0xb286933bccbec9ca1cd92257d12d12ebab9b1201

   // Result:
   Please input your key file password: 
   account 0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21 current nonce: 0, sending nonce: 0
   transaction sent successfully
   {
       "Hash": "0x9c0e2565b8a0b33c3f69aa6eb9bad4a86c3925a1fe12272e2082091b9b1c5609",
       "Data": {
           "From": "0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21",
           "To": "0xb286933bccbec9ca1cd92257d12d12ebab9b1201",
           "Amount": 10000,
           "AccountNonce": 0,
           "GasPrice": 1,
           "GasLimit": 21000,
           "Timestamp": 0,
           "Payload": ""
       },
       "Signature": {
           "Sig": "N8XzJ/GEpU73dpzW5t5WShmVPFb8gQOrInGdypul8aBaDakmhbZ2rdqekA5bWslHQBfsoafeMukF5b7A1/6JWQA="
       }
   }

--------------

GetAccountNonce
~~~~~~~~~~~~~~~

This method is used to obtain the nonce of the address.

+---------+-------------------------------------------------------------------+
| Type    | Template                                                          |
+=========+===================================================================+
| Console | ``client getnonce -a <rpc address> --account 0x<public address>`` |
+---------+-------------------------------------------------------------------+

.. _parameters-3:

Parameters
^^^^^^^^^^

-  ``address, a``:``string`` - address for client to request (default:
   “127.0.0.1:8027”)
-  ``account``:``string`` - wallet address

.. _returns-3:

Returns
^^^^^^^

-  ``result``:``uint64`` - nonce

.. _example-3:

Example
^^^^^^^

.. code:: js

   // Request
   client getnonce --account 0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21

   // Result
   3

--------------

GetBlockHeight
~~~~~~~~~~~~~~

This method is used to obtain the height of the blockchain.

+---------+--------------------------------------------+
| Type    | Template                                   |
+=========+============================================+
| Console | ``client getblockheight -a <rpc address>`` |
+---------+--------------------------------------------+

.. _parameters-4:

Parameters
^^^^^^^^^^

-  ``address, a``:``string`` - address for client to request (default:
   “127.0.0.1:8027”)

.. _returns-4:

Returns
^^^^^^^

-  ``result``:``uint64`` - nonce

.. _example-4:

Example
^^^^^^^

.. code:: js

   // Request
   client getblockheight

   // Result
   1928

--------------

GetBlock
~~~~~~~~

This method is used to obtain the block content based on block height or
block hash.

+---------+-----------------------------------------------------------------+
| Type    | Template                                                        |
+=========+=================================================================+
| Console | ``client getblock --height -1 --hash -f=true -a <rpc address>`` |
+---------+-----------------------------------------------------------------+

.. _parameters-5:

Parameters
^^^^^^^^^^

-  ``address, a``:``string`` - address for client to request (default:
   “127.0.0.1:8027”)
-  ``hash``:``string`` - block hash
-  ``height``:``string`` - block height
-  ``fulltx, f``:``boll`` - whether to include detailed transaction
   information

.. _returns-5:

Returns
^^^^^^^

-  ``debts``:``array`` - debts in block
-  ``Hash``:``string`` - debts hash
-  ``Data``:``json`` - debts data
-  ``TxHash``:``string`` - txhash in debt
-  ``Shard``:``int`` - shard number of seele node where debts on
-  ``Account``:``array`` - debt account
-  ``Amount``:``int64`` - debt amount
-  ``Fee``:``int64`` - debt fee
-  ``Code``:``string`` - debt code
-  ``hash``:``string`` - block hash
-  ``header``:``json`` - block header
-  ``CreateTimestamp``:``uint64`` - create timestamp
-  ``Creator``:``string`` - creator address
-  ``DebtHash``:``string`` - debts hash
-  ``Difficulty``:``big.Int`` - block difficulty
-  ``ExtraData``:``string`` - extra data
-  ``Height``:``unit64`` - block height
-  ``Nonce``:``unit64`` - block nonce
-  ``PreviousBlockHash``:``string`` - previous block hash
-  ``ReceiptHash``:``string`` - Receipts hash
-  ``stateHash``:``string`` - state tree hash
-  ``TxDebtHash``:``string`` - debts hash
-  ``TxHash``:``string`` - tx hash
-  ``totalDifficulty``:``big.Int`` - total difficulty
-  ``transactions``:``array`` - transaction array
-  ``accountNonce``:``unit64`` - account nonce
-  ``amount``:``Int`` - transaction amount
-  ``gasLimit``:``Int`` - transaction gas limit
-  ``gasPrice``:``Int`` - transaction gas price
-  ``from``:``string`` - transaction provider
-  ``hash``:``string`` - transaction hash
-  ``payload``:``array`` - transaction payload
-  ``timestamp``:``big.Int`` - timestamp
-  ``to``:``string`` - transaction receiver
-  ``txDebts``:``array`` - transaction debts
-  ``Data``:``json`` - txDebts data
-  ``Account``:``string`` - transaction account
-  ``Amount``:``int`` - transaction amount
-  ``Code``:``string`` - transaction code
-  ``Fee``:``int`` - transaction fee
-  ``Shard``:``int`` - transaction shard number
-  ``TxHash``:``string`` - transaction hash
-  ``Hash``:``string`` - txDebts hash

.. _example-5:

Example
^^^^^^^

.. code:: js

   // Request
   client getblock --height 10368 --fulltx=true

   // Result
   {
       "jsonrpc": "2.0",
       "id": 1,
       "result": {
           "debts": [
               {
                   "Hash": "0x0da1ed893e7f0ca2558c193b3b82ed20575a6978bea5b14f282309c69fee368e",
                   "Data": {
                       "TxHash": "0x58752f8aeb2c69dd2c32059d3ad8b2d3d860c6d92aa2b3b30ff985e564f60fae",
                       "Shard": 2,
                       "Account": "0x0ea2a45ab5a909c309439b0e004c61b7b2a3e831",
                       "Amount": 10000,
                       "Fee": 0,
                       "Code": ""
                   }
               }
           ],
           "hash": "0x000002069d9de64bad509239e2a121afbf7de183576457a1d1fb077d19fa3e8c",
           "header": {
               "PreviousBlockHash": "0x000001cba2c0b82402b3d2d2ad49f50ca0b21aee18c8123486377b2ec93aa0e0",
               "Creator": "0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21",
               "StateHash": "0x8af14975f636ace27571cfcdcd9a1a1b4a5b15228977cf6207e82f63abf96ffd",
               "TxHash": "0xdb00575ff0cc0de89bd6c1799d37e5f600687963785176ca76e81bebfde6a03f",
               "ReceiptHash": "0x02fa1d68e7bbf0b833f6e8719efb11b32c7f760e4ae050a4f9b58b8dd8ad1620",
               "TxDebtHash": "0x58d7c36b25a715f5076ccb878940920f6bb333ab142287452509f881103960d2",
               "DebtHash": "0x0000000000000000000000000000000000000000000000000000000000000000",
               "Difficulty": 6563003,
               "Height": 10368,
               "CreateTimestamp": 1539050098,
               "Nonce": 17825487295277268182,
               "ExtraData": ""
           },
           "totalDifficulty": 68985339754,
           "transactions": [
               {
                   "accountNonce": 0,
                   "amount": 150000000,
                   "from": "0x0000000000000000000000000000000000000000",
                   "gasLimit": 0,
                   "gasPrice": 0,
                   "hash": "0x6fb17b265260caed33b4e8f58ad84b508dd8950b9bc93dae8518fc96912f76bb",
                   "payload": "",
                   "timestamp": 1539931510,
                   "to": "0xd5a145191b7ca9cb4f3dc850e426c1e853d2a9f1"
               },
               {
                   "accountNonce": 280,
                   "amount": 10000,
                   "from": "0xec759db47a65f6537d630517f6cd3ca39c6f93d1",
                   "gasLimit": 21000,
                   "gasPrice": 1,
                   "hash": "0xf526dc404145cd409601e951fec4f2222f3abf578381cdaaea9db3a791a79cbd",
                   "payload": "",
                   "timestamp": 0,
                   "to": "0xa00d22dc3624d4696eff8d1641b442f79c3379b1"
               }
           ],
           "txDebts": [
               {
                   "Hash": "0xe1c24a636a7c27aea7c384f6eb61eb49168129105f4c081ffa8ca7e77198b3f6",
                   "Data": {
                       "TxHash": "0x0b30a6edf95a16933a0a77ffd3eb15680d4e3cb79466f21c1181c013a68eae62",
                       "Shard": 2,
                       "Account": "0x0ea2a45ab5a909c309439b0e004c61b7b2a3e831",
                       "Amount": 10000,
                       "Fee": 0,
                       "Code": ""
                   }
               }
           ]
       }
   }
   // Request
   client getblock --hash 0x000002069d9de64bad509239e2a121afbf7de183576457a1d1fb077d19fa3e8c --fulltx=true

   // Result
   {
       "jsonrpc": "2.0",
       "id": 1,
       "result": {
           "debts": [
               {
                   "Hash": "0x0da1ed893e7f0ca2558c193b3b82ed20575a6978bea5b14f282309c69fee368e",
                   "Data": {
                       "TxHash": "0x58752f8aeb2c69dd2c32059d3ad8b2d3d860c6d92aa2b3b30ff985e564f60fae",
                       "Shard": 2,
                       "Account": "0x0ea2a45ab5a909c309439b0e004c61b7b2a3e831",
                       "Amount": 10000,
                       "Fee": 0,
                       "Code": ""
                   }
               }
           ],
           "hash": "0x000002069d9de64bad509239e2a121afbf7de183576457a1d1fb077d19fa3e8c",
           "header": {
               "PreviousBlockHash": "0x000001cba2c0b82402b3d2d2ad49f50ca0b21aee18c8123486377b2ec93aa0e0",
               "Creator": "0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21",
               "StateHash": "0x8af14975f636ace27571cfcdcd9a1a1b4a5b15228977cf6207e82f63abf96ffd",
               "TxHash": "0xdb00575ff0cc0de89bd6c1799d37e5f600687963785176ca76e81bebfde6a03f",
               "ReceiptHash": "0x02fa1d68e7bbf0b833f6e8719efb11b32c7f760e4ae050a4f9b58b8dd8ad1620",
               "TxDebtHash": "0x58d7c36b25a715f5076ccb878940920f6bb333ab142287452509f881103960d2",
               "DebtHash": "0x0000000000000000000000000000000000000000000000000000000000000000",
               "Difficulty": 6563003,
               "Height": 10368,
               "CreateTimestamp": 1539050098,
               "Nonce": 17825487295277268182,
               "ExtraData": ""
           },
           "totalDifficulty": 68985339754,
           "transactions": [
               {
                   "accountNonce": 0,
                   "amount": 150000000,
                   "from": "0x0000000000000000000000000000000000000000",
                   "gasLimit": 0,
                   "gasPrice": 0,
                   "hash": "0x6fb17b265260caed33b4e8f58ad84b508dd8950b9bc93dae8518fc96912f76bb",
                   "payload": "",
                   "timestamp": 1539931510,
                   "to": "0xd5a145191b7ca9cb4f3dc850e426c1e853d2a9f1"
               },
               {
                   "accountNonce": 280,
                   "amount": 10000,
                   "from": "0xec759db47a65f6537d630517f6cd3ca39c6f93d1",
                   "gasLimit": 21000,
                   "gasPrice": 1,
                   "hash": "0xf526dc404145cd409601e951fec4f2222f3abf578381cdaaea9db3a791a79cbd",
                   "payload": "",
                   "timestamp": 0,
                   "to": "0xa00d22dc3624d4696eff8d1641b442f79c3379b1"
               }
           ],
           "txDebts": [
               {
                   "Hash": "0xe1c24a636a7c27aea7c384f6eb61eb49168129105f4c081ffa8ca7e77198b3f6",
                   "Data": {
                       "TxHash": "0x0b30a6edf95a16933a0a77ffd3eb15680d4e3cb79466f21c1181c013a68eae62",
                       "Shard": 2,
                       "Account": "0x0ea2a45ab5a909c309439b0e004c61b7b2a3e831",
                       "Amount": 10000,
                       "Fee": 0,
                       "Code": ""
                   }
               }
           ]
       }
   }

--------------

SaveKey
~~~~~~~

This method saves the private key.

+---------+----------------------------------------+
| Type    | Template                               |
+=========+========================================+
| Console | \`client savekey –privatekey 0x –file  |
+---------+----------------------------------------+

.. _parameters-6:

Parameters
^^^^^^^^^^

-  ``privatekey``:``string`` - private key for account
-  ``file``:``string`` - key store file name (default: “.keystore”)

.. _returns-6:

Returns
^^^^^^^

-  none

.. _example-6:

Example
^^^^^^^

.. code:: js

   // Request
   client savekey --privatekey 0x52117b49022b246ee3921a7ff6771df065594a0dde555e40d8ce940a3ecfb654

   // Result
   Password:
   Repeat password:
   store key successful

--------------

GetAccountShardNum
~~~~~~~~~~~~~~~~~~

This method is used to get the account shard number with the specified
account.

+-----------------------------------+-----------------------------------+
| Type                              | Template                          |
+===================================+===================================+
| Console                           | ``client getshardnum --account <s |
|                                   | tring>``                          |
|                                   | \ ``client getshardnum --privatek |
|                                   | ey <string>``                     |
+-----------------------------------+-----------------------------------+

.. _parameters-7:

Parameters
^^^^^^^^^^

-  ``account``:``string`` - account address
-  ``privatekey``:``string`` - private key for account

.. _returns-7:

Returns
^^^^^^^

-  ``shard number``:``int`` - shard number

.. _example-7:

Example
^^^^^^^

.. code:: js

   // Request
   client getshardnum --account 0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21

   // Result
   shard number: 1

   // Request
   client getshardnum --privatekey 0xf65e40c6809643b25ce4df33153da2f3338876f181f83d2281c6ac4a987b1479

   // Result
   shard number: 1

--------------

Call
~~~~

This method is used to execute a given transaction on a statedb of a
given block height. It does not affect the statedb or blockchain and is
useful for executing and retrieving values. However, the height
currently does not support optional and will remove the from parameter
in the next version or more.

+-----------------------------------+-----------------------------------+
| Type                              | Template                          |
+===================================+===================================+
| Console                           | ``client call -a <rpc address> -- |
|                                   | payload 0x<abi bytecode> --to <st |
|                                   | ring> --height <int>``            |
+-----------------------------------+-----------------------------------+

.. _parameters-8:

Parameters
^^^^^^^^^^

-  ``address, a``:``string`` - address for client to request (default:
   “127.0.0.1:8027”)
-  ``height``:``int64`` - block height (default: -1)
-  ``payload``:``string`` - transaction payload info
-  ``to``:``string`` - to address

.. _returns-8:

Returns
^^^^^^^

-  ``contract``:``string`` - contract address
-  ``failed``:``bool`` - contract executes successfully or not
-  ``poststate``:``string`` - state trie root hash after transaction
   execution
-  ``result``:``string`` - transaction result
-  ``totalFee``:``int64`` - transaction fee
-  ``txhash``:``string`` - transaction hash
-  ``usedGas``:``int64`` - transaction gas

.. _example-8:

Example
^^^^^^^

When using the example below, the contract must be deployed first. The
solidity code file:

::

   pragma solidity ^0.4.0;

   contract SimpleStorage {
       uint storedData=23;

       function set(uint x) {
           storedData=x;
       }
       
       function get() constant returns(uint) {
           return storedData;
       }
   }

As you can see, the example is testing the get function.

.. code:: js

   // Request
   client call --payload 0x6d4ce63c --to 0x9df8ed11ea024183bd584480e80952c9b04e0122 --height -1

   // Result
   succeeded in calling a contract
   {
           "contract": "0x",
           "failed": false,
           "poststate": "0x7c8b22f29b0f9e4db9d61264d3ea6bb8fdff412fc667d411a5e9e98205d36197",
           "result": "0x0000000000000000000000000000000000000000000000000000000000000005",
           "totalFee": 101,
           "txhash": "0x16330ce64136bd756491d4685b4fadd1d81fc36e88eff7987d1784bec466da77",
           "usedGas": 424
   }

--------------

GetLogs
~~~~~~~

This method gets the event logs by block height, the contract address,
and the event name.

+-----------------------------------+-----------------------------------+
| Type                              | Template                          |
+===================================+===================================+
| Console                           | ``client getlogs --height <block  |
|                                   | height> --address 0x<contract add |
|                                   | ress> --topic 0x<event name hash> |
|                                   | ``                                |
+-----------------------------------+-----------------------------------+

.. _parameters-9:

Parameters
^^^^^^^^^^

-  ``address, a``:``string`` - address for client to request (default:
   “127.0.0.1:8027”)
-  ``height``:``int64`` - block height (default: -1)
-  ``contract``:``string`` - contract code in hex
-  ``topic``:``string`` - topic

.. _returns-9:

Returns
^^^^^^^

-  ``response``:``GetLogsResponse`` - response parameter struct
-  ``Txhash``:``string`` - transaction hash
-  ``LogIndex``:``uint`` - log index in receipt’s logs
-  ``Log``:``string`` - log json

.. _example-9:

Example
^^^^^^^

When using the example below, the contract must be deployed first. The
solidity code file:

::

   pragma solidity ^0.4.0;

   contract simple_storage_1 {
       uint storedData=23;
       
       event getLog(address addr, string message);
       event getLog1(string message);
       event getLog2(string message);

       function set(uint x) public{
           getLog1("set getLog1");
           getLog2("set getLog2");
           storedData=x;
       }
       
       function get() constant public returns(uint) {
           getLog(msg.sender, "get getLog");
           getLog1("get getLog1");
           set(16);
           return storedData;
       }
   }

As you can see, this example is testing the get function. In this
situation, the height is the block height of the block containing the
get transaction.

.. code:: js

   // Request
   client getlogs --height 299 --address 0x40bdd5ab58a26cf761607684bd0230b1ea8200f2 --topic 0x978acaf30839c63aff19afed19ff8f3a430103773a67e3890aa1639af9a71bc4

   // Result
   [
           {
                   "Log": {
                           "address": "0x40bdd5ab58a26cf761607684bd0230b1ea8200f2",
                           "blockNumber": 299,
                           "data": "AAAAAAAAAAAAAAAACleicU4ZO3rFBHXOYl8tz7SD10EAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAKZ2V0IGdldExvZwAAAAAAAAAAAAAAAAAAAAAAAAAAAAA=",
                           "topics": [
                                   "0x978acaf30839c63aff19afed19ff8f3a430103773a67e3890aa1639af9a71bc4"
                           ],
                           "transactionIndex": 1
                   },
                   "LogIndex": 0,
                   "Txhash": "0x2a06accc3739845451d50c74bc28a66c6152e9e536e263c3549a404abe8259fc"
           }
   ]

--------------

GetBlockTransactionCount
~~~~~~~~~~~~~~~~~~~~~~~~

This method is used to obtain the number of transactions in the
transaction pool based on block height or hash.

+---------+---------------------------------------------------------+
| Type    | Template                                                |
+=========+=========================================================+
| Console | ``client getblocktxcount --height -1 -a <rpc address>`` |
+---------+---------------------------------------------------------+

.. _parameters-10:

Parameters
^^^^^^^^^^

-  ``address, a``:``string`` - address for client to request (default:
   “127.0.0.1:8027”)
-  ``hash``:``string`` - hash value in hex
-  ``height``:``int64`` - block height (default: -1)

.. _returns-10:

Returns
^^^^^^^

-  ``result``:``int`` - number of transaction

.. _example-10:

Example
^^^^^^^

.. code:: js

   // Request
   client getblocktxcount --height 4202

   // Result
   2

   // Request
   client getblocktxcount --hash 0x0000015592fab87d6efa10e63d7722f6f359d90a1aff9e70930b291931c34922

   // Result
   2

--------------

GetTransactionByBlockIndex
~~~~~~~~~~~~~~~~~~~~~~~~~~

This method is used to obtain the transaction content based on block
height and transaction index.

+---------+----------------------------------------------------------------+
| Type    | Template                                                       |
+=========+================================================================+
| Console | ``client gettxinblock --height -1 --index 0 -a <rpc address>`` |
+---------+----------------------------------------------------------------+

.. _parameters-11:

Parameters
^^^^^^^^^^

-  ``address, a``:``string`` - address for client to request (default:
   “127.0.0.1:8027”)
-  ``hash``:``string`` - block height
-  ``height``:``int`` - block height (default: -1)
-  ``index``:``int`` - transaction index, start with 0 (default: 0)

.. _returns-11:

Returns
^^^^^^^

-  ``accountNonce``:``unit64`` - account nonce
-  ``amount``:``Int`` - transaction amount
-  ``gasLimit``:``Int`` - transaction gas limit
-  ``gasPrice``:``Int`` - transaction gas price
-  ``from``:``string`` - transaction provider
-  ``to``:``string`` - transaction receiver
-  ``hash``:``string`` - transaction hash
-  ``payload``:``array`` - transaction payload
-  ``timestamp``:``string`` - transaction timestamp

.. _example-11:

Example
^^^^^^^

.. code:: js

   // Request
   client gettxinblock --hash 0x0000015592fab87d6efa10e63d7722f6f359d90a1aff9e70930b291931c34922 --height -1 --index 1

   // Result
   {
           "accountNonce": 0,
           "amount": 150000000,
           "from": "0x0000000000000000000000000000000000000000",
           "gasLimit": 0,
           "gasPrice": 0,
           "hash": "0x473ea3667d073491d5896a93fcf84d7dd822988d07482f21e7a875787539e62e",
           "payload": "",
           "timestamp": 1540178976,
           "to": "0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21"
   }

--------------

GetTransactionByHash
~~~~~~~~~~~~~~~~~~~~

This method returns tx information by hash.

+---------+---------------------------------------------------------+
| Type    | Template                                                |
+=========+=========================================================+
| Console | ``client gettxbyhash --hash <string> -a <rpc address>`` |
+---------+---------------------------------------------------------+

.. _parameters-12:

Parameters
^^^^^^^^^^

-  ``hash``:``string`` - hash value in hex
-  ``address, a``:``string`` - address for client to request (default:
   “127.0.0.1:8027”)

.. _returns-12:

Returns
^^^^^^^

-  ``blockHash``:``string`` - block hash
-  ``blockHeight``:``int`` - block height
-  ``status``:``string`` - transaction status
-  ``accountNonce``:``unit64`` - account nonce
-  ``amount``:``Int`` - transaction amount
-  ``gasLimit``:``Int`` - transaction gas limit
-  ``gasPrice``:``Int`` - transaction gas price
-  ``from``:``string`` - transaction provider
-  ``to``:``string`` - transaction receiver
-  ``hash``:``string`` - transaction hash
-  ``payload``:``array`` - transaction payload
-  ``timestamp``:``int64`` - transaction timestamp
-  ``txIndex``:``int`` - transaction index in block

.. _example-12:

Example
^^^^^^^

.. code:: js

   // Request
   client gettxbyhash --hash 0x473ea3667d073491d5896a93fcf84d7dd822988d07482f21e7a875787539e62e

   // Result
   {
           "blockHash": "0x0000009c753570436b0bdd4ea1b9cfb1611f181f7aae82d4ba265761c50c8479",
           "blockHeight": 3608,
           "status": "block",
           "transaction": {
                   "accountNonce": 0,
                   "amount": 150000000,
                   "from": "0x0000000000000000000000000000000000000000",
                   "gasLimit": 0,
                   "gasPrice": 0,
                   "hash": "0x473ea3667d073491d5896a93fcf84d7dd822988d07482f21e7a875787539e62e",
                   "payload": "",
                   "timestamp": 1540178976,
                   "to": "0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21"
           },
           "txIndex": 0
   }

--------------

GetReceiptByTxHash
~~~~~~~~~~~~~~~~~~

This method is used to obtain the receipt contents based on transaction
hash.

+-----------------------------------+-----------------------------------+
| Type                              | Template                          |
+===================================+===================================+
| Console                           | ``client getreceipt --hash <strin |
|                                   | g> --abi <string> -a <rpc address |
|                                   | >``                               |
+-----------------------------------+-----------------------------------+

.. _parameters-13:

Parameters
^^^^^^^^^^

-  ``address, a``:``string`` - address for client to request (default:
   “127.0.0.1:8027”)
-  ``hash``:``string`` - hash value in hex
-  ``abi``:``string`` - the abi file of contract

.. _returns-13:

Returns
^^^^^^^

-  ``contract``:``string`` - contract address
-  ``failed``:``bool`` - transaction executes successfully or not
-  ``poststate``:``string`` - state trie root hash after transaction
   execution
-  ``result``:``string`` - transaction result
-  ``totalFee``:``int`` - transaction fee
-  ``txhash``:``string`` - transaction hash
-  ``usedGas``:``int`` - transaction gas

.. _example-13:

Example
^^^^^^^

.. code:: js

   // Request
   client getreceipt --hash 0x9c0e2565b8a0b33c3f69aa6eb9bad4a86c3925a1fe12272e2082091b9b1c5609

   // Result
   {
       "contract": "0x",
       "failed": false,
       "poststate": "0xef59ced1b06d3ec77aa5c3b0fa1bd7cdd83890961f49d06aabe0a2d57583dd3b",
       "result": "0x",
       "totalFee": 21000,
       "txhash": "0x9c0e2565b8a0b33c3f69aa6eb9bad4a86c3925a1fe12272e2082091b9b1c5609",
       "usedGas": 21000
   }

--------------

GetDebtByHash
~~~~~~~~~~~~~

This method is used to obtain the receipt contents based on transaction
hash.

+---------+-----------------------------------------------------------+
| Type    | Template                                                  |
+=========+===========================================================+
| Console | ``client getdebtbyhash --hash <string> -a <rpc address>`` |
+---------+-----------------------------------------------------------+

.. _parameters-14:

Parameters
^^^^^^^^^^

-  ``address, a``:``string`` - address for client to request (default:
   “127.0.0.1:8027”)
-  ``hash``:``string`` - hash value in hex

.. _returns-14:

Returns
^^^^^^^

-  ``blockHash``:``string`` - block hash of the debt on
-  ``blockHeight``:``int64`` - block height of the debt on
-  ``debt``:``json`` - debt json
-  ``Data``:``json`` - debt data
-  ``Account``:``string`` - debt account
-  ``Amount``:``int64`` - debt amount
-  ``Code``:``string`` - debt code
-  ``Fee``:``int64`` - debt fee
-  ``Shard``:``int`` - shard number of seele node where debts on
-  ``TxHash``:``string`` - txhash in debt
-  ``Hash``:``string`` - debts hash
-  ``debtIndex``:``json`` - debt index json
-  ``BlockHash``:``string`` - block hash of the debt on
-  ``Index``:``string`` - debt index of the block debts
-  ``status``:``string`` - debt status

.. _example-14:

Example
^^^^^^^

.. code:: js

   // Request
   client getdebtbyhash --hash 0x0da1ed893e7f0ca2558c193b3b82ed20575a6978bea5b14f282309c69fee368e

   // Result
   {
           "blockHash": "0x000001a8946d75258f9e269d516e797779ca6bd4b190c701f81456c60958c688",
           "blockHeight": 1112,
           "debt": {
                   "Data": {
                           "Account": "0x0ea2a45ab5a909c309439b0e004c61b7b2a3e831",
                           "Amount": 10000,
                           "Code": "",
                           "Fee": 0,
                           "Shard": 2,
                           "TxHash": "0x58752f8aeb2c69dd2c32059d3ad8b2d3d860c6d92aa2b3b30ff985e564f60fae"
                   },
                   "Hash": "0x0da1ed893e7f0ca2558c193b3b82ed20575a6978bea5b14f282309c69fee368e"
           },
           "debtIndex": {
                   "BlockHash": "0x000001a8946d75258f9e269d516e797779ca6bd4b190c701f81456c60958c688",
                   "Index": 0
           },
           "status": "block"
   }

--------------

GetPeersInfo
~~~~~~~~~~~~

This method returns the information of peer nodes.

+---------+---------------------------------------+
| Type    | Template                              |
+=========+=======================================+
| Console | ``client peersinfo -a <rpc address>`` |
+---------+---------------------------------------+

.. _parameters-15:

Parameters
^^^^^^^^^^

none

.. _returns-15:

Returns
^^^^^^^

-  ``id``:``string`` - node ID
-  ``caps``:``array`` - peer node protocol and version array
-  ``network``:``struct`` - network access address collection
-  ``localAddress``:``string`` - local address
-  ``remoteAddress``:``string`` - remote address
-  ``protocols``:``mao`` - node collection, key is the node name
-  ``version``:``struct`` - node protocal
-  ``difficulty``:``struct`` - node difficulty
-  ``head``:``struct`` - current block hash of the node

.. _example-15:

Example
^^^^^^^

.. code:: js

   // Request
   client getpeersinfo

   // Result
   [
       {
           "caps": [
               "lightSeele/1",
               "seele/1"
           ],
           "id": "0x0ea2a45ab5a909c309439b0e004c61b7b2a3e831",
           "network": {
               "localAddress": "127.0.0.1:55239",
               "remoteAddress": "127.0.0.1:8058"
           },
           "protocols": {
               "lightSeele": "handshake",
               "seele": "handshake"
           },
           "shard": 2
       }
   ]

--------------

GetPeerCount
~~~~~~~~~~~~

This method returns the number of peer nodes.

+---------+-----------------------------------+
| Type    | Template                          |
+=========+===================================+
| Console | ``client peers -a <rpc address>`` |
+---------+-----------------------------------+

.. _parameters-16:

Parameters
^^^^^^^^^^

none

.. _returns-16:

Returns
^^^^^^^

-  ``result``:``int`` - Peer note quantity

.. _example-16:

Example
^^^^^^^

.. code:: js

   // Request
   client peers

   // Result
   1

--------------

GetNetworkVersion
~~~~~~~~~~~~~~~~~

This method returns the network version.

+---------+----------------------------------------+
| Type    | Template                               |
+=========+========================================+
| Console | ``client netversion -a <rpc address>`` |
+---------+----------------------------------------+

.. _parameters-17:

Parameters
^^^^^^^^^^

none

.. _returns-17:

Returns
^^^^^^^

-  ``result``:``uint64`` - version number

.. _example-17:

Example
^^^^^^^

.. code:: js

   // Request
   client netversion

   // Result
   1.0

--------------

GetProtocolVersion
~~~~~~~~~~~~~~~~~~

This method returns the protocol version.

+---------+---------------------------------------------+
| Type    | Template                                    |
+=========+=============================================+
| Console | ``client protocolversion -a <rpc address>`` |
+---------+---------------------------------------------+

.. _parameters-18:

Parameters
^^^^^^^^^^

none

.. _returns-18:

Returns
^^^^^^^

-  ``result``:``uint64`` - version number

.. _example-18:

Example
^^^^^^^

.. code:: js

   // Request
   client protocolversion

   // Result
   1

--------------

GetNetworkID
~~~~~~~~~~~~

This method returns the network id.

+---------+---------------------------------------+
| Type    | Template                              |
+=========+=======================================+
| Console | ``client networkid -a <rpc address>`` |
+---------+---------------------------------------+

.. _parameters-19:

Parameters
^^^^^^^^^^

none

.. _returns-19:

Returns
^^^^^^^

-  ``result``:``string`` - network id

.. _example-19:

Example
^^^^^^^

.. code:: js

   // Request
   client networkid

   // Result
   seele

--------------

Miner Start
~~~~~~~~~~~

This method starts the miner with an input number of threads.

+-----------------------------------+-----------------------------------+
| Type                              | Template                          |
+===================================+===================================+
| Console                           | ``client miner start --threads <m |
|                                   | iner threads num> -a <rpc address |
|                                   | >``                               |
+-----------------------------------+-----------------------------------+

.. _parameters-20:

Parameters
^^^^^^^^^^

-  ``threads``:``int`` - number of threads

.. _returns-20:

Returns
^^^^^^^

none

.. _example-20:

Example
^^^^^^^

.. code:: js

   // Request
   client miner start --threads 2

   // Result
   true

--------------

Miner Stop
~~~~~~~~~~

This method stops the miner.

+---------+----------------------------------------+
| Type    | Template                               |
+=========+========================================+
| Console | ``client miner stop -a <rpc address>`` |
+---------+----------------------------------------+

.. _parameters-21:

Parameters
^^^^^^^^^^

none

.. _returns-21:

Returns
^^^^^^^

none

.. _example-21:

Example
^^^^^^^

.. code:: js

   // Request
   client miner stop

   // Result
   true

--------------

Miner Status
~~~~~~~~~~~~

This method returns the miner’s status.

+---------+------------------------------------------+
| Type    | Template                                 |
+=========+==========================================+
| Console | ``client miner status -a <rpc address>`` |
+---------+------------------------------------------+

.. _parameters-22:

Parameters
^^^^^^^^^^

none

.. _returns-22:

Returns
^^^^^^^

none

.. _example-22:

Example
^^^^^^^

.. code:: js

   // Request
   client miner status

   // Result
   Running

--------------

Miner GetCoinbase
~~~~~~~~~~~~~~~~~

This method is used to obtain the coinbase of miner consensus.

+---------+-----------------------------------------------+
| Type    | Template                                      |
+=========+===============================================+
| Console | ``client miner getcoinbase -a <rpc address>`` |
+---------+-----------------------------------------------+

.. _parameters-23:

Parameters
^^^^^^^^^^

none

.. _returns-23:

Returns
^^^^^^^

-  ``result``:``string`` - coinbase

.. _example-23:

Example
^^^^^^^

.. code:: js

   // Request
   client miner getcoinbase

   // Result
   "0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21"

--------------

Miner SetThreads
~~~~~~~~~~~~~~~~

This method is used to set the threads of miner consensus.

+---------+--------------------------------------------------------------+
| Type    | Template                                                     |
+=========+==============================================================+
| Console | ``client miner setthreads --threads <int> -a <rpc address>`` |
+---------+--------------------------------------------------------------+

.. _parameters-24:

Parameters
^^^^^^^^^^

-  ``threads``:``int`` - miner threads (default: 0)

.. _returns-24:

Returns
^^^^^^^

-  ``result``:``int`` - threads

.. _example-24:

Example
^^^^^^^

.. code:: js

   // Request
   client miner setthreads --threads 2

   // Result
   true

--------------

Miner SetCoinbase
~~~~~~~~~~~~~~~~~

This method is used to set the coinbase

+---------+-------------------------------------------------------------------+
| Type    | Template                                                          |
+=========+===================================================================+
| Console | ``client miner setcoinbase --coinbase <string> -a <rpc address>`` |
+---------+-------------------------------------------------------------------+

.. _parameters-25:

Parameters
^^^^^^^^^^

-  ``coinbase``:``string`` coinbase of the miner

.. _returns-25:

Returns
^^^^^^^

-  none

.. _example-25:

Example
^^^^^^^

.. code:: js

   // Request
   client miner setcoinbase --coinbase 0x16fba5fcb9bc4ee7c3b7fed667e41c9a0248da71

   // Result
   true

--------------

Miner GetEngineInfo
~~~~~~~~~~~~~~~~~~~

This method returns engine information of miner

+---------+-------------------------------------------+
| Type    | Template                                  |
+=========+===========================================+
| Console | ``client getengineinfo -a <rpc address>`` |
+---------+-------------------------------------------+

.. _parameters-26:

Parameters
^^^^^^^^^^

-  ``address, a``:``string`` address for client to request (default:
   “127.0.0.1:8027”)

.. _returns-26:

Returns
^^^^^^^

-  none

.. _example-26:

Example
^^^^^^^

.. code:: js

   // Request
   client getengineinfo

   // Result
   {
       "hashrate": 495812.2433994204,
       "threads": 1
   }

--------------

GetTxPoolContent
~~~~~~~~~~~~~~~~

This method is used to obtain the transaction pool content.

+---------+----------------------------------------------+
| Type    | Template                                     |
+=========+==============================================+
| Console | ``client gettxpoolcontent -a <rpc address>`` |
+---------+----------------------------------------------+

.. _parameters-27:

Parameters
^^^^^^^^^^

none

.. _returns-27:

Returns
^^^^^^^

-  ``accountNonce``:``unit64`` - account nonce
-  ``amount``:``Int`` - transaction amount
-  ``from``:``string`` - transaction provider
-  ``to``:``string`` - transaction receiver
-  ``hash``:``string`` - transaction hash
-  ``payload``:``array`` - transaction payload
-  ``timestamp``:``string`` - transaction timestamp
-  ``fee``:``int`` - transaction fee

.. _example-27:

Example
^^^^^^^

.. code:: js

   // Request
   client gettxpoolcontent

   // Result
   {
       "0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21": [
           {
               "accountNonce": 4,
               "amount": 10000,
               "fee": 1,
               "from": "0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21",
               "hash": "0x1d9579c07e8cbcab36efdd810d2ebd27585c1b79eb379afde5e077c22ad46e44",
               "payload": "",
               "timestamp": 0,
               "to": "0x16fba5fcb9bc4ee7c3b7fed667e41c9a0248da71"
           }
       ]
   }

--------------

GetTxPoolTxCount
~~~~~~~~~~~~~~~~

This method is used to obtain the number of transactions in the
transaction pool.

+---------+--------------------------------------------+
| Type    | Template                                   |
+=========+============================================+
| Console | ``client gettxpoolcount -a <rpc address>`` |
+---------+--------------------------------------------+

.. _parameters-28:

Parameters
^^^^^^^^^^

none

.. _returns-28:

Returns
^^^^^^^

-  ``result``:``uint64`` - number of transactions

.. _example-28:

Example
^^^^^^^

.. code:: js

   // Request
   client gettxpoolcount

   // Result
   1

--------------

GetPendingTransactions
~~~~~~~~~~~~~~~~~~~~~~

This method is used to obtain pending transactions in the transaction
pool.

+---------+-------------------------------------------+
| Type    | Template                                  |
+=========+===========================================+
| Console | ``client getpendingtxs -a <rpc address>`` |
+---------+-------------------------------------------+

.. _parameters-29:

Parameters
^^^^^^^^^^

none

.. _returns-29:

Returns
^^^^^^^

-  ``accountNonce``:``unit64`` - account nonce
-  ``amount``:``Int`` - transaction amount
-  ``from``:``string`` - transaction provider
-  ``to``:``string`` - transaction receiver
-  ``hash``:``string`` - transaction hash
-  ``payload``:``array`` - transaction payload
-  ``timestamp``:``string`` - transaction timestamp
-  ``fee``:``int`` - transaction fee

.. _example-29:

Example
^^^^^^^

.. code:: js

   // Request
   client getpendingtxs

   // Result
   [
       {
           "accountNonce": 6,
           "amount": 10000,
           "fee": 1,
           "from": "0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21",
           "hash": "0x4ad5843af174d32e31b54ef81ddcbfeec43f4eb5d01885dfe9828f9ce907fb80",
           "payload": "",
           "timestamp": 0,
           "to": "0x16fba5fcb9bc4ee7c3b7fed667e41c9a0248da71"
       }
   ]

--------------

GetPendingDebts
~~~~~~~~~~~~~~~

This method is used to obtain pending debts in the debts pool.

+---------+--------------------------------------+
| Type    | Template                             |
+=========+======================================+
| Console | ``client getdebts -a <rpc address>`` |
+---------+--------------------------------------+

.. _parameters-30:

Parameters
^^^^^^^^^^

none

.. _returns-30:

Returns
^^^^^^^

-  ``Data``:``json`` - debt data
-  ``Account``:``array`` - debt account
-  ``Amount``:``int64`` - debt amount
-  ``Code``:``string`` - debt code
-  ``Fee``:``int64`` - debt fee
-  ``Shard``:``int`` - shard number of seele node where debts on
-  ``TxHash``:``string`` - txhash in debt
-  ``Hash``:``string`` - debts hash

.. _example-30:

Example
^^^^^^^

.. code:: js

   // Request
   client getdebts

   // Result
   [
           {
                   "Data": {
                           "Account": "0x0ea2a45ab5a909c309439b0e004c61b7b2a3e831",
                           "Amount": 10000,
                           "Code": "",
                           "Fee": 0,
                           "Shard": 2,
                           "TxHash": "0x049305964eac1c62b19f0a6a0841b1d24683c4c4f9a3f23c69c87dcca9ec3e28"
                   },
                   "Hash": "0xdcf8489c27e934c3f289c4a1d843b86dbd3445e8943903613ce640d7fb043e87"
           }
   ]

--------------

DumpHeap
~~~~~~~~

This method dump heap for profiling and returns the file path.

+---------+--------------------------------------+
| Type    | Template                             |
+=========+======================================+
| Console | ``client dumpheap -a <rpc address>`` |
+---------+--------------------------------------+

.. _parameters-31:

Parameters
^^^^^^^^^^

none

.. _returns-31:

Returns
^^^^^^^

-  ``result``:``string`` file path

.. _example-31:

Example
^^^^^^^

.. code:: js

   // Request
   client dumpheap

   // Result
   C:\Users\dell-2\.seele\heap.dump

--------------

Key
~~~

This method is used to generate a public/private key pair and print them
with hex values.

+---------+------------------------------+
| Type    | Template                     |
+=========+==============================+
| Console | ``client key --shard <int>`` |
+---------+------------------------------+

.. _parameters-32:

Parameters
^^^^^^^^^^

-  ``shard``:``uint`` shard number

.. _returns-32:

Returns
^^^^^^^

-  ``public key``:``string`` - public key
-  ``private key``:``string`` - private key

.. _example-32:

Example
^^^^^^^

.. code:: js

   // Request
   client key

   // Result
   public key:  0xf66b94477311556da1767e267e0a5782045eea61
   private key: 0x52117b49022b246ee3921a7ff6771df065594a0dde555e40d8ce940a3ecfb654

--------------

Sign
~~~~

This method is used to sign data with your private key.

+-----------------------------------+-----------------------------------+
| Type                              | Template                          |
+===================================+===================================+
| Console                           | ``client sign --amount <int> --pa |
|                                   | yload <string> --fee <int> --nonc |
|                                   | e <int> --privatekey <string> --t |
|                                   | o <string> -a <rpc address>``     |
+-----------------------------------+-----------------------------------+

.. _parameters-33:

Parameters
^^^^^^^^^^

-  ``address, a``:``string`` address for client to request (default:
   “127.0.0.1:8027”)
-  ``privatekey``:``string`` private key
-  ``to``:``string`` public address of the receiver
-  ``amount``:``unit64`` the amount of the transferred coins
-  ``fee``:``unit64`` transaction fee
-  ``payload``:``string`` transaction payload
-  ``nonce``:``int`` transaction nonce

.. _returns-33:

Returns
^^^^^^^

-  ``Hash``:``string`` transaction hash
-  ``Data``:``struct`` transaction data
-  ``From``:``string`` transaction provider
-  ``To``:``string`` transaction receiver
-  ``Amount``:``string`` public address of the receiver
-  ``AccountNonce``:``unit64`` account nonce
-  ``Fee``:``string`` transaction fee
-  ``Timestamp``:``string`` transaction timestamp
-  ``Payload``:``string`` transaction payload
-  ``Signature``:``string`` transaction signature
-  ``Sig``:``string`` transaction sig

.. _example-33:

Example
^^^^^^^

.. code:: js

   // Request
   client sign --amount 20000 --fee 1 --nonce 7 --privatekey 0xf65e40c6809643b25ce4df33153da2f3338876f181f83d2281c6ac4a987b1479 --to 0x0ea2a45ab5a909c309439b0e004c61b7b2a3e831

   // Result
   account 0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21 current nonce: 7, sending nonce: 7
   {
           "Hash": "0x9ba03f6c4fcbe61a19f1721ec46c3f9dd3db91d236083a33b17396220c4accea",
           "Data": {
                   "From": "0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21",
                   "To": "0x0ea2a45ab5a909c309439b0e004c61b7b2a3e831",
                   "Amount": 20000,
                   "AccountNonce": 7,
                   "Fee": 1,
                   "Timestamp": 0,
                   "Payload": ""
           },
           "Signature": {
                   "Sig": "BFkYL2KdCsoXl/njQs+v9/rwj3c5DVAMjfGTF7P6IdxiL1ra/NpLG/cM2HabPgqD1lV8PBjBy6UAmHuNxz5M1gA="
           }
   }

--------------

GeneratePayload
~~~~~~~~~~~~~~~

This method is used to generate payload.

+-----------------------------------+-----------------------------------+
| Type                              | Template                          |
+===================================+===================================+
| Console                           | ``client payload --abi <string> - |
|                                   | -method <string> --args <string>` |
|                                   | `                                 |
+-----------------------------------+-----------------------------------+

.. _parameters-34:

Parameters
^^^^^^^^^^

-  ``abi``:``string`` the abi file of contract
-  ``method``:``string`` the method name of contract
-  ``args``:``string`` the parameters of contract method

.. _returns-34:

Returns
^^^^^^^

-  ``payload``:``string`` payload data

.. _example-34:

Example
^^^^^^^

.. code:: js

   // Request
   client payload --abi test.sol --method set --args 10

   // Result
   payload:  0x60fe47b1000000000000000000000000000000000000000000000000000000000000000a

--------------

CreateHTLC
~~~~~~~~~~

This method is used to create HTLC.

+-----------------------------------+-----------------------------------+
| Type                              | Template                          |
+===================================+===================================+
| Console                           | ``client htlc create --amount <un |
|                                   | it64> --fee <unit64> --from <file |
|                                   | > --to <string> --hash <string>`` |
+-----------------------------------+-----------------------------------+

.. _parameters-35:

Parameters
^^^^^^^^^^

-  ``address, a``:``string`` address for client to request (default:
   “127.0.0.1:8027”)
-  ``from``:``string`` key file of the sender
-  ``to``:``string`` to address
-  ``amount``:``unit64`` amount value, unit is fan
-  ``fee``:``unit64`` transaction fee
-  ``nonce``:``int`` transaction nonce (default: 0)
-  ``hash``:``string`` hash value in hex
-  ``time``:``int`` time lock in the HTLC (default: 0)

.. _returns-35:

Returns
^^^^^^^

-  ``HashLock``:``string`` contract hash lock
-  ``TimeLock``:``string`` lock time
-  ``Tx``:``struct`` tx
-  ``Hash``:``string`` transaction hash
-  ``Data``:``struct`` transaction data
-  ``From``:``string`` transaction provider
-  ``To``:``string`` transaction receiver
-  ``Amount``:``uint64`` public address of the receiver
-  ``AccountNonce``:``unit64`` account nonce
-  ``Fee``:``unit64`` transaction fee
-  ``Timestamp``:``unit64`` transaction timestamp
-  ``Payload``:``string`` transaction payload
-  ``Signature``:``string`` transaction signature
-  ``Sig``:``string`` transaction sig

.. _example-35:

Example
^^^^^^^

.. code:: js

   // Request
   client htlc create --amount 10000 --fee 1 --from .keystore-shard1-0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21 --to 0x16fba5fcb9bc4ee7c3b7fed667e41c9a0248da71 --hash 0x9b9d066a68bc533fca7be7aaaffd21c9c971bb4b4960e79dcb36c532b67753dc

   // Result
   Please input your key file password:
   account 0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21 current nonce: 7, sending nonce: 7
   {
           "HashLock": "0x9b9d066a68bc533fca7be7aaaffd21c9c971bb4b4960e79dcb36c532b67753dc",
           "TimeLock": 0,
           "Tx": {
                   "Hash": "0xc6ec049925ca2f9ec9860806c75ccbaddfc60e2c8a717d35be905bc1f1173e36",
                   "Data": {
                           "From": "0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21",
                           "To": "0x0000000000000000000000000000000000000103",
                           "Amount": 10000,
                           "AccountNonce": 7,
                           "Fee": 1,
                           "Timestamp": 0,
                           "Payload": "0x007b22486173684c6f636b223a22307839623964303636613638626335333366636137626537616161666664323163396339373162623462343936306537396463623336633533326236373735336463222c2254696d654c6f636b223a302c22546f223a223078313666626135666362396263346565376333623766656436363765343163
   39613032343864613731227d"
                   },
                   "Signature": {
                           "Sig": "Kfup/u6aNxxCucvrollCfCNlL5iXd6ZXyEsQr5GE/9VirAgrNvIjkqmra9eTd9lxCZZXOtDMZNrAzpAQCXT3sAE="
                   }
           }
   }

--------------

DecodeHTLC
~~~~~~~~~~

This method is used to decode HTLC contract information.

+---------+----------------------------------+
| Type    | Template                         |
+=========+==================================+
| Console | ``client htlc decode --payload`` |
+---------+----------------------------------+

.. _parameters-36:

Parameters
^^^^^^^^^^

-  ``payload``:``string`` transaction payload info

.. _returns-36:

Returns
^^^^^^^

-  ``HashLock``:``string`` contract hash lock
-  ``TimeLock``:``string`` lock time
-  ``Tx``:``struct`` tx
-  ``Hash``:``string`` transaction hash
-  ``Data``:``struct`` transaction data
-  ``From``:``string`` transaction provider
-  ``To``:``string`` transaction receiver
-  ``Amount``:``uint64`` public address of the receiver
-  ``AccountNonce``:``unit64`` account nonce
-  ``Fee``:``unit64`` transaction fee
-  ``Timestamp``:``unit64`` transaction timestamp
-  ``Payload``:``string`` transaction payload
-  ``Signature``:``string`` transaction signature
-  ``Sig``:``string`` transaction sig
-  ``To``:``string`` transaction receiver
-  ``Refunded``:``bool`` whether refunded
-  ``Withdrawed``:``bool`` whether withdrawed
-  ``Preimage``:``string`` HTLC preimage

.. _example-36:

Example
^^^^^^^

.. code:: js

   // Request
   client htlc decode --payload 0x7b22486173684c6f636b223a22307839623964303636613638626335333366636137626537616161666664323163396339373162623462343936306537396463623336633533326236373735336463222c2254696d654c6f636b223a302c22546f223a22307831366662613566636239626334656537633362376665643636376534316339613032343864613731227d

   // Result
   {
           "Tx": null,
           "HashLock": "0x9b9d066a68bc533fca7be7aaaffd21c9c971bb4b4960e79dcb36c532b67753dc",
           "TimeLock": 0,
           "To": "0x16fba5fcb9bc4ee7c3b7fed667e41c9a0248da71",
           "Refunded": false,
           "Withdrawed": false,
           "Preimage": ""
   }

--------------

GetHTLC
~~~~~~~

This method is used to get HTLC information.

+-----------------------------------+-----------------------------------+
| Type                              | Template                          |
+===================================+===================================+
| Console                           | ``client htlc get --fee <unit64>  |
|                                   | --from <file> --nonce <int> --has |
|                                   | h <string>``                      |
+-----------------------------------+-----------------------------------+

.. _parameters-37:

Parameters
^^^^^^^^^^

-  ``address, a``:``string`` address for client to request (default:
   “127.0.0.1:8027”)
-  ``from``:``string`` key file of the sender
-  ``fee``:``unit64`` transaction fee
-  ``nonce``:``int`` transaction nonce (default: 0)
-  ``hash``:``string`` hash value in hex

.. _returns-37:

Returns
^^^^^^^

-  ``HashLock``:``string`` contract hash lock
-  ``TimeLock``:``string`` lock time
-  ``Tx``:``struct`` tx
-  ``Hash``:``string`` transaction hash
-  ``Data``:``struct`` transaction data
-  ``From``:``string`` transaction provider
-  ``To``:``string`` transaction receiver
-  ``Amount``:``uint64`` public address of the receiver
-  ``AccountNonce``:``unit64`` account nonce
-  ``Fee``:``unit64`` transaction fee
-  ``Timestamp``:``unit64`` transaction timestamp
-  ``Payload``:``string`` transaction payload
-  ``Signature``:``string`` transaction signature
-  ``Sig``:``string`` transaction sig
-  ``hash``:``string`` get hash

.. _example-37:

Example
^^^^^^^

.. code:: js

   // Request
   client htlc get --fee 1 --from .keystore-shard1-0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21 --nonce 7 --hash 0xc6ec049925ca2f9ec9860806c75ccbaddfc60e2c8a717d35be905bc1f1173e36

   // Result
   Please input your key file password:
   account 0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21 current nonce: 7, sending nonce: 7
   {
           "Tx": {
                   "Hash": "0xc0efd904a084bb5b043cf08e0d826a68a71e0c6a01a4a279c2814802c5a1238d",
                   "Data": {
                           "From": "0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21",
                           "To": "0x0000000000000000000000000000000000000103",
                           "Amount": 0,
                           "AccountNonce": 7,
                           "Fee": 1,
                           "Timestamp": 0,
                           "Payload": "0x03c6ec049925ca2f9ec9860806c75ccbaddfc60e2c8a717d35be905bc1f1173e36"
                   },
                   "Signature": {
                           "Sig": "IySR/k7YpfXX0l8n8bwd7KRbrgE7hTVlfzqvS1diKT9X8zKXlMfQ8ijfvd4EVSY6TcLWpAb9TfoeRVjIGoVXJgE="
                   }
           },
           "hash": "0xc6ec049925ca2f9ec9860806c75ccbaddfc60e2c8a717d35be905bc1f1173e36"
   }

--------------

GenerateHTLCKey
~~~~~~~~~~~~~~~

This method is used to generate preimage key and key hash.

+---------+---------------------+
| Type    | Template            |
+=========+=====================+
| Console | ``client htlc key`` |
+---------+---------------------+

.. _parameters-38:

Parameters
^^^^^^^^^^

none

.. _returns-38:

Returns
^^^^^^^

-  ``preimage``:``string`` preimage key
-  ``hash``:``string`` key hash

.. _example-38:

Example
^^^^^^^

.. code:: js

   // Request
   client htlc key

   // Result
   preimage: 0xffacc1067faf412f19db50b53b0b6a87d3f8a3af1778342edaa6d7f448a60b6a
   hash: 0x39e29785892df0be30d54f406381cbb7c3566510fb6d6862c4da6ca4a16a66fe

--------------

RefundFromHTLC
~~~~~~~~~~~~~~

This method is used to refund from HTLC.

+-----------------------------------+-----------------------------------+
| Type                              | Template                          |
+===================================+===================================+
| Console                           | ``client htlc refund --fee <unit6 |
|                                   | 4> --from <file> --nonce <int> -- |
|                                   | hash <string>``                   |
+-----------------------------------+-----------------------------------+

.. _parameters-39:

Parameters
^^^^^^^^^^

-  ``address, a``:``string`` address for client to request (default:
   “127.0.0.1:8027”)
-  ``from``:``string`` key file of the sender
-  ``fee``:``unit64`` transaction fee
-  ``nonce``:``int`` transaction nonce (default: 0)
-  ``hash``:``string`` hash value in hex

.. _returns-39:

Returns
^^^^^^^

-  ``HashLock``:``string`` contract hash lock
-  ``TimeLock``:``string`` lock time
-  ``Tx``:``struct`` tx
-  ``Hash``:``string`` transaction hash
-  ``Data``:``struct`` transaction data
-  ``From``:``string`` transaction provider
-  ``To``:``string`` transaction receiver
-  ``Amount``:``uint64`` public address of the receiver
-  ``AccountNonce``:``unit64`` account nonce
-  ``Fee``:``unit64`` transaction fee
-  ``Timestamp``:``unit64`` transaction timestamp
-  ``Payload``:``string`` transaction payload
-  ``Signature``:``string`` transaction signature
-  ``Sig``:``string`` transaction sig
-  ``hash``:``string`` get hash

.. _example-39:

Example
^^^^^^^

.. code:: js

   // Request
   client htlc refund --fee 1 --from .keystore-shard1-0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21 --nonce 7 --hash 0xc6ec049925ca2f9ec9860806c75ccbaddfc60e2c8a717d35be905bc1f1173e36

   // Result
   Please input your key file password:
   account 0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21 current nonce: 7, sending nonce: 7
   {
           "Tx": {
                   "Hash": "0x3662a1e37c654db07e9b72f8b756e3f1890da5fa105fa81101a790f7161469ea",
                   "Data": {
                           "From": "0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21",
                           "To": "0x0000000000000000000000000000000000000103",
                           "Amount": 0,
                           "AccountNonce": 7,
                           "Fee": 1,
                           "Timestamp": 0,
                           "Payload": "0x02c6ec049925ca2f9ec9860806c75ccbaddfc60e2c8a717d35be905bc1f1173e36"
                   },
                   "Signature": {
                           "Sig": "vxrwq8LbniTBuTi0TX/0AC57k74MWkViTPpl7BMsKoVZIXvF0NLTQ1fZsKrlBS//Co1SHjhZ8Ttjc73up115IwE="
                   }
           },
           "hash": "0xc6ec049925ca2f9ec9860806c75ccbaddfc60e2c8a717d35be905bc1f1173e36"
   }

--------------

GenerateHTLCStamptime
~~~~~~~~~~~~~~~~~~~~~

This method is used to generate unix timestamp.

+---------+-----------------------------------+
| Type    | Template                          |
+=========+===================================+
| Console | ``client htlc time --time <int>`` |
+---------+-----------------------------------+

.. _parameters-40:

Parameters
^^^^^^^^^^

-  ``time``:``uint64`` time lock in the HTLC (default: 0)

.. _returns-40:

Returns
^^^^^^^

-  ``locktime``:``uint64`` unix time stamptime

.. _example-40:

Example
^^^^^^^

.. code:: js

   // Request
   client htlc time

   // Result
   locktime: 1538982094

--------------

WithdrawFromHTLC
~~~~~~~~~~~~~~~~

This method is used to withdraw from HTLC.

+-----------------------------------+-----------------------------------+
| Type                              | Template                          |
+===================================+===================================+
| Console                           | ``client htlc withdraw --fee <uni |
|                                   | t64> --from <file> --nonce <int>  |
|                                   | --hash <string> --preimage <strin |
|                                   | g>``                              |
+-----------------------------------+-----------------------------------+

.. _parameters-41:

Parameters
^^^^^^^^^^

-  ``address, a``:``string`` address for client to request (default:
   “127.0.0.1:8027”)
-  ``from``:``string`` key file of the sender
-  ``fee``:``unit64`` transaction fee
-  ``nonce``:``int`` transaction nonce (default: 0)
-  ``hash``:``string`` hash value in hex
-  ``preimage``:``string`` preimage of hash in the HTLC

.. _returns-41:

Returns
^^^^^^^

-  ``HashLock``:``string`` contract hash lock
-  ``TimeLock``:``string`` lock time
-  ``Tx``:``struct`` tx
-  ``Hash``:``string`` transaction hash
-  ``Data``:``struct`` transaction data
-  ``From``:``string`` transaction provider
-  ``To``:``string`` transaction receiver
-  ``Amount``:``uint64`` public address of the receiver
-  ``AccountNonce``:``unit64`` account nonce
-  ``Fee``:``unit64`` transaction fee
-  ``Timestamp``:``unit64`` transaction timestamp
-  ``Payload``:``string`` transaction payload
-  ``Signature``:``string`` transaction signature
-  ``Sig``:``string`` transaction sig
-  ``hash``:``string`` get hash
-  ``preimage``:``string`` preimage of hash in the HTLC

.. _example-41:

Example
^^^^^^^

.. code:: js

   // Request
   client htlc withdraw --fee 1 --from .keystore-shard1-0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21 --nonce 7 --hash 0xc6ec049925ca2f9ec9860806c75ccbaddfc60e2c8a717d35be905bc1f1173e36 --preimage 0xffacc1067faf412f19db50b53b0b6a87d3f8a3af1778342edaa6d7f448a60b6a

   // Result
   Please input your key file password:
   account 0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21 current nonce: 7, sending nonce: 7
   {
           "Tx": {
                   "Hash": "0x44ffbd4aef7481b4375fc0b7cdba135986e8f822a59d222f4517ac43be11ea16",
                   "Data": {
                           "From": "0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21",
                           "To": "0x0000000000000000000000000000000000000103",
                           "Amount": 0,
                           "AccountNonce": 7,
                           "Fee": 1,
                           "Timestamp": 0,
                           "Payload": "0x017b2248617368223a22307863366563303439393235636132663965633938363038303663373563636261646466633630653263386137313764333562653930356263316631313733653336222c22507265696d616765223a2230786666616363313036376661663431326631396462353062353362306236613837643366386133616631
   3737383334326564616136643766343438613630623661227d"
                   },
                   "Signature": {
                           "Sig": "gYUQC4KpPJKIdL4G160QQXEYBSqZzVbDevtshXN/mRJcDfYNBPDJmKTBpe07Fz9IhDt8RKJY/uEyEQrQNbhD6AA="
                   }
           },
           "hash": "0xc6ec049925ca2f9ec9860806c75ccbaddfc60e2c8a717d35be905bc1f1173e36",
           "preimage": "0xffacc1067faf412f19db50b53b0b6a87d3f8a3af1778342edaa6d7f448a60b6a"
   }

--------------

RegisterDomainName
~~~~~~~~~~~~~~~~~~

This method is used to register a domain name.

+-----------------------------------+-----------------------------------+
| Type                              | Template                          |
+===================================+===================================+
| Console                           | ``client domain register --fee <u |
|                                   | nit64> --from <file> --nonce <int |
|                                   | > --name <string>``               |
+-----------------------------------+-----------------------------------+

.. _parameters-42:

Parameters
^^^^^^^^^^

-  ``address, a``:``string`` address for client to request (default:
   “127.0.0.1:8027”)
-  ``from``:``string`` key file of the sender
-  ``fee``:``unit64`` transaction fee
-  ``nonce``:``int`` transaction nonce (default: 0)
-  ``name``:``string`` domain or subchain name

.. _returns-42:

Returns
^^^^^^^

-  ``Hash``:``string`` transaction hash
-  ``Data``:``struct`` transaction data
-  ``From``:``string`` transaction provider
-  ``To``:``string`` transaction receiver
-  ``Amount``:``uint64`` public address of the receiver
-  ``AccountNonce``:``unit64`` account nonce
-  ``Fee``:``unit64`` transaction fee
-  ``Timestamp``:``unit64`` transaction timestamp
-  ``Payload``:``string`` transaction payload
-  ``Signature``:``string`` transaction signature
-  ``Sig``:``string`` transaction sig

.. _example-42:

Example
^^^^^^^

.. code:: js

   // Request
   client domain register --from .keystore-shard1-0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21 --fee 1 --name test1

   // Result
   Please input your key file password:
   account 0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21 current nonce: 7, sending nonce: 7
   {
           "Hash": "0x654c264e25bbe4db8b4e8600ef5407f6f3ac420b916f805f10015362aeb16af8",
           "Data": {
                   "From": "0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21",
                   "To": "0x0000000000000000000000000000000000000101",
                   "Amount": 0,
                   "AccountNonce": 7,
                   "Fee": 1,
                   "Timestamp": 0,
                   "Payload": "0x007465737431"
           },
           "Signature": {
                   "Sig": "kqXargvc/ltBDPIQXwJAIUY/wn9uDb6UM7JkTiMTkGYmcF+y22mb0peCXx2OBpF6Y9vKXJUTNIFD2G/RNA3FpwA="
           }
   }

--------------

GetDomainNameOwner
~~~~~~~~~~~~~~~~~~

This method is used to get the domain name owner.

+-----------------------------------+-----------------------------------+
| Type                              | Template                          |
+===================================+===================================+
| Console                           | ``client domain owner --fee <unit |
|                                   | 64> --from <file> --nonce <int> - |
|                                   | -name <string>``                  |
+-----------------------------------+-----------------------------------+

.. _parameters-43:

Parameters
^^^^^^^^^^

-  ``address, a``:``string`` address for client to request (default:
   “127.0.0.1:8027”)
-  ``from``:``string`` key file of the sender
-  ``fee``:``unit64`` transaction fee
-  ``nonce``:``int`` transaction nonce (default: 0)
-  ``name``:``string`` domain or subchain name

.. _returns-43:

Returns
^^^^^^^

-  ``Hash``:``string`` transaction hash
-  ``Data``:``struct`` transaction data
-  ``From``:``string`` transaction provider
-  ``To``:``string`` transaction receiver
-  ``Amount``:``uint64`` public address of the receiver
-  ``AccountNonce``:``unit64`` account nonce
-  ``Fee``:``unit64`` transaction fee
-  ``Timestamp``:``unit64`` transaction timestamp
-  ``Payload``:``string`` transaction payload
-  ``Signature``:``string`` transaction signature
-  ``Sig``:``string`` transaction sig

.. _example-43:

Example
^^^^^^^

.. code:: js

   // Request
   client domain owner --from .keystore-shard1-0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21 --fee 1 --name test1

   // Result
   Please input your key file password:
   account 0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21 current nonce: 8, sending nonce: 8
   {
           "Hash": "0xb468f33fe8bfb0558aef0bd123cd086a51d4fd0bd224398d6394ef2998009a1a",
           "Data": {
                   "From": "0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21",
                   "To": "0x0000000000000000000000000000000000000101",
                   "Amount": 0,
                   "AccountNonce": 8,
                   "Fee": 1,
                   "Timestamp": 0,
                   "Payload": "0x017465737431"
           },
           "Signature": {
                   "Sig": "3uEYGubuV/qCpad4reomXRNq3QyKNVG9c302C7u4WZoK7YZYiBd7mxCFq/vQwbU2opt9Rnp6NUHrU608Y/5VIQE="
           }
   }

--------------

GenSubChainCfgFile
~~~~~~~~~~~~~~~~~~

This method is used to generate sub chain config file.

+-----------------------------------+-----------------------------------+
| Type                              | Template                          |
+===================================+===================================+
| Console                           | ``client subchain config --fee <u |
|                                   | nit64> --from <file> --nonce <int |
|                                   | > --name <string>``               |
+-----------------------------------+-----------------------------------+

.. _parameters-44:

Parameters
^^^^^^^^^^

-  ``address, a``:``string`` address for client to request (default:
   “127.0.0.1:8027”)
-  ``coinbase``:``string`` miner coinbase in hex
-  ``privatekey``:``string`` private key for account
-  ``name``:``string`` domain or subchain name
-  ``output, o``:``string`` subchain config file path
-  ``shard``:``string`` shard number (default: 0)
-  ``node, n``:``string`` subchain static node, for example:-n
   address:port -n address:prot

.. _returns-44:

Returns
^^^^^^^

TODO

.. _example-44:

Example
^^^^^^^

.. code:: js

   // Request
   TODO

   // Result
   TODO

--------------

QuerySubChain
~~~~~~~~~~~~~

This method is used to query sub chain.

+-----------------------------------+-----------------------------------+
| Type                              | Template                          |
+===================================+===================================+
| Console                           | ``client subchain query --fee <un |
|                                   | it64> --from <file> --nonce <int> |
|                                   |  --name <string>``                |
+-----------------------------------+-----------------------------------+

.. _parameters-45:

Parameters
^^^^^^^^^^

-  ``address, a``:``string`` address for client to request (default:
   “127.0.0.1:8027”)
-  ``from``:``string`` key file of the sender
-  ``fee``:``unit64`` transaction fee
-  ``nonce``:``int`` transaction nonce (default: 0)
-  ``name``:``string`` domain or subchain name

.. _returns-45:

Returns
^^^^^^^

TODO

.. _example-45:

Example
^^^^^^^

.. code:: js

   // Request
   TODO

   // Result
   TODO

--------------
