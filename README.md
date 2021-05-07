# ~/.dotfiles

Backup, restore, and sync my preferences and settings while sharing what I have so someone else can learn from this code or teach me where I could improve.

To get more in depth with this idea have a look at [this unofficial guide to dotfiles on GitHub](https://dotfiles.github.io).

## Install

```
# Remove previous .dotfiles, if exists
rm -rf ~/.dotfiles

# Clone this repository
git clone https://github.com/sheldonled/dotfiles.git ~/.dotfiles

# Clone any other sub config, or internall setup into the subconfig folder
git clone https://path/to/git/subsetup.git ~/.dotfiles/subconfig/subsetup

# Make files executable
chmod -R +x ~/.dotfiles

# Install
~/.dotfiles/install
```

## What this will do

There are 2 configurations, one for Mac OS and another for Debian-based linux (I use Ubuntu most of the times).

The Linux logic might be broken. It's using my previous setup and the update is pending.

The install script, located at `~/.dotfiles/install` will check if you're using Linux or Mac, then invoke the correct installers.

### Mac OS
The  `~/.dotfiles/install` will run each installer located at  `~/.dotfiles/installers/macos`. They will:

* Install `powerline` fonts, they're used on my iTerm setup
* Copy configuration files (like `zshrc` or `Brewfile`) to my home directory
* Install [Homebrew](https://brew.sh)
* Install iTerm theme (I use [Cobalt2](https://github.com/wesbos/Cobalt2-iterm)) and some zsh plugins
* Create `~/.ssh` folder if it doesn't exist. Create auth keys if doesn't exist, copy my default ssh config file
* Run any subconfiguration setup if there's any. I use this for company-specific stuff, or if I'm doing something privately
* Setup some sudo configs (e.g. use fingerprint when executing sudo instead of typing password)
* Setup dozens of preferences on Mac

### Linux
//TODO
