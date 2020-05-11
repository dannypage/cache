# Install Ruby with ASDF on Ubuntu


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
