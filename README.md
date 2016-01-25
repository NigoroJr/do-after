# do-after
A simple script for executing a command after another.

## What is this?
"Append" a command after you started executing it.

## Why?
I often find myself wanting to play a music file after one finishes.

```
$ mplayer some_file
# (10 seconds later...)
# Oh wait! I want to play another_file too, but it's too late!
# I'll do some other stuff while some_file is playing.
# (30 minutes later...)
# Why is there no music playing...?
```

But with this script,

```
$ mplayer some_file
# Oh wait!
# (Open another terminal)
$ do-after 12345 mplayer another_file &
$ disown
# (Close terminal)
```

Tested with zsh 5.2.

## zsh completion
Put the `_do_after` file in your `$FPATH`.

## Caveats
This script doesn't look at the exit status of the previous command.

## License
MIT

## Author
Naoki Mizuno
