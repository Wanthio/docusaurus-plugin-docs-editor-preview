---
sidebar_position: 4
---

# **Glossary**

**A**

- **Address Checksum:** Checksum validation is a way to determine if an address is valid and does not contain typos. 
- **Adaptive PoW** (In development for IOTA 1.5): With this feature, the coordinator can issue a milestone and simultaneously set the future PoW score. This means that if the network is not fully utilized, the PoW will be reduced to the point where it can be executed by microdevices. Accordingly, the coordinator can also raise the PoW difficulty in case of high utilization and thus make an attack very expensive.
- **Auto peering (IOTA 1.5):** A mechanism that allows nodes to automatically select their neighbors without manual intervention by the node operator. 
- **API interface:** To send data transactions (value 0) and query the tangle. 
- **Atomic Transactions:** Instead of the bundle construct, IOTA 1.5 uses simpler Atomic Transactions. This reduces network overhead and signature verification load, improves spam protection and rate control, and shortens the length of Merkle proofs (for future sharding). It also reduces implementation overhead and increases maintainability of the core node software. 
- **Application Layer (IOTA 2.0):** The top layer of the 3-layer communication protocol. The IOTA protocol allows a variety of external applications to run on the Message Tangle. Anyone can design an application and users can decide which applications to run on their nodes. These applications will all use the communication layer to transmit and store data.
- **Approval Switch (IOTA 2.0):** when a message is selected as a parent, we can choose from the strong or weak tip pool. This mechanism is called Approval Switch.
- **Approval Weight (IOTA 2.0):** A message gets Mana-weight by approving the message directly or indirectly. However, only strong Parents can pass on the mana weight to the past, while weak Parents receive the weight from their weak Children but do not pass it on.
- **Approvers (IOTA 2.0):** Parents are approved by their referencing messages called approvers. It is thus a reverse mapping of parents. As in the parents’ definition, an approver might be either strong or weak.

**B**

- **Balance:** Funds on the addresses (account). These are always available and cannot be deleted or forgotten.
- **Blockchain Bottleneck:** The more transactions are issued, the more the block rate and size becomes a bottleneck in the system. It is no longer possible to capture all incoming transactions in a prompt manner. Attempts to speed up block rates result in more orphaned blocks (blocks are left behind) and reduce the security of the blockchain. 
- **Branch (IOTA 2.0):** A version of the ledger that temporarily coexists with other versions, each spawned by conflicting transactions.
- **Bee (IOTA 2.0):** Production-ready implementation of the core client without coordinator in the Rust programming language. All previous developments and ideas from IRI, Ict, Hornet and Go Shimmer are merged into a unified platform.
- **Bootstrapping attack:** An attack in which a node downloads malicious snapshot files, including invalid transactions and balances.

**C**

- **Curl:** This is the main hash function currently in use. It is based on the “sponge” construction of the Keccak inventors (SHA-3). 
- **Confirmed:** Confirmed transactions. In IOTA 1.0 & 1.5, transactions are still confirmed by the coordinator (milestones). 
- **CTPS:** Confirmed transaction per second.
- **Cumulative Weight:** A system for valuing transactions. Each additional transaction that references a transaction increases its cumulative weight. When tips are selected, a path through transactions that has a higher cumulative weight is preferred.
- **CommNet: **The CommNet is a test-only network and is similar to the DevNet except that it is maintained by the IOTA community. The Hornet nodes (no longer IRI nodes) in the CommNet continue to use a coordinator operated by the IOTA community.
- **Chronicle:** Official permanode solution of the IOTA Foundation. It allows to store all transactions reaching a node in a distributed database that is secure and scales well. Chronicle is used to store the Tangle’s unlimited data flow and make it queryable. In other words, permanence allows the entire history of the Tangle to be stored indefinitely and makes that data easily accessible.
- **Consensus:** Agreement on a specific date or value in distributed multi-agent systems, in the presence of faulty processes. 
- **Coordinator (only up to IOTA 2.0): **A trusted entity, as protection against malicious transactions. The Tangle is not yet a final product, it is still in beta. The network currently relies on a kind of shield, the so-called coordinator called “Compass”. It is open-source and runs on a Hornet node. The COO acts as a centralized, voluntary, and temporary alternative consensus mechanism for the Tangle. To do this, the COO sends honest transactions to the full nodes at regular intervals. These packets contain a signed transaction with no value, called a milestone. The full nodes in the Tangle consider a transaction as confirmed only if it is approved by a milestone. Important: The coordinator can only confirm transactions, but he cannot bypass the consensus rules. To create, freeze or steal tokens is not possible for him. This fixed rule and the COO address is hardcoded on each full node, so the coordinator’s influence on the tangle is very limited, since the tangle is also constantly monitored by all the other full nodes. > The Coo will be switched off with the IOTA 2.0 upgrade.
- **Communication Layer (IOTA 2.0):** This layer stores and communicates information. This layer contains the distributed ledger or tangle. The rate control and timestamps are also located in this layer.
- **Core Object type (IOTA 2.0):** An object type that must be parsed by all nodes. Parsers are computer programs responsible for decomposing and converting an input into a format more suitable for further processing.
- **Core Application (IOTA 2.0): **Core application that must be executed by all nodes, for example the value transfer application.  
- **Child (IOTA 2.0): **A transaction that directly references two others in the Tangle, referred to as parents.

