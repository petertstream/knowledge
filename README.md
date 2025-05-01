# .knowledge
Collection of things that are good to know

# SteamDeck
## Set SteamDeck to NOT read-only so you can install packages with pacman, e.g. like pip etc.
1. set a password for your admin user (link description here later, TODO)
2. sudo steamos-readonly disable
3. sudo pacman-key --init
4. sudo pacman-key --populate archlinux
5. sudo pacman-key --populate archlinux holo

Now you can install packages with pacman.

## Install pip with pacman
1. sudo pacman -S python-pip
  But that's not enough, you need to install pipx 
2. sudo pacman -S python-pipx

## Install sth with pipx (e.g. uv)
1. pipx install uv

