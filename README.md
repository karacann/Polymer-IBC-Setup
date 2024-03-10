# ![image](https://github.com/karacann/Polymer-IBC-Setup/assets/128327604/de632a49-c50e-4f38-9c31-2dcf7258a5c0)


> Polymer IBC testnet

> Minimum requirements
    CPU	2
    RAM	2+ GB
    Storage	40 GB SSD 
 
> It is a very important project for me and I invite you to participate.

 [Polymer Discord](https://discord.gg/nSUdZ7tg)

```console
sudo apt update -y && sudo apt upgrade -y
sudo apt-get install git -y
sudo apt-get install -y ca-certificates curl gnupg
sudo mkdir -p /etc/apt/keyrings

# We enter in
sudo nano /etc/apt/sources.list.d/nodesource.list
> # deb [signed-by=/etc/apt/keyrings/nodesource.gpg] https://deb.nodesource.com/node_ jammy main

sudo apt update -y && sudo apt upgrade -y
sudo apt-get install -y nodejs
```

```console
# polymer installation
git clone https://github.com/sarox0987/polymerlab-ibc-app-solidity.git
cd polymerlab-ibc-app-solidity

# just and forge installation
curl --proto '=https' --tlsv1.2 -sSf https://just.systems/install.sh | bash -s -- --to /usr/local/bin
curl -L https://foundry.paradigm.xyz | bash
source /root/.bashrc
foundryup
forge build
```

<h1 align="center"> Wallet and API key preparation </h1>

> Create a testnet metamask account for Polymer.

> [from here](https://www.alchemy.com/faucets/optimism-sepolia) optimism - [from here](https://www.alchemy.com/faucets/base-sepolia) base faucet alın.

> Alchemy account [create and](https://dashboard.alchemy.com/apps) Create Optimism Sepolia and Base Sepolia App from the apps section.

<![image](https://github.com/karacann/Polymer-IBC-Setup/assets/128327604/ad5aa5f0-47e7-4337-83b7-fbee1ded4cbc)


```console
# let's get inside
nano .env
```

> `PRIVATE_KEY_1` = Metamask private key

> `OP_ALCHEMY_API_KEY` = Optimism API Key

> `BASE_ALCHEMY_API_KEY` = Base apı Key

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

![image](https://github.com/karacann/Polymer-IBC-Setup/assets/128327604/49339449-3b42-4a66-a4d5-2fd72d922274)


> If it fails, run `npx hardhat clean` and `just do-it` again.

> Send the screenshot to the #proof channel on discord and get the dev role.

