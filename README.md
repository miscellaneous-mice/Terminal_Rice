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
- For Using [eendroroy theme](https://github.com/eendroroy/alacritty-theme) use alacritty_eendroroy
- For Using nord theme use alacritty_nord
- For Using [catppuccin theme](https://github.com/catppuccin/alacritty#usage) use alacritty_catppuccin
- References
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
- Install zsh and dependencies
```
$ sudo pacman -S zsh wget
```
- we need to make it our default shell
```
$ sudo usermod $USER -s /usr/bin/zsh
$ logout
```
- Install Oh-my-zsh
```
$ touch ~/.zshrc
$ sh -c "$(wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
```
- Installating useful plugins for zsh
```
$ cd ~/.oh-my-zsh/plugins
$ git clone https://github.com/zsh-users/zsh-syntax-highlighting.git
$ git clone https://github.com/zsh-users/zsh-completions ~/.oh-my-zsh/custom/plugins/zsh-completions
```
- Change your zshrc file with mine.
```
$ mv ~/.zshrc ~/Backup/
$ cp ~/Terminal_Rice/.zshrc ~/
```
- Apply your zsh configuration
```
$ source ~/.zshrc
```

- References
  - https://computingforgeeks.com/how-to-install-and-configure-zsh-shell-on-linux/?expand_article=1

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
- Configuring syntax highlighting
```
:TSInstallInfo
:TSInstall python
:TSInstall cpp
```

**Only for C++ and Python**
- Install npm, nodejs and clang. Update all the tools.
```
$ sudo pacman -Syu nodejs npm clang
$ sudo npm i -g npm
$ sudo npm i -g n
```
- Move customs folder to backup. Copy this repo's custom foldr to nvim configs.
```
$ mv ~/.config/nvim/lua/custom ~/Backup
$ cp -r ~/Terminal_Rice/custom ~/.config/nvim/lua/
```
- To set theme ```space t h``` -> Set theme
- Run these commands
```
:MasonInstallAll
```
- Quit and run the nvim.
- For C++ You can change the formatting by
```
$ ~/.local/share/nvim/mason/bin/clang-format --style microsoft  --dump-config > .clang-format
```

- References
  - https://youtu.be/Mtgo-nP_r8Y?si=U47CeRvPBzUUC3c3
  - https://youtu.be/4BnVeOUeZxc?si=9HEfYz-SDExRR5Y4








