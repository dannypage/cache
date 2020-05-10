# Copy Without Indent

Every time I copy into VIM it indents if more than one line is involved.
`:set paste`

You can turn it off with: 
`:set nopaste`

Or if doing it enough, place this in the `.vimrc` and have it always available:

`set pastetoggle=<F3>`

Credit: https://stackoverflow.com/a/2514520
