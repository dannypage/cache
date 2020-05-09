# Installing Jupyter
## Ubuntu via Python3

Install Jupyter to your system:
```
pip3 install jupyterlab
pip3 install notebook
vim ~/.bash_profile
```

In the Bash Profile: add `export PATH=$PATH:~/.local/bin` [^1]

Finally:
```
source ~/.bash_profile
jupyter notebook
```

It'll open a server that you can hit via browser.

[^1] [Jupyter Command Not Found](https://stackoverflow.com/questions/35313876/after-installing-with-pip-jupyter-command-not-found/59571314#59571314)
