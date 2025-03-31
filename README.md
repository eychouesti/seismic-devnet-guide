![image](https://github.com/user-attachments/assets/e8c83ea9-d5c9-4f5a-af6d-1237c2c2309d)

# **Welcome to the devnet guide for Seismic** #

As a minimum specification, it is recommended that you do it with a more up-to-date CPU and a minimum of 8GB.

### In this guide, we will complete the following two steps in order. In the first step, we will deploy a contract. In the second step, we will interact with the deployed contract. ###

 - Installing WSL

-  Update WSL

 - Installing Rust

- Installing sfoundryup

- Run sfoundryup

- Cloning repository

- Deploying your first contract

### Interact with deployed contract ###

- Install Bun

- Install node dependencies

- Interact with contract






If you're using Windows, you need to install WSL or rent a Linux server.

There are two options for installing WSL. First, you can search for the latest Ubuntu on the Microsoft Store and install it on your computer or you can open CMD and install it manually




## **Installing WSL**

```bash
wsl --install
```

After WSL is successfully installed on your computer  we need set a username and password. 



## **Installing latest update for WSL**

```bash
sudo apt update && sudo apt upgrade -y
```



## **Installing RUST**

```bash
curl https://sh.rustup.rs -sSf | sh
```
![Screenshot 2025-03-31 172701](https://github.com/user-attachments/assets/c37fe90c-252c-4124-853e-bc4183544357)



In this section  only press *Enter*




*If the installation is completed successfully, you will encounter this screen.*


![Screenshot 2025-03-31 164232](https://github.com/user-attachments/assets/42d2d303-bace-426d-9008-c143d8552961)

After the installation is complete, copy the code below, paste it, and press Enter

```bash
. "$HOME/.cargo/env"
```




## **Install sfoundryup**

```bash
curl -L \
     -H "Accept: application/vnd.github.v3.raw" \
     "https://api.github.com/repos/SeismicSystems/seismic-foundry/contents/sfoundryup/install?ref=seismic" | bash
source ~/.bashrc
```

![image](https://github.com/user-attachments/assets/663c29f4-56fe-4421-819c-7f98890c2d7e)

After the installation is complete, open a new tab for WSL and proceed to the next step

At this stage, we run sfoundryup

## **Run sfoundryup**

```bash
sfoundryup 
```

*Attention, the duration of this step depends on your computer's specifications and may take some time.*



## **Clone repository**

```bash
git clone --recurse-submodules https://github.com/SeismicSystems/try-devnet.git
```

*We are navigating into the cloned repository*

```bash
cd try-devnet/packages/contract/
```

![Screenshot 2025-03-31 165858](https://github.com/user-attachments/assets/4b3a1918-d127-4c7b-9f0a-654ae712ddcb)



## **Deploy contract**
 


```bash
bash script/deploy.sh
```



![image](https://github.com/user-attachments/assets/f0eec8ae-fb18-49d8-9668-4f6e67bd08dd)


After logging into the site, we paste the address provided on the screen and get the faucet. After receiving the faucet, we press the Enter key on the screen

for faucet - https://faucet-2.seismicdev.net/



# Congratulations! After completing all the steps correctly, you have deployed your first contract on Seismic #

![image](https://github.com/user-attachments/assets/474a600d-0c37-489a-9a21-3b80834738d3)



# ** Step 2: Interact with deployed contract** #

## Install Bun ##

```bash
curl -fsSL https://bun.sh/install | bash
```
![image](https://github.com/user-attachments/assets/8365b83a-68f7-45ae-9551-ca1b4de495ae)

## Install node dependencies ##

1. 

```bash
cd try-devnet/packages/cli/
```

2. 

```bash
bun install
```
![image](https://github.com/user-attachments/assets/43f901b6-bad2-4959-a12c-9990b70edb80)


## Final: Interact with deployed contract ##


```bash
bash script/transact.sh
```

We get the faucet for our address from the faucet site.
We press the enter key after taking the faucet.

![image](https://github.com/user-attachments/assets/48b7470d-b2e7-47f6-ac80-57fd9f47e044)

# Congratulations! You have successfully completed all the steps. #

