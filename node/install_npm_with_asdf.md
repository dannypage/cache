# Install NPM with ASDF

## Install ASDF as prerequisite

```
$ sudo apt-get update && sudo apt-get upgrade
$ sudo apt-get install -y libssl-dev
$ git clone https://github.com/asdf-vm/asdf.git ~/.asdf --branch v0.7.8
$ vim ~/.bashrc
```
Add the following to Bash:

```
. $HOME/.asdf/asdf.sh
. $HOME/.asdf/completions/asdf.bash
```

## Install NPM via ASDF

```
$ asdf plugin-add nodejs https://github.com/asdf-vm/asdf-nodejs.git
$ bash ~/.asdf/plugins/nodejs/bin/import-release-team-keyring
$ asdf install nodejs latest
$ asdf list nodejs
  >> 14.3.0
$ asdf global nodejs 14.3.0
```
