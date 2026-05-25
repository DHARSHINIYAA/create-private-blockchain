# EXP - CREATE-PRIVATE-BLOCK-CHAIN

# AIM 
To create a Private Blockchain and to add nodes, create accounts, transfer Ether into it by creating and deploying Smart contract.

# PROCEDURE

1.Go to https //geth.ethereum.org/ and download the software for windows. While installing select both geth and development tools. 
2.To check whether the geth is installed ,run “geth” command in your command prompt. 
3.To create a Private Blockchain , we must create a genesis block. 
In your command prompt, create a directory go-ethereum. 
4.Create two nodes inside go-ethereum. 
5.Open vs code using “code .” 

<img width="940" height="435" alt="image" src="https://github.com/user-attachments/assets/eb4c894b-338d-43bf-a8de-b3de3b8d2487" />


## To create account for two nodes 
6.Open terminal in vs code and change directory to node1.

<img width="704" height="75" alt="image" src="https://github.com/user-attachments/assets/c63d4fc8-2f67-4afe-8647-edf36008b766" />

Save the public address and password of node1 in info.txt. 


7.Repeat the same procedures for node2

<img width="664" height="111" alt="image" src="https://github.com/user-attachments/assets/b420fb61-85bf-4196-9438-5476a2653517" />

Save the public address and password of node2 in info.txt. 



## To create a genesis block  
8.Create a file named “privateblock.json” inside go-ethereum. 
Replace {Chain id } with your own chain id and check whether it exists or not using https //chainlist.org/ 
Replace initial signer address and firstnode address with node1 address saved in info.txt. 
and second node with node2 address saved in info.txt  Then replace balance as “3000000000000000000” for both nodes. 


## To configure both nodes using genesis block  
9.change directory to node1 in terminal and run this command. 

<img width="623" height="34" alt="image" src="https://github.com/user-attachments/assets/b088db06-1d0e-4667-889a-31cfa0af5550" />


10.Split terminal and cd to node2 and run the same.

11. Again split terminal and create bootnode.

<img width="632" height="69" alt="image" src="https://github.com/user-attachments/assets/59ef1ced-672d-43cc-98fa-5196f1956478" />

13. To generate key

<img width="784" height="72" alt="image" src="https://github.com/user-attachments/assets/1031854b-6715-4f99-bc30-10fb1edb0a20" />

14. save the enode value in info.txt. 
15. Run node1 and node2
    
Replace Node1 address in {signer address} and {address node1} and enode value with {your value} 
{Network id} is your chain id given in privateblock.json.
Create password.txt undernode1 and node2 and enter the password in it. 
Replace password.txt with { PASSWORD_FILE_NAME_EXTENSION }. 

```

geth --datadir "./data"  --port 30304 --bootnodes enode://3b09d8ea1e557f33fa765193829ea7527851fcaa89565d2c3d3d745c1cfb092accbdde62e4dc84e61c58433ad7a3a720322211de0d46d2e5657646ff500d6bdd@127.0.0.1:0?discport=30301 --authrpc.port 8547 --ipcdisable --allow-insecure-unlock  --http --http.corsdomain="https://remix.ethereum.org" --http.api web3,eth,debug,personal,net --networkid 12345678 --unlock 0x8BBe81A05CB440F79Bd395191C35a9d9f892bB57 --password "./password.txt"  --mine --miner.etherbase=0x8BBe81A05CB440F79Bd395191C35a9d9f892bB57
```

```
geth --datadir "./data"  --port 30306 --bootnodes enode://3b09d8ea1e557f33fa765193829ea7527851fcaa89565d2c3d3d745c1cfb092accbdde62e4dc84e61c58433ad7a3a720322211de0d46d2e5657646ff500d6bdd@127.0.0.1:0?discport=30301  -authrpc.port 8546 --networkid 12345678 --unlock 0x1207323Ca7217e0A21a35B9Dbf26180FD1320E3A --password password.txt
```

15.Go to https //remix.ethereum.org/  and in left pane click deploy and run transactions icon. 
16.Change the environment to Custom-External HTTP Provider 
17.Click on file and under contract, create new file named “New.sol” 
18.Save the file and go to deploy tab and click deploy. 
19.Node1 has deployed and added to blockchain. 


# PROGRAM

<img width="1650" height="756" alt="Screenshot 2026-05-25 070408" src="https://github.com/user-attachments/assets/f1daf8c3-bfa1-4553-bb0c-3eaf5a27c72c" />

### Smart Contract  New.sol 
<img width="1919" height="1014" alt="image" src="https://github.com/user-attachments/assets/e1150e09-513c-49b2-a842-ba46c6fae350" />

# OUTPUT
<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/bd00f37c-d341-47b2-bdc1-c9914ea19182" />

# RESULT 
Thus, the Private Blockchain is created, nodes are added with accounts, and Ether is transferred into it by creating and deploying Smart contract successfully. 
