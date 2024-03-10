# ![image](https://github.com/karacann/Polymer-IBC-Setup/assets/128327604/ec1e208a-7390-4c64-8800-dd9b92ecccb7)


> Creating IBC Channel for DEV testnet

> Advisors include Al-Bassam and official partners include Celestia and Polygon
Minimum requirements
CPU	2
RAM	2+ GB
Storage	40 GB SSD

> After completing all the steps, do not forget to enter Discord and take part.


> - [Polymer Discord](https://discord.gg/nSUdZ7tg)

```console
sudo apt update -y && sudo apt upgrade -y
sudo apt-get install git -y
sudo apt-get install -y ca-certificates curl gnupg
sudo mkdir -p /etc/apt/keyrings

# içersine giriyoruz
sudo nano /etc/apt/sources.list.d/nodesource.list
# alttaki komutu içersine girdiğimiz dosyaya yazıyoruz. (# ile deb arasında boşluk bırakın)
#deb [signed-by=/etc/apt/keyrings/nodesource.gpg] https://deb.nodesource.com/node_ jammy main

sudo apt update -y && sudo apt upgrade -y
sudo apt-get install -y nodejs
```

```console
# polymer kurulum
git clone https://github.com/sarox0987/polymerlab-ibc-app-solidity.git
cd polymerlab-ibc-app-solidity

# just  ve forge kurulumu
curl --proto '=https' --tlsv1.2 -sSf https://just.systems/install.sh | bash -s -- --to /usr/local/bin
curl -L https://foundry.paradigm.xyz | bash
source /root/.bashrc
foundryup
forge build
```

<h1 align="center"> Wallet and API key preparation </h1>

> It would be beneficial to create a testnet metamask account for Polymer.

> [From here](https://www.alchemy.com/faucets/optimism-sepolia) optimism - [From here](https://www.alchemy.com/faucets/base-sepolia) Get base and optimism faucet.

> Alchemy account [create and](https://dashboard.alchemy.com/apps) Create Optimism Sepolia and Base Sepolia App from the apps section.

<img width="1222" alt="Ekran Resmi 2024-03-09 22 26 16" src="https://github.com/ruesandora/Polymer/assets/101149671/b0c470c3-89f8-400f-81ec-e143b40d7349">

```console
# Let's enter in
nano .env
```

> `PRIVATE_KEY_1` = Metamask private key

> `OP_ALCHEMY_API_KEY` = Optimism API Key'i 

> `BASE_ALCHEMY_API_KEY` = Base apı Key'i

> It will be inside the quotes, I save and exit with CTRL X enter.

```console
# chanel creation phase
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
source ~/.bashrc
nvm install 18
nvm use 18
npm install
just install
just do-it
```

> You will get logs like below and it will say done.

![image](https://github.com/karacann/Polymer-IBC-Setup/assets/128327604/91b59fb8-69a1-405d-84af-47aa70946bcb)


> If it gives an error, enter this command, `npx hardhat clean` and `just do-it` run again.

> Post the screenshot to the #proof channel and request your role.

