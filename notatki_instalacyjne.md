1. monitor + rozdzielczosc (xrandr)
Trzeba stworzyc plik ~/.xprofile ktory bedize to robil automatycznie, zeby po reboocie zachowywala sie nowa rozdzielczosc.

```
#!/bin/sh
xrandr --newmode "3840x1080_60.00"  346.00  3840 4088 4496 5152  1080 1083 1093 1120 -hsync +vsync
xrandr --addmode Virtual1 3840x1080_60.00
```

2. git
Nie ma gita. Prosty `sudo apt-get install git`.

3. i3
prosty apt-install i4 i przelogowanie sie
Od razu trzeba pobrac swoja konfiguracje
git clone https://github.com/MichalPrzyl/i3_config i wrzucic to do katalogu `~/.config/i3`. Pewnie tam bedzie plik `config` wiec go podmien/zamien.

4. rofi
Prosty zamiennik d-menu. 
Prosta komenda: `sudo apt install rofi`. I gotowe.

5. Alacritty - poprawna instrukcja
`sudo apt install cmake`
Nie sluchaj tego co jest na dole. to jest poprawna instrukcja:

Po pierwsze zainstaluje dependency
`https://github.com/alacritty/alacritty/blob/master/INSTALL.md#debianubuntu`

Po drugie zainstaluj rust i cargo:
`https://doc.rust-lang.org/cargo/getting-started/installation.html`

i na koniec
`cargo install alacritty`

Zrobienie zeby alacritty bylo defaultowe:
`https://askubuntu.com/questions/1364954/make-alacritty-the-default-terminal-permanently`
Skrot tego linku:
	1. `sudo update-alternatives --install /usr/bin/x-terminal-emulator x-terminal-emulator /usr/bin/alacritty 50`
	2. `sudo update-alternatives --config x-terminal-emulator`

Moja konfiguracja alacritty: `https://github.com/MichalPrzyl/alacritty_config`

6. zsh
wiki instalacji:
https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH
Wystarczy `sudo apt install zsh`. 

Tak zrobisz zeby to bylo domyslne:
```
chsh -s $(which zsh)
```
Uruchom gdzies powloke ZSH zeby uruchomic konfiguracje wstepna.

Moja konfiguracja zsh: `https://github.com/MichalPrzyl/zsh_config`


6.1 oh-my-zsh
https://ohmyz.sh/#install

7. feh
`sudo apt install feh`

8. picom
Tutaj info
`https://github.com/yshui/picom`
Tutaj sa wypisane dependencies ktore trzeba zrobic `sudo apt install ...`.
Potem `sudo apt install picom`.
A potem zostaje moj config:
`https://github.com/MichalPrzyl/picom_config`

9. wyglad
super poradnik do i3 wygladu:
`https://itsfoss.com/i3-customization/`
``

7. Nvim

8. Emacs doom
Fajny artykuł:
`https://www.maketecheasier.com/install-doom-emacs/`
