# Agent-billions



### Verify agent Identity 
# Use Codespace click this: ([GitHub Codespaces](https://github.com/codespaces))
- Choose blank


1. Update system & install basics
```
sudo apt update && sudo apt upgrade -y
sudo apt install git -y
sudo apt install nodejs npm -y
```

- install Node 18 using:
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
source ~/.bashrc
nvm install 20
nvm use 20
```
- Check version:
- node -v
- should show v20.x.x

2. Clone the repository
```
cd /workspaces/codespaces-blank
git clone https://github.com/BillionsNetwork/verified-agent-identity
cd verified-agent-identity
```

- install dependencies
```
npm install shell-quote @iden3/js-iden3-auth @0xpolygonid/js-sdk ethers uuid@8.3.2 cross-fetch
```

3. run scripts
```
cd scripts
sed -i 's/const { v7: uuid } = require("uuid");/const { v4: uuid } = require("uuid");/' shared/utils.js
node createNewEthereumIdentity.js
node manualLinkHumanToAgent.js --challenge '{"name":"YourName","description":"Billions AI Agent from Philippines"}'
```
- Edit "YourName"
- CLick the links provided in the console to complete the verification.
<img width="1249" height="75" alt="image" src="https://github.com/user-attachments/assets/c787d1d3-8aeb-4d6d-a8d9-9c96599bdead" />

- Intall skill
```
npx clawhub@latest install verified-agent-identity
```
- Y & enter
```
npx skills add BillionsNetwork/verified-agent-identity
```
- Y & enter


## if you done check you agent did here: https://attestations-explorer.billions.network/
<img width="1912" height="708" alt="image" src="https://github.com/user-attachments/assets/50088f8a-0d6a-48b9-b32c-4cbd56dbdebe" />



<img width="416" height="104" alt="image" src="https://github.com/user-attachments/assets/01a86ed7-6f63-4ceb-b513-c829a4136722" />

# Done










