# Crosschain Technology

With a programming/instructing language geared towards thingies (robots/mobots/IoT _etc._), such as ***Diego***, using _'blockchain technology'_ seems a logical choice. Blockchain redundancy is required for thingies to remember their current (or mission) commands/instructions and also the memory of commands/instructions in the thingy's past.  Remembering interactions from the world and others is an important tenet of learning and building intelligence. The immutability provided by blockchain can be leveraged to build pseudo-psychological conditioning of each robot, which in turn, can be used to develop discrimination and discernment.

However, there are some problems with trying to fit blockchain technology into the application of instructing robots to _do things_. The _proof-of-work_ and _proof_of_stake_ mechanisms are exemplary to act as a deterrent from malicious intent when it comes to ledging financial transactions, but for conversational dialogue amongst robots and humans the '_transactions_' are richer and complex.  Any malicious intent should be detecting counterfeit sources, as with blockchain, but in addition to that an informed validation of the dialogue is by far a better solution to not just forbid the counterfeiter (not let the counterfeiter's chain into the ledger) but to entrap the counterfeiter or teach the counterfeiter the error of their ways.

The idiom 'trust is earned not gained' is never practised with blockchain.  Trust of other parties, either known or a stranger, is given by the authority of the majority of those who hold the distributed ledger, be that in public, private, or hybrid blockchain applications. When blockchain technology is applied to financial transactions, such as cryptocurrencies, the majority of transactions are unrelated party transactions, so 'mining' for chain validity seems the best (or reasonable) approach. If transactions are conversations, as parts of a dialogue, the validity should be the content of the transactions (the conversations) rather than just the validity of the chain.

So what is the alternative to blockchain?  Well lets first simplify matters with an example.

Simply put, blockchain works with a digital ledger shared by everyone. Validation of a chain is agreed upon and added to the blockchain.  In simplified terms the blockchain for three nodes (as a simplified example) can be depicted as follows (_fig. 1_)...

| ![Blockchain Example](https://raw.githubusercontent.com/tavman7/diego.github.io/main/_img/blockchain.jpg "Blockchain Example") |
| :---: |
| *fig. 1: Blockchain Example* |

The digital ledger is, by its nature, decentralised, since every node has a copy (three in this example). Each node can undertaken _proof of work_ in order to validate the transactions and therefore the blockchain. Yet blockchain, in this respect, is a _double-edged sword_. The decentralisation and community validation can be seen as a benefit with blockchain, but transparency is inevitable and redundancy is incurred as the blockchain grows, both are not desirable in most cases.

Transparency could be an issue in cases where blockchain is used, as all transactions are 'transparent' in the blockchain, according to Ali (2021), "_when working in a commercial environment, complete transparency isn’t ideal, as it allows the participants to see what each member is doing in real-time._" In **Diego** system design transparency is ideal, particular in cases of communication relay.

In blockchain redundancy is beneficial since the _proof of work_ takes more _'work'_ making it more difficult for malicious intent. This deterrent is then magnified by each addition to the blockchain.  However, there comes a point when the amount of 'work' surpasses the deterrent and becomes more expensive for nodes to validate the blockchain as the blockchain grows (known as mining).

The mission of **Diego**, as a system, is for thingies (robots, IoT, mobots, etc.) to learn accumulatively as humans have being doing throughout their lives _ _i.e._ learn from a baby → learn through childhood → learn through adolescence → learn through adulthood. So the redundancy that stifles blockchain is something desirable for **Diego**. However, humans do not learn **everything** _in the world_ as they grow up, they learn from their environment, their peers, and their superiors. So we need to change the paradigm of blockchain where validation of transactions (albeit conversations) is not the responsibility of every node.  Adiitionally we should not rely on a digital ledger for every transaction.  This change is what I have termed, 'crosschain', because chains are crossed as they grow.

Firstly in crosschain, transactions are better termed as 'conversations', since we are working with 'communication'. In crosschain every node keeps their own digital ledger, of all the conversations they have made. A conversation is a **Diego** command executed and/or reply to a command from another node.  The depiction used in _fig. 1_ can therefore be modified as in _fig. 2_...

| ![Crosschain Example](https://raw.githubusercontent.com/tavman7/diego.github.io/main/_img/crosschain.jpg "Crosschain Example") |
| :---: |
| *fig. 2: Crosschain Example* |

In _fig. 2_ each of the three nodes has their own ledger of their conversations, depicted, in this example, as their own individual colour. Every conversation recorded in their ledger is a **Diego** command, either a command for itself, a command for a request, or, a command as an acknowledgement.  This can be seen in our example with the 'purple' node who has had no interaction with the other nodes, but has recorded its own commands in its own ledger.

For the other two nodes in _fig. 2_ (mustard and green) have a dialogue between each other. In this case each node still keeps their own ledger but for every conversation between each node they keep a crossed chain of each others conversations. Mustard node keeps records of  its conversations and all conversations of green node (that it hears) as a chain on another chain, and _visa versa_.

All dialogues are possible, for instance, _fig. 3_ depicts the purple node having a one way conversation with the mustard node and the green node...

| ![Dual One-way Dialogue](https://raw.githubusercontent.com/tavman7/diego.github.io/main/_img/dual_oneway_dialogue.jpg "Dual One-way Dialogue") |
| :---: |
| *fig. 2: Dual One-way Dialogue* |

Then _fig. 4_ shows a conversation relayed from mustard node to green node through purple node...

| ![Relayed Dialogue](https://raw.githubusercontent.com/tavman7/diego.github.io/main/_img/realyed_dialogue.jpg "Relayed Dialogue") |
| :---: |
| *fig. 2: Relayed Dialogue* |

The relayed conversation is handled using the `_relay` postposit in **Diego** code. The intended recipient of the conversation, in this example the green node, is referred to in the **Diego** command of the mustard node, usually by addressing the object by moniker, uuid, or other identifier (like `label`s for instance).  The `_relay` postposit provides two functions for the dialogue, first any node picking up the command with the `_relay` postposit (in this case the purple node) will record that command in its own ledger, even if the conversation has nothing to do with them. The purple node knows that the conservation has to be relayed so picks it up. When the callee node (green node) hears the conversation relayed from a node other than the caller (purple node in this example) it will record the conversation in its ledger.  In green's ledger the conservation will have come from purple node, but since the `_relay` postposit exists green node knows the purple node (in this case) is not the originator.  Any reply from the green node will then have the `_relay` postposit, so the conservation can be relayed back.

Validation of the crosschain is identical to the methodology of blockchain.  Even in the relayed example, the chain can be validated back to the originator through the green-purple chain then the purple-mustard chain.

Redundancy is part of each node's learning processes, just as humans, the nodes now have an experience and memory of their interaction with another peer.  Since nodes are robots/IoT, they can be programmed in **Diego** to record (and share) their environments, so just like humans, growing their intelligence of the world around them.

## References

<!--Ali, F 2021, _The top 5 problems with blockchain technology_, viewed 6 September 2021, https://www.makeuseof.com/problems-with-blockchain-technology/ -->

[Ali, Fawad (2021); 'The Top 5 Problems with Blockchain Technology'; MUO, Technology Explained, 16-Jul-2021; (viewed 06-Sep-2021)](https://www.makeuseof.com/problems-with-blockchain-technology/)

[Pratt, Mary K. (2021); 'Top 10 Benefits of Blockchain Technology for Business'; TechTarget, Digital Business Transformation, 02-Jun-2021; (viewed 06-Sep-2021)](https://searchcio.techtarget.com/feature/Top-10-benefits-of-blockchain-technology-for-business})

