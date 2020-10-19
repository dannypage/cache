# Better Git Diff

> Thankfully, it’s not only possible to configure a custom regex specific to your language to help Git better orient itself, there’s even a pre-defined set of patterns for many languages and formats right there in Git. All we have to do is tell Git which patterns to use for our file extensions.

Add the following to ~/.gitattributes
```
*.py    diff=python
*.rb    diff=ruby
*.rake  diff=ruby
```

If not already set, you can make it the global default for all git repos on the system.

```
$ git config --global core.attributesfile ~/.gitattributes
```

Thanks to @tekin on Twitter for this tidbit. https://tekin.co.uk/2020/10/better-git-diff-output-for-ruby-python-elixir-and-more
