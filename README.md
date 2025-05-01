# .knowledge
Collection of things that are good to know

# SteamDeck
## Set SteamDeck to NOT read-only so you can install packages with pacman, e.g. like pip etc.
1. set a password for your admin user if not already done
   -> passwd
3. sudo steamos-readonly disable
4. sudo pacman-key --init
5. sudo pacman-key --populate archlinux
6. sudo pacman-key --populate archlinux holo

Now you can install packages with pacman.

## Be careful
rootfs is not large on SteamDeck. Installing packages etc. might fill the drive.
Also, when packages cannot be installed, check if there is a message "not enough space on hard drive" or similar.

## Install pip with pacman
1. sudo pacman -S python-pip
  But that's not enough, you need to install pipx 
2. sudo pacman -S python-pipx

## Install sth with pipx (e.g. uv)
1. pipx install uv

## Installing ollama on steam deck
rootfs gets bloated when you install ollama directly (see above).
What I did:
1. Created a folder "AI"
2. cd AI
3. Downloaded ollama version to this folder -> curl -L https://ollama.com/download/ollama-linux-amd64.tgz -o ollama-linux-amd64.tgz
4. Unpack tar in this folder -> tar -xzf ollama-linux-amd64.tgz
5. I get a "bin" and "lib" folder
6. Downloaded ollama rocm version to this folder -> curl -L https://ollama.com/download/ollama-linux-amd64-rocm.tgz -o ollama-linux-amd64-rocm.tgz
7. Unpack tar in this folder -> tar -xzf ollama-linux-amd64-rocm.tgz
8. It updates the "lib" folder
