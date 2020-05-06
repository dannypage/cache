# How To Run DragonRuby

## General Structure

- `dragonruby <mygame>/app/main.rb` is the main starting point.
- Can put general files in the top of <mygame>. 

## Windows

Add to the profile this alias: 
```
function DragonRuby { & C:\Users\danie\AppData\Roaming\itch\apps\dragonruby-gtk\dragonruby-windows-amd64\dragonruby $args }
New-Alias -Name s -Value Get-GitStatus -Force -Option AllScope
```

Then download files or create any `my_game` style folders anywhere and can run them easily.
