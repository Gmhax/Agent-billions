# Agent-billions



### Verify agent Identity ([GitHub Codespaces](https://github.com/codespaces))


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
node createNewEthereumIdentity.js
node manualLinkHumanToAgent.js --challenge '{"name":"YourName","description":"Billions AI Agent from Philippines"}'
```
- Edit "YourName"
- Follow any links provided in the console to complete the verification.
<img width="1249" height="75" alt="image" src="https://github.com/user-attachments/assets/c787d1d3-8aeb-4d6d-a8d9-9c96599bdead" />


<img width="416" height="104" alt="image" src="https://github.com/user-attachments/assets/01a86ed7-6f63-4ceb-b513-c829a4136722" />

# Done



# NOTE if you encounter UUID error follow this guide.
## Fix UUID version in script

- This avoids the “uuid is not a function” error:
```
cd scripts
sed -i 's/const { v7: uuid } = require("uuid");/const { v4: uuid } = require("uuid");/' shared/utils.js
```

- Execute the Script follow step 3. 







