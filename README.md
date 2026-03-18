# Agent-billions



### Verify agent Identity (Codespaces)

1. Update system & install basics
```
sudo apt update && sudo apt upgrade -y
sudo apt install git -y
sudo apt install nodejs npm -y
```

- check v. 
```node -v```
👉 It should be v18 or higher

❌ If it's lower, install Node 18 using:
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
source ~/.bashrc
nvm install 18
nvm use 18
```

2. Clone the repository
```
git clone https://github.com/BillionsNetwork/verified-agent-identity
cd verified-agent-identity
```

- install dependencies
```npm install shell-quote @iden3/js-iden3-auth @0xpolygonid/js-sdk ethers uuid cross-fetch```

3. run scripts
```
cd scripts
node createNewEthereumIdentity.js
node manualLinkHumanToAgent.js --challenge '{"name":"YourName","description":"Billions AI Agent from Philippines"}'
```
- Edit "YourName"

<img width="416" height="104" alt="image" src="https://github.com/user-attachments/assets/01a86ed7-6f63-4ceb-b513-c829a4136722" />

# Done