**D**

- **Data:** The tangle is a way of proving the integrity of data (verifiability of completeness and origin) in a trustworthy manner. At present, there are several cryptographic methods that make this possible, but security gaps are repeatedly discovered here, making data vulnerable to manipulation. This is a major problem, especially in cloud computing, where third-party audit tools are sometimes even used (for a fee) to ensure this data integrity. This is exactly where IOTA comes in and offers a relatively easy way to escape this with its protocol and without fees.
- **Data transactions: **These are confirmed directly and are notarized. With the help of “notarization”, it can be proven that an electronic document existed in a certain form at a certain time and has not been changed since its creation. When a notarization is created, a unique hash (fingerprint) of a document is calculated and stored together with a timestamp in the IOTA ledger (tangle) in an immutable manner.
- **Data storage:** Just like the internet, the IOTA protocol does not store data or in other words, the Tangle is not a data storage. If someone wants to store the history of transactions in a decentralized way, they can build a second-layer solution for this themselves or pay third parties for this storage. For the basic layer, IOTA focuses on performance, throughput, and security rather than building a global database.
- **Distributed Ledger Technology (DLT):** This is a database architecture that allows owners of digital assets to transfer and document them from peer to peer. Each transfer in a DLT is stored as a record in a distributed ledger (database). This database is stored in all nodes of a network.
- **DevNet:** The DevNet (developer network) is a pure test network. It is similar to the Main net except that the tokens are free, and it takes less time and computing power to create and send a transaction.
- **Decay: **Both Mana and Pending Mana decay proportionally to its value, preventing Mana from growing indefinitely over time.
- **Double-spending:** Double-spending is a potential flaw in a digital money system where the same single digital token can be spent more than once. Unlike physical money, a digital token consists of a digital file that can be duplicated or counterfeited.
- **dRNG (Decentralized Random Number Generator):** This random number generator is required in Fast Probabilistic Consensus (FPC) to make the consensus model more resilient to attacks. In the case of conflicting transactions, the FPC votes on the transactions in question in several rounds. The threshold at which a node changes its mind in this vote is 50% +/- a small random deviation (using dRNG). In order to avoid stalemate or a specific outcome in the voting, this additional random component prevents potentially malicious nodes from influencing the voting process.
- **Dust Protection (IOTA 1.5):** Someone who wants to harm IOTA could automatically send 1i for years to repeatedly recreated addresses, driving up the ledger’s memory requirements to the point where a full-node would eventually only run on large servers. Some kind of pledge solution will be implemented after the Chrysalis update: Only if the value transfer is less than the equivalent of 0.003 cents must the receiving address be previously charged with a certain minimum balance, otherwise the value transaction will not be accepted. This means that only the one who wants to make microtransactions must “previously” charge the destination address with 1 Ki. So, the first transaction must be a 1 Ki initial transaction for the following microtransactions. This will probably be able to be regulated automatically by the Wallet. Also, the addresses with Colored Coins have to be tokenized. After the Coordicide, there will be another solution for IOTA 2.0.

