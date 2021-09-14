# Blockchain, Ethereum, Smart contracts, Solidity

In October 2008, coinciding with the economic crisis of that year, it was
published an article titled ["Bitcoin: A Peer-to-peer Electronic Cash System"](https://bitcoin.org/bitcoin.pdf)
in which the author, who signed as [Satoshi Nakamoto](https://en.wikipedia.org/wiki/Satoshi_Nakamoto), 
describes a system called Bitcoin that allows people to exchange electronic 
currency with each other, this is in a peer-to-peer (P2P) mode, without the need 
for a central intermediary authority or bank.

![Satochi Paper](../figures/bitcoin_paper.png)

One of the central ideas of the Bitcoin P2P system was to use a chain
of blocks (or blockchain) to store the monetary operations carried out
by stakeholders of the system. Initially, blockchain was conceived
as the tool that made the Bitcoin network possible by holding its operations.

![Blockchain](../figures/blockchain.jpeg)

## Ethereum

As time went by, Bitcoin enthusiasts realized that innovations technologies 
proposed by Satoshi could serve to support not only the operation of a P2P network 
of financial transfers but also to support the operation of much more complex 
applications.

One of these people was [Vitalik Buterin](https://en.wikipedia.org/wiki/Vitalik_Buterin), 
who in 2013 presented some ideas of a programable general-purpose blockchain 
through which developers could build decentralized applications abstracting them 
from the implementation details of the P2P network, the blockchain, and consensus 
algorithms.

Vitalik, together with [Gavin Wood](https://en.wikipedia.org/wiki/Gavin_Wood) were 
polishing these incipient ideas for years until July 2015, when the first block 
of the Ethereum blockchain was mined starting its operation.

### Main components

- **P2P Network**: Ethereum runs on the Ethereum's main network (Mainnet) following 
the *DEVp2p* protocol. In addition to the mainnet, there are alternative Ethereum 
networks like Rinkeby or Ropsten;
- **Consensus rules**: defined in the [Yellow Paper](https://ethereum.github.io/yellowpaper/paper.pdf) 
of Ethereum;
- **Transactions**: these are the network messages that include, among other things, 
sender, recipient, value, payload data;
- **State machine**: State transitions in Ethereum are processed by the Ethereum 
virtual machine([EVM](https://ethereum.org/en/developers/docs/evm/)). EVM programs 
are called smart contracts, which are written in high-level languages, like Solidity, 
and later compiled into bytecode;
- **Data structures**: the state of the Ethereum network is stored in key-value databases 
(e.g., [LevelDB](https://en.wikipedia.org/wiki/LevelDB])) after it has been serialized
using a format called  [Merkle Patricia Trie](https://easythereentropy.wordpress.com/2014/06/04/understanding-the-ethereum-trie/);
- **Consensus algorithms**: from its origins, Ethereum used the consensus 
algorithm [Proof-of-Work (PoW)](https://ethereum.org/en/developers/docs/consensus-mechanisms/pow/), 
employed by Bitcoin, to verify transactions. There is currently a migration process 
underway to a new and more efficient consensus algorithm called [Proof-of-Stake (PoS)](https://ethereum.org/en/developers/docs/consensus-mechanisms/pos/);
- **Clients**: software applications that implement the specifications of Ethereum 
and allows communication through the P2P network with other clients of Ethereum.

### Ethers and Wallets

The currency in Ethereum is *ether*. To interact with the Ethereum network, you 
need an account with ethers. These ethers are stored in `wallets`, which are 
software applications that help manage an Ethereum account.

There are a wide variety of wallets, web-based, desktop, mobile, and even physical 
devices called `cold wallets`. [Metamask] (https://metamask.io) is a widely used 
wallet for its ease of use and convenience. [Here](https://github.com/ethereumbook/ethereumbook/blob/develop/02intro.asciidoc#getting-started-with-metamask) 
it is explained how to create a `wallet` in Metamask and add test ethers.

![Blockchain](../figures/metamask.png)

### Smart contracts and Solidity

Computer programs running on the Ethereum network in the context of the EVM are 
called *smart contracts*. Smart contracts are written in high-level programming 
languages and then compiled into machine code. One of these languages, and perhaps 
the most widely used, is [Solidity] (https://docs.soliditylang.org/en/latest/), 
created by Gavin Wood, one of the Ethereum co-creator.

Solidity is an imperative [open source](https://github.com/ethereum/solidity) 
programming language with a syntax similar to the Java language. Below you can 
see an example taken from the Ethereum documentation.

```Solidity
// SPDX-License-Identifier: GPL-3.0
pragma solidity >= 0.7.0;

contract Coin {
    // The keyword "public" makes variables
    // accessible from other contracts
    address public minter;
    mapping (address => uint) public balances;

    // Events allow clients to react to specific
    // contract changes you declare
    event Sent(address from, address to, uint amount);

    // Constructor code is only run when the contract
    // is created
    constructor() {
        minter = msg.sender;
    }

    // Sends an amount of newly created coins to an address
    // Can only be called by the contract creator
    function mint(address receiver, uint amount) public {
        require(msg.sender == minter);
        require(amount < 1e60);
        balances[receiver] += amount;
    }

    // Sends an amount of existing coins
    // from any caller to an address
    function send(address receiver, uint amount) public {
        require(amount <= balances[msg.sender], "Insufficient balance.");
        balances[msg.sender] -= amount;
        balances[receiver] += amount;
        emit Sent(msg.sender, receiver, amount);
    }
}
```

For more information on Solidity, consult the tutorials and documentation in 
the [materials] (../ materials) directory of this repository.

## Referencias

- [Ethereum Development Documentation](https://ethereum.org/en/developers/docs/)

- [Mastering Ethererum: Building smart contracts and dapps](https://github.com/ethereumbook/ethereumbook)

- [Ethereum and Solidity: The complete developer guide](https://www.udemy.com/course/ethereum-and-solidity-the-complete-developers-guide)

