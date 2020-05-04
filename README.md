## setup MacOS workstation

### [SSH Key](https://help.github.com/en/enterprise/2.16/user/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

```sh
  ssh-keygen -t rsa -b 4096 -C 'beaurain.florent@gmail.com' && \
    eval "$(ssh-agent -s)" && \
    ssh-add -K ~/.ssh/id_rsa
```

### [Homebrew](https://brew.sh/index_fr)

```sh
  /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
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

### [Chezmoi](https://github.com/twpayne/chezmoi)

```sh
  brew install twpayne/taps/chezmoi && \
    chezmoi init https://github.com/beauraF/setup && \
    brew bundle install --no-lock --file $(chezmoi source-path)/Brewfile && \
    chezmoi apply -v
```

### [zsh-completions](https://github.com/zsh-users/zsh-completions)

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

### [GPG Key](https://help.github.com/en/articles/generating-a-new-gpg-key)

```sh
  gpg --full-generate-key
```