**E**

- **Eclipse attack: **A cyber-attack that aims to isolate a specific user rather than attack the entire network.
- **Entropy: **In cryptology, this term represents a measure of the “disorder” in texts. Entropy is usually abbreviated with the Greek capital letter Η.
- **ETH Virtual Machine:** A VM is what executes the Smart Contract code so that it runs deterministically. The language in which you run the code provides hooks to access the sandbox on which the VM runs. In the case of IOTA, this is the ISCP sandbox, which only provides access to IOTA tokens, thus consensus also runs on IOTA tokens. It is only the VM that IOTA works with, foreign tokens have nothing to do with a VM running the SC code, not the ETH VM, nor the Cartesi VM.
- **Epoch (IOTA 2.0):** A time interval used for a specific type of consensus mana. At the end of each epoch, a snapshot is taken of the state of mana distribution on the network. Since this tool uses the timestamp of messages, each node can eventually reach a consensus on the mana distribution of an epoch.

**F**

- **Faucet: **A pool of tokens (funds). Upon uncomplicated request, one gets a limited number of tokens for testing, especially for developers of own apps this is a great help.
- **Firefly (IOTA 1.5):** Firefly is a wallet, intended to serve as a platform for the current and future IOTA ecosystem.
- **Finality:** The property that once a transaction has been completed, there is no way to reverse or change it. This is the moment when the parties involved in a transfer can consider the transaction completed. Finality can be deterministic or probabilistic.
- **Full nodes (Hornet, Bee): **They form the core (infrastructure) of the IOTA network. In order to participate in the peer-to-peer network, the full node must always be online and connected to neighbors (other full nodes). In addition, the transaction database must be synchronized with all other full nodes in the network. The role of full nodes is to interact with clients (wallets, DApps, etc.) and attach their transactions to the ledger, make transactions known to all other full nodes in the network, validate transactions and store them in the ledger.
- **Future Cone (IOTA 2.0): **All messages that directly or indirectly reference a message are called its future cone.
- **Fork:** In IT, this is a new development branch after a project is split into a second follow-on project; the source code or parts of it are developed independently of the original parent project.

**G**

- **Genesis transaction: **The Genesis transaction is the first transaction that created all IOTA tokens and distributed them to the addresses of the buyers.
- **GoShimmer (No Main net):** Prototype of Shimmer in the Go programming language. With this node-testing software, consensus is already reached without a coordinator. GoShimmer implements the various modules of Coordicide, such as auto peering, node identities, Mana, etc. GoShimmer serves as a test environment for the first alpha version and the test network. Everything tested here will be gradually merged with Hornet and later implemented in Bee.
- **Generic Data Object (IOTA 2.0):** The most basic object type. All unrecognized data objects are treated this way.

**H**

- **History: **The list of transactions that were directly or indirectly authorized by a particular transaction.
- **Hash values: **Checksums that are applied to the encryption of messages of variable length. Hash values are like fingerprints of a very long data set. Each message is assigned a very specific hash value.
- **Hooks:** An interface that allows foreign program code to be integrated into an existing application to extend it, change its flow, or intercept certain events.
- **Hornet Node (IOTA 1.5):** A completely new implementation of the core client in the Go programming language. The goal is to have a new core client which should contribute massively to the scaling of the network with a significantly increased performance. Hornet will use the architecture and modular concept of GoShimmer and is intended for low-end devices such as a Raspberry Pi. In addition, the coordinator will also run as a plugin via Hornet.

**I**

- **Inclusion state: **Used to determine if a transaction has been accepted and confirmed by the network. Especially for a transaction and a list of tips: Inclusion state is true if the tip refers to this transaction.

**L**

