# Orca on Ubuntu WSL 

Basically this is for creating images in Plotly. It's absurd the number of libraries it needed that weren't included? The Chromium thing didn't work either. Extremely frustrating. But worth dumping the history just incase I need it. Also probably will not be needed when WSL works with GUI too.

Biggest takeaway, the server needs to be actively running apparently, and maybe that PATH redirect to the shim.

More here: https://github.com/plotly/orca#linux-troubleshooting-headless-server-configuration

```
  255  cd ~/WGU/C744/
  256  pysrc
  257  pip3 install psutil
  258  npm install -g electron@6.1.4 orca
  259  sudo apt install npm
  260  orac
  261  orca
  262  npm install -g electron@6.1.4 orca
  263  asdf plugin-add nodejs https://github.com/asdf-vm/asdf-nodejs.git
  264  sudo apt uninstall npm
  265  sudo apt remove npm
  266  bash ~/.asdf/plugins/nodejs/bin/import-release-team-keyring
  267  asdf install npm latest
  268  sudo apt remove node
  269  sudo apt remove nodejs
  270  asdf install nodejs latest
  271  asdf list nodejs
  272  asdf global nodejs 14.3.0
  273  npm
  274  asdf reshim nodejs
  275  npm
  276  source ~/.bash_profile
  277  npm
  278  npm -v
  279  npm install -g electron@6.1.4 orca
  242  orca
  243  sudo apt-get update
  244  sudo apt-get install libnss3
  245  orca
  246  sudo apt-get install libgdk_pixbuf
  247  sudo apt-get install gdk-pixbuf2
  248  sudo apt-get install libgtk2.0-0
  249  orca
  250  sudo apt-get install libgtk-3
  251  sudo apt-get install libgconf-2-4
  252  sudo apt-get install chromium-browser
  253  orca
  254  sudo apt-get install libgtk-3
  286  xvfb-run -a /home/dpage/.asdf/shims/orca
  287  orca serve
  288  xvfb-run -a /home/dpage/.asdf/shims/orca serve
  289  history
  280  pysrc
  281  jupyter notebook
```
