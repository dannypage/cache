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

## Install NodeJS via ASDF

```
$ asdf plugin-add nodejs https://github.com/asdf-vm/asdf-nodejs.git
$ bash ~/.asdf/plugins/nodejs/bin/import-release-team-keyring
$ asdf install nodejs latest
$ asdf list nodejs
  >> 14.3.0
$ asdf global nodejs 14.3.0
```

Make sure NPM works:

```
$ npm
>> /usr/bin/npm: No such file or directory
$ source ~/.bash_profile
$ npm
>> <works>
```

Probably needed to refresh the entire PATH.
