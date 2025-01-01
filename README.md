# Files to get going with dev enviroment

Steps
- clone repo and copy contents into `~/.config/`
- install kitty (no need to add to path)
- build tmux from source (see tmux github)
- install nvim (github)
- install omzsh and set zsh as default on omz first launch
- install nvm (node version manager). [add this config to your .zshrc](#) 
- install nodejs with nvm `nvm install 22`
- add `/home/<USERNAME>/.local/kitty.app/bin/kitty -e tmux new-session -A -s main` as startup application. Add shortcut (SUPER+T) for it to [optional]
- startup kitty with `/home/<USERNAME>/.local/kitty.app/bin/kitty -e tmux new-session -A -s main` or with shourtcut from previous step
- inside tmux session press `TMUX_LEADER + I` to install tmux plugins from config
- resource tmux config: `tmux source ~/.config/tmux/tmux.conf`
- Setup "JetbrainsMono Nerd Font". Install font files (ttf) to `~/.local/share/fonts/` and maybe restart system for changes to take effect
- install `golang, ruby, lua` languages.

> [!NOTE]
> tmux, kitty, nvim don't isntall from package manager repost. get from github


## zshrc additions

Appent do `.zshrc`

```
# Neovim path
export PATH="$PATH:/opt/nvim-linux64/bin" # important

# for nvm
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion

# for tmux
tmux source ~/.config/tmux/tmux.conf

# aliases
alias c=clear
alias g=git

# golang path
export PATH=$PATH:/usr/local/go/bin
```

