# Install Ruby on Mac with ASDF

```
$ brew install coreutils curl git
$ brew install asdf
$ echo -e "\n. $(brew --prefix asdf)/asdf.sh" >> ~/.zprofile

$ asdf plugin-add ruby https://github.com/asdf-vm/asdf-ruby.git
$ asdf install ruby latest
$ asdf global ruby 3.0.0
```
