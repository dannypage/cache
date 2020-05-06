# PowerShell Aliases (And Profile)

_via [Stack Overflow](https://stackoverflow.com/questions/2858484/creating-aliases-in-powershell-for-git-commands)_

Create a PowerShell profile (if you don't already have one):

`New-Item -Type file -Path $PROFILE -Force`

Open it to edit:

`notepad $PROFILE`

Add the following functions and aliases:

```
function Get-GitStatus { & git status $args }
New-Alias -Name s -Value Get-GitStatus
function Set-GitCommit { & git commit -am $args }
New-Alias -Name c -Value Set-GitCommit
```

When you restart your PowerShell session, you should be able to pass arguments to the aliases as well. e.g.:

`c "This is a commit message"`
