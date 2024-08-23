# MooV_Blockchain

Bootcamp on Aleo platform using Leo

## Workshop 1
Difficulty Level (Scale of 1 - 3) - 1

<bold>Deployment Link:<bold/> at19hgu9w08zqty6ushevcrs89m78dytsz0p27wxw7xv8kg3ju2uvgqqwrdv7

{ Preview }

<bold>Description with command you used:<bold/>
1st command : leo run main 3u32 2u32 --network testnet
Where main =》transition function name, 3u32 2u32 is the inputs and network is specified testnet

2nd command : leo deploy --network testnet
This is the deployment command.


## Workshop 2
Difficulty Level (Scale of 1 - 3) - 2

<bold>Deployment Link:<bold/> at15svj4aa8q8gvfxdx3xc5m9qkctyavr39n0rem9qnky9s8nz4vygqwmzyv9

{ Preview }

<bold>Description with command you used:<bold/>
1st Command : leo run mint <type_aleo_address> <type_amount>u64 (the leo adress was typed with an amount of 1000)
This command returned two outputs with the first output having an amount of 900 while the second output returned an amount of 100.

2nd command: leo run transfer "<Token_Record>" <to_address> <amount>u64
The generated record from the 1st command is used as the second command's first input and then our 'to address' and amount.

3rd Command : leo deploy --network testnet
This is the deployment command.


## Workshop 3
Difficulty Level (Scale of 1 - 3) - 3

<bold>Deployment Link:<bold/> at1ylh6az26awc9dnwcspxng0dhyw4nvrvgxn7ryf5yreqh0r8gsups8zcs8h

{ Preview }

<bold>Description with command you used:<bold/>
1st command : leo run combine_hash_owner_receiver <type_your_address> <type_friend_address></>
This has only 2 inputs where first input is owner address (self.caller) and second input is the receiver address (the receiver adress must not be the same as the receiver address else and error will be raised.)

2nd command : leo deploy --network testnet
This is the deployment command.