- **Local Snapshots: **Local snapshots are urgently needed to limit the memory requirements of the full nodes to a common size. For this purpose, on the individual nodes old, already confirmed, transactions are deleted from the database. What remains is only a small file (list) with the credits on the respective addresses. full nodes perform the snapshot independently and at their own discretion. This feature allows faster synchronization, lower system resource requirements and no more waiting for global snapshots to clean up the database.
- **Layer:** In DLT a 2nd-layer refers to a secondary framework or protocol built on top of an existing distributed ledger. On these second layers, other applications can be executed without putting too much strain on the base layer. In IOTA, for example, these are the Smart Contracts and IOTA Streams.
- **Local Modifiers:** User-defined conditions that can be considered by nodes during tip selection. In IOTA, nodes do not necessarily have the same view of the tangle. Different types of information that are only available to them locally can be used to strengthen security.
- **Light node:** these are wallets or apps that, unlike full nodes, do not have a full copy of the ledger (Tangle). Therefore, they cannot verify and store transactions. A light node only manages addresses. It can be used to retrieve the ledger’s data, for example, to display credit balances or to start its own transactions and sign them with the private key. These transactions are distributed in the network and verified by the full nodes. If everything is in order, the recipient’s address is linked to the credit and stored in the ledger.

**M**

- **Mining races: **In PoW-based DLTs, the competition between miners for mining rewards and transaction fees is called a mining race. In this race, the fastest and most efficient hardware always wins.
- **Merkle Tree: **A Merkle tree is a data structure used in computer science applications. In cryptocurrencies, Merkle trees are used to encode more efficiently and securely. 
- **Main net: **The public usable IOTA network, in which the IOTA tokens are used that are traded on cryptocurrency exchanges.
- **Milestone (IOTA 1.x): **Milestones are transactions that are signed and issued by the coordinator. Their main goal is to help the Tangle grow healthily and guarantee finality. When milestones directly or indirectly approve a transaction in the Tangle, nodes mark the status of that transaction and its entire history as confirmed.
- **Message (IOTA 2.0):** A message is a core data type that reflects a vertex in the communication layer DAG. It contains the following properties: References to other messages, the sender’s public key, the issuing time of the message, the message sequence number from the node that issued the message, the payload that can be interpreted by higher layers, the nonce that the message uses to satisfy the PoW requirement, a signature that signs all of the above fields. A message is not forwarded until it becomes “solid”, i.e., its history is known to the node. Messages must currently become solid within a 30 second period or they will be discarded. Messages must also meet a PoW requirement, which currently is to find a nonce so that the hash of the message’s fields (minus the signature) has a certain number of leading zeros.
- **Message overhead: **The additional information (metadata) that must be sent along with the actual information (data). This can include signatures, polls and anything that is transmitted over the network but is not the transaction itself.
- **Mana (IOTA 2.0): **When a value transaction is processed, a quantity called Mana will be “pledged” to a specified node ID. This quantity is related to the amount of IOTA moved into the transaction. The only way to gain Mana is to convince some token holder to pledge it to you. In this sense, Mana is Delegated Proof of Token Ownership. Mana, therefore, provides adequate Sybil protection because it is difficult to acquire it in arbitrary amounts.
- **Markers (IOTA 2.0): **A tool that exists only locally and allows certain calculations to be performed more efficiently, such as the calculation of the approval weight or the presence of certain messages in the past or future cone of another message.

**N**

- **Nakamoto Consensus:** Named after the creator of Bitcoin, Satoshi Nakamoto, the Nakamoto Consensus describes the replacement of coordination / communication between known agents with a cryptographic puzzle (Proof-of-Work). Completion of the puzzle determines which agent acts next. 
- **Neighbors:** Network nodes that are directly connected and can exchange messages without intermediate nodes. 
- **Nodes: **A node is any computer that connects to other nodes in the network via software. In principle, they serve as a connection point for data transfers. The Tangle works with different types of nodes, such as full nodes (Hornet, Bee), light nodes (Wallets), permanodes (Chronicle) or smart contract nodes (Wasp). 
- **Network Layer (IOTA 2.0):** This layer manages the lower layers of Internet communication such as TCP. In this layer, the connections between the nodes are managed by the Auto peering and Peer Discovery modules and the Gossip protocol.
- **Network ID: **The network ID enables user-specific subtangles in which nodes can only recognize messages from the network ID listed in their configuration file.

