~/.dotfiles
========

This is a very draft project that aim to hold my environment setup. The main idea is to backup, restore, and sync my prefs and settings and in the meantime share what I have so someone else can learn or teach me where I could improve.

To get more in deep with the idea please visit [this unofficial guide to dotfiles on GitHub](https://dotfiles.github.io).

This was inspired by [Kassio's](https://github.com/kassio/dotfiles) [.dotfiles project.](https://github.com/kassio/dotfiles)

Install
-------

      #Remove previous .dotfiles, if exists
      rm -rf ~/.dotfiles

      #Clone this repository
      git clone https://github.com/sheldonled/dotfiles.git ~/.dotfiles

      #Clone any other sub config, or internall setup into the subconfig folder
      git clone https://path/to/git/subsetup.git ~/.dotfiles/subconfig/subsetup

      #Make files executable
      chmod -R +x ~/.dotfiles

      #Install
      ~/.dotfiles/install/setup