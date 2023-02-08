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
