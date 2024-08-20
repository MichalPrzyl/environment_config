# Table of contents 
- i3
- Alacritty
- Picom
- Rofi
- fzf

# Applications

## i3
## Alacritty

```bash
cargo install alacritty
```

sometimes I need to 

```bash
sudo apt-get update
sudo apt-get install libfontconfig1-dev
```

### Setting alacritty as default terminal

```bash
sudo update-alternatives --install /usr/bin/x-terminal-emulator x-terminal-emulator $(which alacritty) 50
sudo update-alternatives --config x-terminal-emulator
```

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
