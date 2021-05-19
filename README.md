# InitPower9k

A guide for setting up InitPower9k.

## Iterm
---

- Install Homebrew
> /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

- Install Iterm
> brew cask install iterm2

- Change Iterm color Scheme

## Fish
---

Install Fish
> brew install fish

Install oh-my-fish
> curl -L https://get.oh-my.fish | fish

Install Fisher
> curl -sL https://git.io/fisher | source && fisher install jorgebucaran/fisher

Install & Configure omf plugins
- acomagu/fish-async-prompt
- jorgebucaran/replay.fish
- oh-my-fish/plugin-pj
> set -U PROJECT_PATHS ~/Coding/Projects ~/home
- jhillyerd/plugin-git

Abbreviation | Command
--- | ---
gb | `git branch -vv`
gco | `git checkout`
gcod | `git checkout develop`
gcom | `git checkout master`
gcb | `git checkout -b`
gc | `git commit -v`
gc! | `git commit -v --amend`
gcm | `git commit -m`
gcam | `git commit -a -m`
gd | `git diff`
gds | `git diff --stat`
gl | `git pull`
ggl | `pull origin current-branch`
gp | `git push`
gpo | `git push origin`
ggp | `push origin current-branch`
ggpnp | `pull & push origin current-branch`
grb | `git rebase`
grbm | `git rebase master`
grbd | `git rebase develop`
ggu | `fetch & rebase current-branch on top of the upstream branch`
gsta | `git stash`
ga | `git add`
gaa | `git add --all`


## Zsh
---

Install zsh
> brew install zsh

Install oh-my-zsh
> $ sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

Install & Configure omzsh plugins
```sh
vi ~/.zshrc
ZSH_THEME="agnoster"
plugins=(git sublime vscode history history-substring-search zsh-syntax-highlighting zsh-autosuggestions)
```

## Shell
List installed shells
> cat /etc/shells

Set default shell
> chsh -s <path_to_shell>

## Miscellaneous
---

### Mac
- Bind `⌘+1` to Iterm
- Bind `⌘+2` to Amphetamine
- Bind `⌘+3` to Sleep

```
    System Preferences » Keyboard » Shortcuts » App Shortcuts
    Click +
    Menu Title = Sleep
```

![Bind sleep hotkey](resources/bind_sleep.png?raw=true "Bind sleep")

#### Terminal Notification
> osascript -e 'display notification "Process execution complete" with title "Process terminated" sound name "Morse"'

```sh
alias nf "osascript -e 'display notification \"Process execution complete\" with title \"Process terminated\" sound name \"Morse\"'"
funcsave nf
```

#### Touch Bar
Install My TouchBar. My Rules.
> brew install --cask mtmr

<!-- Modify [resources/items.json](~/Library/Application\ Support/MTMR/items.json) -->
Modify [~/Library/Application\ Support/MTMR/items.json](resources/items.json)