**O**

- **Orphan:** A transaction (or block) that is not referenced by any subsequent transaction (or block). An orphan is not considered confirmed and will not be part of the consensus.
- **Object (IOTA 2.0):** the most basic unit of information in the IOTA protocol. Each object has a type and size and contains data.
- **Oracles:** Oracles are designed to build a secure bridge between the digital and physical worlds in a decentralized, permissionless way. They bring off-chain data to decentralized applications and smart contracts on the IOTA network.
- **OTV (IOTA 2.0):** On Tangle Voting is the internal name for the multiverse described by Hans Moog.
- **OTVFPCS (IOTA 2.0):** On Tangle Voting with FPCS (Fast Probabilistic Consensus on a Set) is a mechanism for breaking metastability, which can be used in addition to OTV (On Tangle Voting). Generally, in IOTA2.0, reaching a high approval weight is the finality criteria. If the approval weight is high enough, the message / transaction is finalized. With OTVFPC the initial opinion is created with OTV, if after some time the opinions of the nodes are still split, for whatever reason, FPC is activated to break this metastable state. The finality of value transactions should be reached faster this way.

**P**

- **Parents (IOTA 2.0): **A message directly references between 1-8 previous messages that we call its parents. A parent can be either strong or weak (see approval switch).
- **Parallel reality ledger state (IOTA 2.0):** This state is used to track conflicts in the tangle. Two new ledger entries that are causally valid but in conflict with each other (ex. Double Spend) are posted into two separate “realities” for this purpose, representing possible but mutually exclusive future ledger states. The consensus mechanism (with FPC, etc.) will now operate until the perception of most nodes’ tilts in one direction and one of the two possible ledger states is accepted as true.
- **Partition Tolerant:** This means that a part of the Tangle can be disconnected from the main tangle for a certain time and continue to run without an Internet connection. These parts can be reconnected to the main Tangle when the Internet connection is restored.
- **Past Cone (IOTA 2.0):** All messages that are directly or indirectly referenced by a message are called its past cone.
- **Parasite Chain Attacks: **A double spending attack on the Tangle. Here, an attacker attempts to reverse a transaction by setting up an alternate Tangle in which the funds were not spent. He then tries to get the majority of the network to accept the alternative Tangle as the legitimate one.
- **Parsing:** Parsers are computer programs responsible for breaking down and converting an input into a format more suitable for further processing.
- **Permanode: **This type of node permanently stores the entire transaction history, possibly with the help of external storage solutions, and possibly only its own transactions (selective permanode).
- **Pending: **A transaction has been seen by the network but not yet confirmed.
- **Peer to Peer Network:** A decentralized network of different network nodes that are connected to each other and exchange data.
- **Peering:** The process of discovering and connecting to other network nodes.
- **Payload (IOTA 2.0):** A field in a message that determines the type. Examples are Value payload (TransactionType type), FPC Opinion payload (StatementType type), dRNG payload (Payload), Salt declaration payload, Generic data payload.
- **Private Tangle:** A private tangle is comparable to a test network under complete control of the operator. This allows companies and developers to test their applications under self-defined environment variables without external influences and protected from prying eyes. There is no interoperability between a private Tangle and the IOTA Tangle. So, sending from one to the other does not work either. Each private Tangle is an independent network with its own nodes, tokens, and coordinator.
- **Proof of Work (PoW):** A time-consuming (expensive) mathematical calculation that uses computational power to prevent spam attacks. It consists of a difficult cryptographic puzzle that is easy to verify.
- **Proof of Inclusion (PoI):** With PoI, one is able to provide evidence that a transaction was indirectly referenced by another transaction without having to present the full chain of actual transactions between the two transactions. This is done by using a sequence of hashes instead of the actual transaction data to prove the inclusion of a transaction (inclusion) in the referenced subtangle.
- **Pruning:** In computer science, this is a term for simplifying, shortening, and optimizing decision trees. In IOTA, this is done by local snapshots on each full node. Old transactions that have already been confirmed are deleted from the database, leaving only a file (list) of credits on each address. 
- **Public & private keys: **These are used in cryptographic systems which use key pairs. There are public keys and private keys which are known only to the owner. The generation of such keys depends on cryptographic algorithms based on mathematical problems to generate one-way functions. Effective security requires keeping the private key (seed) private; the public key (address) can be distributed openly without compromising security.

