Some fundamental tools and maintainable dotfile collections (Mac specific). And one may follow along as he/she gets a new Mac.

# change your name
if this is a working Mac or other reasons, you want to change your user root and your username, please check out [apple support](https://support.apple.com/zh-cn/HT201548)

# iterm2 and theme
Just google online for iterm2 and [iterm theme](https://iterm2colorschemes.com/). And put on my favorite theme of all time, Gruvbox !!!

# zsh
If you're using this dotfiles proj, you may want to first comment out links other than shell and zsh, since it may get messy and vim and other tools deserve to be handled carefully.

```yml
# in file install.conf.yaml
# commit like this 
- link:
    ~/.shell:
    ~/.zsh:
    ~/.zshrc:
    # ~/.vim:
    # ~/.vimrc:
```
Then, you shall run `./install`

There you may run into some troubles, for examples as I change to a M1 Mac
1. there is no default python, only python3. some shell functions would break, just find and fix it
2. in fact I install brew prior to this section, brew go off-grid. fix with `export PATH="/opt/homebrew/bin:$PATH"` in zshrc (I put it in zshrc_local_before)



But nothing we can't handle


# brew and tools
first, go to [brew website](https://docs.brew.sh/Installation) for installation instruction.

then, install these babies.
```bash
brew install tldr  # great replacement for man

brew install bat  # great replacement for cat

brew install ranger

brew install trash

# please do install these two, or "install" would be faulty
brew install ripgrep # replacement for grep, command used as rg
brew install exa  # replacement for ls

# something wrong with fasd on my mac 
brew install fasd # more advanced than z but slower

brew install htop  # this tool needs some time to learning

# faster, git sesentive
brew install fd  # fast than find

# to replace grep
brew install ripgrep  # rg

brew install fzf

# modern ssh
brew install mosh

# ack https://beyondgrep.com/documentation
brew install

# this one is important, and we will config more of it later
`brew install tmux` 

# *** other fancy stuff was discovered later on ***
# not installed yet
brew install atool  # for the aunpack
```


# vim
> I used vim8 back in the day. But here I'm gonna switch to neovim for a change
```bash
brew install neovim
# change neovim to the default vim
```
Then link back install.conf.yaml, do another `./install`. Then install vim-plug


## vim-plug
Following the repo's suggestion, put the plug.vim under the dir autoload. Then copy and run its command line.


## coc
`brew install node` 

If the python interpreter is wrong, `:CocConfig`, and put 
```
 "python.pythonPath": "/Users/someguy/opt/anaconda3/bin/python"
```

need to make it work popup is default , need key bindings


# tmux

# local zshrc (some fancy tools)
## macOS
```
# to make grep and ls display with better color
brew install coreutils

# useful tools
brew install z
# add the line below to zshrc_local_after 
. /usr/local/etc/profile.d/z.sh





```
