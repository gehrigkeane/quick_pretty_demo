# quick_pretty_demo
A lightening fast introduction to the shell with colors and stuff...

---

# Quickly, `.zshrc`

Let's start with order of events:

* `.zshenv` is always sourced, though prefer `.zshrc`
* `.zprofile` is sourced for login shells
* `.zshrc` The only file anyone uses (sourced for interactive shells) 
* `.zlogin` is sourced for login shells
* `.zlogout` is sourced when exiting

---

# Sourced?

`source` is a built-in command that executes the content of the file passed in the current shell. 

```bash
# For example, reload your shell configuration
source ~/.zshrc
```

`.` (period) is a synonym

```bash
# This is the same in fewer keystrokes
. ~/.zshrc
```

[ref](https://superuser.com/a/46146)

---

# What's a login shell?

* **Interactive**: the shell knows the user is ready/waiting behind the keyboard.
* **Non-interactive**: the shell knows the user is AFK
* **Login**: the shell is run as-part-of user login.
* **Non-login**: Any other shell run by the user after logging on

[ref](https://unix.stackexchange.com/a/50667)

---

# Be Organized

Quick recommendation to organize and partition shell configuration.

Consider...

```bash
# ~/.zshrc
source .zstuff
```

```bash
# ~/.zstuff
source ~/.shellaliases
source ~/.shellcolors
source ~/.shellfn
source ~/.shellpaths
source ~/.shellsecrets
source ~/.shellvars
```

```bash
# ~/.shellvars
export EDITOR="vim"
export GOPATH=$HOME/dev/golang
...
```

---

# Use a plugin manager

[`oh-my-zsh`](https://github.com/ohmyzsh/ohmyzsh)

> 🙃 A delightful community-driven framework for managing your zsh configuration.

[`zinit`](https://github.com/zdharma-continuum/zinit)

> 🌻 Flexible and fast ZSH plugin manager 


## Some plugins!

[zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)

> Fish-like autosuggestions for zsh

[fast-syntax-highlighting](https://github.com/zdharma-continuum/fast-syntax-highlighting)

> Feature-rich syntax highlighting for ZSH 

---

# Style your prompt

[spaceship](https://github.com/spaceship-prompt/spaceship-prompt)

> 🚀⭐ Minimalistic, powerful and extremely customizable Zsh prompt 

(deprecated) [powerlevel9k](https://github.com/Powerlevel9k/powerlevel9k)

(replacement) [powerline10k](https://github.com/romkatv/powerlevel10k)

...

---

# ls

```bash
ls -lG
```

Environment variables can only get you soo far... let's leave the 1980's

My favorite: [lsd](https://github.com/Peltoche/lsd)

```bash
lsd -Al ~/
```

More popular, a bit slower: [exa](https://github.com/ogham/exa)

```bash
exa -al ~/
```

---

# fzf

[fzf](https://github.com/junegunn/fzf)

```bash
# select git branches in horizontal split below (15 lines)
git branch | fzf-tmux -d 15
```

[fzf-tab](https://github.com/Aloxaf/fzf-tab)

```
# behold...
cd ~/...
gco ...
```

---

# Git

[tig](https://github.com/jonas/tig)

```bash
tig

# View stash
tig stash
```

[forgit](https://github.com/wfxr/forgit)

```bash
fga
fgcb
fgi
```

[gti](http://r-wos.org/hacks/gti Humorous git alias)

---

# Lightening round!

ncdu

[ripgrep](https://github.com/BurntSushi/ripgrep)

> ripgrep recursively searches directories for a regex pattern while respecting your gitignore 

```bash
rg "Repository" ./
```

[tldr](https://tldr.sh/) or [tealdeer](https://github.com/dbrgn/tealdeer)

> Simplified and community-driven man pages

```bash
tldr tar
```

[xh](https://github.com/ducaale/xh)

> Friendly and fast tool for sending HTTP requests 

```bash
xh :3000/users                 # resolves to http://localhost:3000/users
```

(macOCR) [ocr](https://github.com/schappim/macOCR)

> Get any text on your screen into your clipboard.

---

# Questions?

---

# References

Configuration Software

1. [oh-my-zsh](https://github.com/ohmyzsh/ohmyzsh)
1. (Windows) [oh-my-posh](https://ohmyposh.dev/docs/installation/windows)
2. [spaceship](https://github.com/spaceship-prompt/spaceship-prompt)
3. [zinit](https://github.com/zdharma-continuum/zinit)
4. [powerlevel10k](https://github.com/romkatv/powerlevel10k)

ZSH Plugins

1. [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)
2. [fast-syntax-highlighting](https://github.com/zdharma-continuum/fast-syntax-highlighting)

Command Line Tools

1. [slides](https://github.com/maaslalani/slides)
2. [lsd](https://github.com/Peltoche/lsd)
3. [exa](https://github.com/ogham/exa)
4. [fzf](https://github.com/junegunn/fzf)
5. [fzf-tab](https://github.com/Aloxaf/fzf-tab)
6. [tig](https://github.com/jonas/tig)
7. [forgit](https://github.com/wfxr/forgit)
8. [gti](http://r-wos.org/hacks/gti)
9. [rg](https://github.com/BurntSushi/ripgrep)
10. [tldr](https://github.com/dbrgn/tealdeer)
11. [xh](https://github.com/ducaale/xh)
12. [macOCR](https://github.com/schappim/macOCR)
