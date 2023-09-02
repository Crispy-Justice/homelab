# Base linux install

## Update

```bash
sudo apt update && sudo apt upgrade -y

sudo reboot
```

## Install oh-my-zsh

```bash
sudo apt update
sudo apt install zsh powerline fonts-powerline

# oh-my-zsh install script
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## Install docker

```bash
curl -sSL https://get.docker.com | sh
sudo usermod -aG docker $(whoami)
sudo apt install docker-compose
exit
```

## Setup directories for docker installs

```bash
/docker
├─ stack_1/
│  ├─ docker-compose.yaml
│  └─ appdata/
└─ stack_2/
   ├─ docker-compose.yaml
   └─ appdata/
      ├─ app_1/
      │  └─ data/
      └─ app_2/
         ├─ data/
         └─ config/
```
