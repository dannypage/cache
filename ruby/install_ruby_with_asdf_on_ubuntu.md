# Install Ruby with ASDF on Ubuntu

## Pre-req

- Check [ASDF Version](https://asdf-vm.com/#/core-manage-asdf-vm)
- Update everything

```
$ sudo apt-get update && sudo apt-get upgrade
$ sudo apt-get install -y libssl-dev
$ sudo apt-get install -y zlib1g-dev
$ git clone https://github.com/asdf-vm/asdf.git ~/.asdf --branch v0.7.8
$ cd ~/.asdf && git checkout master
$ vim ~/.bash_profile
```

Add the following to Bash:

```
. $HOME/.asdf/asdf.sh
. $HOME/.asdf/completions/asdf.bash
```

## Install Ruby

```
$ source ~/.bashrc
$ asdf plugin-add ruby https://github.com/asdf-vm/asdf-ruby.git
$ asdf install ruby latest
$ asdf global ruby 2.7.1
```

If you need a local Ruby to a set of folders:

```
$ asdf install ruby 2.6.6
$ asdf local ruby 2.6.6
```
