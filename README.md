# dotfiles
A repository for current dotfiles.

*******
## bash
Recommended: append contents of `.bashrc` and `.bash_functions` instead of copying the files themselves.

**Adding/applying bash config files to host**
```
cat /path/to/dotfiles/bash/.bashrc >> ~/.bashrc
cat /path/to/dotfiles/bash/.bash_functions >> ~/.bash_functions
```

## tmux
It is recommended that a `.tmux.conf.local` file is created and edited to generate the config file rather than just the `.tmux.conf file`. However, the `.tmux.conf` file must be linked first.

To install:
```
ln -sf /path/to/dotfiles/tmux/.tmux.conf ~/.tmux.conf
cp /path/to/dotfiles/tmux/.tmux.conf.local ~/.tmux.conf.local
```

## starship
Starship has two dependencies: [nerd font](https://www.nerdfonts.com/font-downloads) and well, [starship](https://starship.rs). When downloading a nerd font, the files are recommended to be stored in
```
~/.local/share/fonts
```
So that when the fonts get updated with the following command
```
fc-cache -fv
```
The command will search `~/.local/share/fonts` and find the fonts you have downloaded, and install them.

Starship can be installed with the following command
```
curl -sS https://starship.rs/install.sh | sh
```
When starship is installed, it will provide additional info so that starship can be initialized, here is an example for bash, which should be added to the end of the `.bashrc` file.
```
eval "$(starship init bash)"
```
The config file can should be copied to the `~/.config` folder, below is an example
```
cp /path/to/dotfiles/starship/starship.toml ~/.config
```
