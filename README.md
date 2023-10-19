# Terminal_Rice


## Configuring neofetch themes
- First git clone this repo
```
$ git clone https://github.com/Chick2D/neofetch-themes.git
```
- Make the config directory for neofetch
```
$ mkdir ~/.config/neofetch
```
- Copy whatever themes you like to your config directory
```
$ cp ~/neofetch-themes/small/dotfetch.conf ~/.config/neofetch/
$ mv ~/.config/neofetch/dotfetch.conf ~/.config/neofetch/config.conf
```
- References
  - https://github.com/Chick2D/neofetch-themes
    
## Configuring alacritty themes
- Copy the config file to your alacritty config file
```
$ mv ~/.config/alacritty/alacritty.yml ~/Backup
$ cp ~/Terminal_Rice/alacritty/alacritty.yml ~/.config/alacritty/
```
- First go into alacritty config directory
```
$ cd ~/.config/alacritty/
```
- Git clone this repo
```
$ git clone https://github.com/eendroroy/alacritty-theme.git
```
- Change the existing import line in ```~/.config/alacritty/alacritty.yml```
```
import:
 - ~/.config/alacritty/alacritty-theme/themes/{theme}.yaml
```
- References
  - https://github.com/eendroroy/alacritty-theme
  - https://fuchsia.googlesource.com/third_party/github.com/alacritty/alacritty/+/refs/tags/v0.10.0-rc2/alacritty.yml

## To make rice setup complete
- Installing colorscripts. See [guide](https://gitlab.com/dwt1/shell-color-scripts)
  ```
  $ yay -S shell-color-scripts
  ```
  - Add this line to your ```~/.zshrc``` file
  ```
  colorscript -e alpha
  ```
- Installing pipes. To execute see [guide](https://github.com/pipeseroni/pipes.sh#contents)
  ```
  $ git clone https://github.com/pipeseroni/pipes.sh.git
  $ cd pipes.sh
  $ sudo make install
  ```
- Installing tty clock terminal. To execute see [guide](https://github.com/xorg62/tty-clock/blob/master/README)
  ```
  $ git clone https://github.com/xorg62/tty-clock.git
  $ cd tty-clock
  $ sudo make install
  ```
- Installing unimatrix. To execute just type ```$ unimatrix```. See [guide](https://github.com/will8211/unimatrix)
  ```
  $ curl -L https://raw.githubusercontent.com/will8211/unimatrix/master/unimatrix.py -o ~/.local/bin/unimatrix
  $ chmod a+rx ~/.local/bin/unimatrix
  ```
  - Add this to your ```~/.zshrc``` file
  ```
  alias unimatrix="~/.local/bin/unimatrix -c blue -u 'Linux'"
  ```

## Configuring zsh
- Given here : https://computingforgeeks.com/how-to-install-and-configure-zsh-shell-on-linux/?expand_article=1
- Change your zshrc file with mine.
```
$ cp ~/Terminal_Rice/zsh/.zshrc ~/
```

## Configuring Vim
- First install neovim
```
$ sudo pacman -S neovim
```
- Move all the nvim config files to Backup
```
$ mkdir -p ~/Backup/nvim
$ mv ~/.config/nvim/* ~/Backup/nvim
```
- Now install NvChad
```
$ git clone https://github.com/NvChad/NvChad ~/.config/nvim --depth 1
```
- Open neovim. Type ```n```
```
$ nvim
```
- To set theme ```space t h``` -> Set cappuccin
- Configuring syntax highlighting
```
:TSInstallInfo
:TSInstall python
```








