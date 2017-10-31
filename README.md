# Dotfiles

My custom Linux config files (aka dotfiles).

**Environment:**
- Linux: Debian & Ubuntu
- Shell: Bash

## Install

Run this:

```sh

git clone https://github.com/tbaecker/dotfiles ~/.dotfiles
~/.dotfiles/script/bootstrap
```

This will symlink the appropriate files in `.dotfiles` to your home directory.
Everything is configured and tweaked within `~/.dotfiles`.

`dotfiles` is a simple script that shall help to keep the environment up to date.
You can find this script in `bin/`.

## Topical

Everything's built around topic areas. If you're adding a new area to your
forked dotfiles — say, "Java" — you can simply add a `java` directory and put
files in there. Anything with an extension of `.bash` will get automatically
included into your shell. Anything with an extension of `.symlink` will get
symlinked without extension into `$HOME` when you run `script/bootstrap`.

## Components

There's a few special files in the hierarchy:

- **bin/**: Anything in `bin/` will get added to your `$PATH` and be made
  available everywhere.
- **topic/\*.symlink**: Any files ending in `*.symlink` get symlinked into
  your `$HOME`. This is so you can keep all of those versioned in your dotfiles
  but still keep those autoloaded files in your home directory. These get
  symlinked in when you run `script/bootstrap`.
- **topic/install.sh**: Any file named install.sh is executed when you run `script/install`

## Credits

While trying to get my dotfiles organized, https://dotfiles.github.io/ was
really helpful to get me started.

From there I explored the plethora of dotfile repositories on github.
I eventually ended up with the concept of "holman does dotfiles".

So this dotfiles repository is primarily based on the work of Zach Holman.
Find the original at github: https://github.com/holman/dotfiles
