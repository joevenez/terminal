# Terminal Configurations

This repository contains configuration and setup files for use on different machines to have the same terminal configurations.

### Shell

Oh-My-ZSH is used which can be downloaded from [here](https://ohmyz.sh/#install) or installed via:

```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### Plugins

#### [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions/tree/master)

```
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

Update `~/.zshrc` plugins to include the plugin. I.e

```
plugins=(
    # other plugins...
    zsh-autosuggestions
)
```

#### [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)

```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

Update `~/.zshrc` plugins to include the plugin. I.e

```
plugins=(
    # other plugins...
    zsh-syntax-highlighting
)
```

#### [zsh-you-should-use](https://github.com/MichaelAquilina/zsh-you-should-use?tab=readme-ov-file)

```
git clone https://github.com/MichaelAquilina/zsh-you-should-use.git $ZSH_CUSTOM/plugins/you-should-use
```

Update `~/.zshrc` plugins to include the plugin. I.e

```
plugins=(
    # ...
    you-should-use
    # ...
)
```

#### [zsh-history-substring-search](https://github.com/zsh-users/zsh-history-substring-search)

```
git clone https://github.com/zsh-users/zsh-history-substring-search ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-history-substring-search
```

Update `~/.zshrc` plugins to include the plugin. I.e

```
plugins=( [plugins...] zsh-history-substring-search)
```

#### [jsontools](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/jsontools)

```
plugins=(... jsontools)
```

### Configuration Files

#### [Zsh](https://ohmyz.sh/)

We can simply copy the `zshrc` from this repo into `~/.zshrc` to have the proper configurations.

NOTE: if there are any aliases or configurations in the current `~/.zshrc` they will be overriden so we need to make sure to migrate any to the new one

#### [Powerlevel10K](https://github.com/romkatv/powerlevel10k)

Install the powerlevel10k repo:

```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/powerlevel10k
```

Update the `ZSH_THEME`

```
ZSH_THEME="powerlevel10k/powerlevel10k"
```

After that we need to source the `zshrc`. Once prompted install the `Meslo` font and than we need to restart the terminal to setup the theme. We can than walkthrough the setup or copy the powerlevel10k configuration from this git repo or start from scratch

#### VS Code

Add the following lines to the settings.json to configure the terminal in VSCode.

```
"terminal.integrated.defaultProfile.osx": "zsh",
"terminal.integrated.fontFamily": "MesloLGS NF",
```

Make the VSCode editor font the same:

```
"editor.fontFamily": "MesloLGS NF",
```

### Settings

### Helpful Links/ Documentation

PowerLevel10K Git symbols: https://github.com/romkatv/powerlevel10k/blob/master/README.md#what-do-different-symbols-in-git-status-mean

Youtube Video inspiration: https://www.youtube.com/watch?v=CF1tMjvHDRA

Iterm text editing presets: https://apple.stackexchange.com/questions/154292/iterm-going-one-word-backwards-and-forwards

TokyoNight color schema: https://raw.githubusercontent.com/mbadolato/iTerm2-Color-Schemes/master/schemes/tokyonight-storm.itermcolors
