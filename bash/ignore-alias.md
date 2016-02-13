### Ignore Alias

You can run a command ignoring bash aliases by prepending the command with a `\`.

Why do this? Well, if you've aliased `ls` to `ls -GFh`, but you want to do a one-off `for i in $(ls)` command and don't want to worry about filenames formatted by the `-F` flag, you can do `for i in $(\ls)` instead.
