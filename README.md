## Setup MacOS workstation 🚀

### [Homebrew](https://brew.sh/index_fr)

```sh
  /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

### [1password](https://1password.com/)

```sh
  brew cask install 1password-cli && \
    eval $(op signin my.1password.com beaurain.florent@gmail.com --shorthand beaurain-florent
```

### SSH Key

```sh
  op get document 7bjb3k4yfndydd3wqjtlf26lve > ~/.ssh/id_rsa && \
    op get document x24ofo3iw5eypnacl7yiqvjuiq > ~/.ssh/id_rsa.pub && \
    chmod 600 ~/.ssh/id_rsa && \
    chmod 644 ~/.ssh/id_rsa.pub
    eval "$(ssh-agent -s)" && \
    ssh-add -K ~/.ssh/id_rsa
```

### PGP Key

```sh
  brew cask install gpg-suite-no-mail && \
    op get document l7b5wtjbhbe67i2ypxrvy45tnu | gpg --import && \
    op get document 4wq4tsl3jjf2fawu7pzh3k22zq | gpg --import
```

### [chezmoi](https://github.com/twpayne/chezmoi)

```sh
  brew install twpayne/taps/chezmoi && \
    chezmoi init https://github.com/beauraF/setup && \
```

### [Brewfile](https://github.com/Homebrew/homebrew-bundle/)

```sh
  brew bundle install --no-lock --file $(chezmoi source-path)/Brewfile
```

### [Oh-My-Zsh](https://ohmyz.sh/)

```sh
  sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

### [spaceship-prompt](https://github.com/denysdovhan/spaceship-prompt)

```sh
  git clone https://github.com/denysdovhan/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt" && \
    ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"
```

### chezmoi apply

```sh
  chezmoi apply -v
```

### [zsh-completions](https://github.com/zsh-users/zsh-completions/)

```sh
  rm -f ~/.zcompdump; compinit
```

### [NGinx](https://www.nginx.com/)

```sh
  sudo brew services start nginx
```

### [VSCode](https://code.visualstudio.com/)

```sh
  code --install-extension editorConfig.editorConfig && \
    code --install-extension ms-azuretools.vscode-docker && \
    code --install-extension monokai.theme-monokai-pro-vscode && \
    code --install-extension esbenp.prettier-vscode && \
    code --install-extension rebornix.ruby && \
    code --install-extension sianglim.slim
```
