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