**R**

- **Rebroadcast: **Repeats the sending of a transaction. While a transaction is being sent to an IOTA node, it may go offline. In this case, the IOTA node may not forward the transactions to its neighbors, and the rest of the network will never see these transactions. As a result, that transaction will never be referenced by the coordinator and thus never confirmed. Resending a bundle means resending the same bundle to an IOTA node. This way you give your transactions another chance to be forwarded to the rest of the network. 
- **Reusable Addresses (IOTA 1.5):** With the implementation of the new signature topic Ed25519 through the IOTA 1.5 Chrysalis upgrade, reusable addresses are supported.
- **Reattachment:** Resending a transaction by re-selecting a tip and referencing newer tips by repeating PoW.

**S**

- **Salt:** In cryptography, salt is a randomly chosen string of characters that is appended to a given plaintext before it is further processed to increase the entropy (disorder) of the input. It is often used for storing and transmitting passwords to increase information security.
- **Sandbox:** An isolated area where programs can be tested.
- **Software as a Service (SaaS):** The SaaS model is a subset of cloud computing. It is based on the principle that the software and IT infrastructure can be operated by an external service provider and rented by the customer as a service.
- **Smart Contract Chain: **Smart contracts are processed via a so-called contract chain, the representation of the contract state. A smart contract writes its state every time it is requested, and a new block is added for each of these state updates. All these updates are collected and confirmed in one block. So, the Chain also contains all the past states. The Chain can contain many Smart Contracts, all working on the same global state of the Chain. From this perspective, the Contract Chain is essentially a blockchain anchored on the Tangle. IOTA Smart Contracts can be considered “classic” Smart Contracts, but with the added feature that you can have multiple such parallel Chains all using the same native IOTA token and trading between them in a trusted manner on the Tangle. This enables trusted interoperability between different applications.
- **Small-world network:** a network in which most nodes can be reached from any other node through a small number of intermediate steps.
- **Solidification time:** The time of solidification when the entire history of a transaction has been received by a node.
- **Splitting Attacks:** An attack in which a malicious node attempts to split the tangle into two branches. As one of the branches grows, the attacker publishes transactions on the other branch to keep both alive. Splitting attacks attempt to slow down the consensus process or perform double spending.
- **Sharding:** IOTA nodes have an upper limit on transactions per second (TPS) they can process. Through a type of database partitioning (breaking a very large database into smaller ones) into more manageable segments (shards), each shard would contain a unique set of account balances and nodes would then be assigned to individual shards to validate transactions. The goal is that by dividing into more manageable segments, it will increase transaction throughput and thus overcome scalability issues.
- **Signatures: **Signatures prove ownership of an address. Clients (Wallets) need this proof before nodes validate a transaction. To prove ownership, input transactions must be signed with the private key used to create the address. A signature is created from both the private key of an address and the bundle hash (IOTA 1.0) of the transaction issued by the address.
- **Solidity (IOTA 2.0):** A message is marked as solid if its entire past cone until the Genesis (or the latest snapshot) is known.
- **Subtangle: **A consistent section of the tangle (i.e., a subset of messages / value objects) such that each contained message / value object also contains its referenced messages / value objects.
- **Streams: **IOTA Streams is a multifunctional second layer data transfer protocol that can be used for various types of data transfer (e.g., streaming data). For example, it allows sensors and other devices to encrypt entire data streams and anchor them in the IOTA Tangle. IOTA’s consensus protocol adds integrity and authenticity to these message streams. Given these characteristics, IOTA Streams fills an important need in industries where integrity, privacy, and immutability collide.
- **Sybil Attack:** An attempt to gain control of a peer-to-peer network by forging multiple false identities. 
- **Snapshot: **A special feature of the Tangle. A snapshot deletes all transactions. Only transactions with a balance > 0 are kept. The metadata such as tags and messages are also deleted. What is left behind is just a list of addresses and balances. After a snapshot, the nodes use this list as “genesis”, a new starting point for the tangle. This reduces the size of the tangle network, allowing IOTA nodes to use less memory. Full nodes perform what are called “Local Snapshots” independently and at their own discretion. This means faster synchronization, lower system resource requirements, and no more waiting for global snapshots to clean up the database. Local snapshots are urgently needed to limit the storage requirements of the full nodes to a common size. By default, nodes store about 30 days of transaction data. This can be changed individually. However, the full node operator must be careful not to snapshot locally too frequently. If they snapshot too quickly, they risk building a subtangle that can fall out of consensus. This would be like a miner in the blockchain that only stores information contained in the last block in the blockchain – it is possible that this block will eventually not become part of the longest chain and this miner will build on an abandoned chain.

