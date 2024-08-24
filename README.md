# Aleo Bootcamp Documentation: Building and Deploying Aleo Programs

Introduction: This documentation outlines the steps taken during our bootcamp to deploy three different Aleo programs using the Leo Language. The programs demonstrate basic arithmetic operations, token minting and transferring, and a simple voice messaging system using Aleo's privacy-preserving smart contracts. Each section will describe the purpose of the program, the code implementation, and the commands used to deploy each of the programs to the Aleo network with their deployment links for confirmation. The program build was performed off-chain while deployment was done on-chain.

# Aleo
You can check out [Aleo](https://developer.aleo.org/getting_started/) to learn more about it.

Everything about developing with the Aleo network has been documented [here](https://developer.aleo.org/getting_started/)

## Deployment Command
To deploy the below programs to the Aleo network, use the following command: `leo deploy --network testnet`

# Task 1 (Hello world )
## Purpose:
The israel_hello2 program is a simple smart contract that demonstrates how to perform a basic arithmetic operation (addition) using Aleo.

## Functionality:
This program defines a transition function called "main" that takes two public u32 integers, a and b, adds them together, and returns the result as c. With "network" being the specified testnet.

## Program Execution Command
`leo run main 3u32 2u32 --network testnet`

## Deployment Link
[israel_hello2](https://explorer.aleo.org/transaction/at19hgu9w08zqty6ushevcrs89m78dytsz0p27wxw7xv8kg3ju2uvgqqwrdv7)

# Task 2
## Purpose:
The jhonny_token4 program demonstrates a basic example of minting and transferring a token on the Aleo network.

## Functionality:
This program defines a Token record and two transitions: mint and transfer. The mint function creates a new token with a specified amount for an owner, while the transfer function allows the transfer of a specified amount of tokens to another address.

## Program Execution Command
1st Command : `leo run mint <type_aleo_address> <type_amount>u64` 

2nd command: `leo run transfer "<Token_Record>" <to_address> <amount>u64` 

We were able to use the generated record from 1st command to input into the second command's first input and then our *to* address and *amount*.

## Deployment Link
[jhonny_token4](https://explorer.aleo.org/transaction/at15svj4aa8q8gvfxdx3xc5m9qkctyavr39n0rem9qnky9s8nz4vygqwmzyv9)

# Task 3

## Purpose:
The vikings_voice6 program is a more complex example that involves sending voice messages between users on the Aleo network, while ensuring data privacy and integrity, the hallmark of Aleo.

## Functionality:
This program allows users to send and receive voice messages. It uses a hashing mechanism to ensure that the message content and user identities are securely stored and processed on the Aleo blockchain. The program includes functions to send voice messages, update the state on-chain, and combine hash values of the owner and receiver.

## Program Execution Command
`leo run combine_hash_owner_receiver <type_your_address> <type_friend_address>` 

This has only 2 inputs where first input is owner address (self.caller) and second input is the receiver address. The second address must not be the same as the first address.

## Deployment Link
[vikings_voice6](https://explorer.aleo.org/transaction/at1ylh6az26awc9dnwcspxng0dhyw4nvrvgxn7ryf5yreqh0r8gsups8zcs8h)

# Deploy Confirmation
After deployment, you can confirm that the deployment is successful by checking with [Aleo's platform](https://testnet.aleoscan.io/).

# Summary
In this workshop, we successfully wrote and deployed three Aleo programs:

- Arithmetic Operation - A simple program for adding two numbers.
- Token Minting and Transfer - A basic implementation of minting and transferring tokens.
- Voice Messaging System - A complex program that securely communicates voice messages between two different addresses on-chain.
