# Table of contents 
- i3
- Alacritty
- Picom
- Rofi
- fzf
- scrot

# Applications

## i3

### Polish language

Command to use in terminal:

// FIXME: This doesn't work at all. Both with "" and without.

```bash
setxkbmap -layout pl
```

Or add this to your i3 config file

```
exec "setxkbmap -layout pl"
```

## Alacritty

You have to install cargo first. Just follow steps from google.

```bash
cargo install alacritty
```

sometimes I need to 

```bash
sudo apt-get update
sudo apt-get install libfontconfig1-dev
```

### Setting alacritty as default terminal

After creating new terminal, alacritty starts up.

```bash
sudo update-alternatives --install /usr/bin/x-terminal-emulator x-terminal-emulator $(which alacritty) 50
sudo update-alternatives --config x-terminal-emulator
```

To check current terminal you can use `echo $TERM`.
If all is set up correctly you'll see `alacritty`.

## Picom

```bash
picom --config ~/.config/picom/picom.conf &
```

## Rofi

It's just better dmenu.
Reference: https://github.com/davatorium/rofi


## fzf

If Ctrl + R doesn't trigger history fuzzy finding - read this:
https://unix.stackexchange.com/questions/665689/fzf-ctlr-r-not-triggering-history-search-on-command-line.
Just find source `key-bindings.zsh` file. It can be here: `/usr/share/doc/fzf/examples/key-bindings.zsh` or in your home dir. It doesnt matter. It only matters that you have to place 

```bash
source /usr/share/doc/fzf/examples/key-bindings.zsh
```
in your `.zshrc` file.


## scrot

### Installation

Just install with

```bash
sudo apt-get install scrot
```


### Usage

Use that command, and select area that you want to create screenshoot with
```bash
scrot -s
```