**T**

- **Tangle:** The Tangle is the underlying core data structure. In mathematical terms it is a directed acyclic graph (DAG). The Tangle is the distributed ledger of IOTA that stores all transactions. 
- **Tag:** A short message which can be attached to a transfer. It can be searched for in the Tangle. 
- **TPS: **Transaction per second 
- **Ternary system: **A trit (trinary digit) can have exactly three states (3 x 1 = 3): -1, 0 and 1. Three trits result in one tryte (33 = 27) and can thus represent 27 combinations. In IOTA, the letters A-Z (26 pieces) and the number 9 are used for this purpose. 
- **Token:** The digital currency form (cryptocurrency). It is a powerful tool for value transfer between people and machines. Total number: 2,779,530,283,277,761 IOTA. The base units are pi, ti, gi, mi, ki, i 
- **Trinity (IOTA 1.0):** An old wallet. After the update to IOTA 1.5 this wallet has no function anymore.
- **Troika:** A ternary hash function (not in use, ternary vision). 
- **Tip:** A transaction that has not yet been approved. 
- **Tip Selection: **The process of selecting previous transactions to be referenced by a new transaction. In these references, a transaction ties into the existing data structure. IOTA only enforces that a transaction approves up to eight other transactions, the tip selection strategy is left to the user (with a good default provided by IOTA).
- **Tip Transaction:** A solid end transaction that is not yet a parent.
- **Transaction (IOTA 2.0):**[** **](https://iota-beginners-guide.com/future-of-iota/iota-2-0-coordicide/)The payload of a value object. It contains the details of a money transfer.
- **Transaction history: **Please read on here.

**U**

- **UTXO model:** This is a so-called addressing model. UTXO stands for “unspent transaction output”, which simply means that you not only keep track of the credits on the address, but also keep track of where the credits come from and where they are sent when they are spent. Each token on an address is thus uniquely identifiable and each issue names the exact token they want to move. This enables faster and more accurate conflict handling and improves the resilience and security of the protocol.

**V**

- **Value Layer (IOTA 2.0): **The Value layer builds on the Communication layer. It works exclusively with payloads of type Value object. This layer has several tasks: Forming the ledger state, processing, validation and output of transactions, conflict detection, conflict resolution via FPC, forming a DAG from value objects, tip selection (on value object tips).
- **Value Transactions: **Value transactions either withdraw IOTA tokens from an address or deposit them to an address. Nodes must verify these transactions to ensure that the sender actually owns the IOTA tokens and that additional tokens are never generated. To do this, the following checks are performed: All IOTA tokens withdrawn from an address are also deposited into one or more other addresses; the value of each transaction does not exceed the total global supply; signatures are valid.
- **Version Number (IOTA 2.0):** Indicates the correct format of each type.
- **Virtual machine: **The technical software encapsulation of a computer system within an executable computer system.

**W**

- **White-flag approach (IOTA 1.5): **Used to calculate credits. A simpler, conflict-avoiding approach that improves the speed and efficiency of tip selection, eliminates certain attacks, and significantly reduces the need for reattachments.
- **Wasp:** A node for IOTA Smart Contracts.

**Z**

- \


\
