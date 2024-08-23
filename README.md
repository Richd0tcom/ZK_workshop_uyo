# ZK_workshop_uyo


This Repository contains the projects/programs built and deployed during our workshop. They include basic arithmetic operations, token minting and transferring, and a simple voice messaging system using Aleo's Zero knowledge circuits. 

### Deployment
To deploy the below programs to the Aleo network, use the following command: `leo deploy --network`
N/B if you forked or cloned the `mainet` build for Leo, add the `--testnet` flag while running the above command


## Project 1 (Hello world)

The rich_first program is a simple ZK circuit that demonstrates how to perform a basic arithmetic operation (addition) using leo.

This program defines a main function that takes two public u32 integers, a and b, adds them together, and returns the result as c.

### execution
`leo run main 3u32 2u32`



### Deployment Link 
https://explorer.aleo.org/transaction/at1nxy9hl2jf5d9dgk9j3cp9hejt2qe2e8t7lvajwaplpzzeh9fuqzq7amhe0



## Project 2 (token minting and transfer)

The token_21969 program demonstrates a basic example of minting and transferring a token on the Aleo network.


This program defines a Token record and two transitions: mint and transfer. The mint function creates a new token with a specified amount for an owner, while the transfer function allows the transfer of a specified amount of tokens to another address. These are all off-chain executions.

### execution
Run this commands in order
`leo run mint <your_aleo_address> <amount>u64`


`leo run transfer "<Token_Record>" <receiver_address> <amount>u64`



### Deployment Link 
https://explorer.aleo.org/transaction/at1t94t949z389dpqmyje9t9m6y9wkw5zgewp7vn7eqerhn957305qs08r9rn



## Project 3 (voice message)

The  program involves sending voice messages between users on the Aleo network using ZK circuits

It allows users to send and receive voice messages. It uses a hashing mechanism to ensure that the message content and user identities are securely stored and processed on the Aleo blockchain. 


`leo run combine_hash_owner_receiver <owner address> <receiver address>`
This has only 2 inputs where first input is owner address (self.caller) and second input is the  receiver address



### Deployment Link 
https://explorer.aleo.org/transaction/at1dju3vrygj5h3mtwp3q002rf5qnk0daz958e4fgmtefx3kh97juysylr7ez

