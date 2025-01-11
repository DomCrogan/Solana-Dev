# Solana-Dev
Learning Solana

Day 1

Technical Advantages of Solana:

Faster confirmation times (validated by the entire network in about 400ms, much faster than most other chains).
Low transaction fees (usually about 5000 lamports per signature).
Maintains consensus across 2500+ validators.

Network Overview:

Validator leader receives all transactions throughout the entire chain, packs them into blocks, and these get propagated throughout Solana.
It uses turbine to do this (block propagation portion of the Solana protocol).
All these transactions can get executed in a parallel fashion due to its design.
Every single transaction on Solana is stateless (doesnt maintain its own state/data).
It’s the accounts that store those bits of data (transactions interact with them).
Every single tx is going to read/write to different accounts on Solana, because all of those read and writes get processed differently on the blockchain, it enables them to be really fast confirmation times, and really fast block propagation.
Solana uses Proof of History (PoH)

Programming on Solana:

Accounts are key to Solana.
Basically everything on Solana is an account (sort of like files on an operation system).
Accounts are unique 256-bit addresses.
They all hold some balance of SOL.
They can store arbitrary data in the form of raw bytes.
Data storage is paid with Rent.
Anyone can credit SOL or read data in a permissionless fashion.
Only the account owner can debit SOL or modify data.
Lamports are the smallest unit of value for the SOL token (1 SOL = 1 billion lamports)
<img width="593" alt="image" src="https://github.com/user-attachments/assets/4a56f871-5265-4de5-83f6-db9ab51452e3" />


Programs:

Programs are smart contracts but on Solana
These are special kinds of accounts (is_executable true then its a program, false is data)
Data is eBPF bytecode (Berkley Packet Filter)
Written in Rust, C/C++, Python
Programs are stateless, they can only read and write data to other accounts not their own, this enables programs to be executed in parallel
Must be the owner of an account to modify them
Programs process instructions
Programs can send instructions to other programs


Program Instructions:

<img width="589" alt="image" src="https://github.com/user-attachments/assets/d02bcef8-9bf7-4184-b9e8-a6b26da770a8" />

Solana Transactions:

<img width="594" alt="image" src="https://github.com/user-attachments/assets/f1e51f5d-90cd-4cd7-bfb7-f9e4753055c7" />


Programs are invoked by instructions

Instructions are sent via transactions

Transactions are atomic

Transactions must be signed 



Lifecycle of a Transaction:


<img width="589" alt="image" src="https://github.com/user-attachments/assets/59f382dd-63c8-41e2-8535-a3b64d0ea6c4" />

