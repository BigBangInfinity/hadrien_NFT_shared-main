Clone three repos to these folders:

```
C:\> git clone https://github.com/BigBangInfinity/hadrien_NFT_shared-backend-my-api
C:\> git clone https://github.com/BigBangInfinity/hadrien_NFT_shared-contract
C:\> git clone https://github.com/BigBangInfinity/hadrien_NFT_shared-scaffold-eth-2
```

npm/yarn install in these folders

use npm for hadrien_NFT_shared-contract and yarn for others (as we did in class).

```
C:\hadrien_NFT_shared-backend-my-api> yarn install
C:\hadrien_NFT_shared-contract> npm install
C:\hadrien_NFT_shared-scaffold-eth-2> yarn install
```

Compile contract
```
C:\ballot_shared-ballotcontract>npx hardhat compile 
```

Deploy token contract
```
C:\ballot_shared-ballotcontract>npx ts-node .\scripts\deployMyNFT.ts
```

token contract deployed at 0x3329d1c289A7c7F149a7C9fe15704cfcC876A4B6

Verify on etherscan:

```
C:\ballot_shared-ballotcontract>npx hardhat verify --network sepolia 0x3329d1c289A7c7F149a7C9fe15704cfcC876A4B6
```


in C:\ballot_shared-backend-my-api\.env, update token address:
NFT_ADDRESS="0x3329d1c289A7c7F149a7C9fe15704cfcC876A4B6"


```
C:\ballot_shared-backend-my-api>yarn run start:dev
```      

Launches Swagger API on 
http://localhost:3001/api

```
C:\ballot_shared-scaffold-eth-2>yarn start
```

Launches Scaffold ETH on 
http://localhost:3000

Mint NFT on the frontend

![image](https://github.com/BigBangInfinity/hadrien_NFT_shared-main/assets/37957341/e628fbff-6ba2-43bd-9fae-5d352f5099e4)
