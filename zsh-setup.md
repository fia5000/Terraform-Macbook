# Install oh-my-zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

# Install antigen
curl -L git.io/antigen > antigen.zsh
source ~/antigen.zsh

# Install Powerline
pip install --user git+git://github.com/powerline/powerline

# Install Powerline Fonts
mkdir Fonts \
cd Fonts \
git clone https://github.com/powerline/fonts.git --depth=1 \
cd fonts \
./install.sh

# Install autojump
brew install autojump

# Install Suggestions
```
mkdir ~/.zsh/zsh-autosuggestions
cd ~/.zsh/zsh-autosuggestions
git clone git://github.com/zsh-users/zsh-autosuggestions ~/.zsh/zsh-autosuggestions
```
# ~/.zshrc
```
source /Users/me/antigen.zsh

# Load the oh-my-zsh's library.
antigen use oh-my-zsh

# Bundles from the default repo (robbyrussell's oh-my-zsh).
antigen bundle git
antigen bundle heroku
antigen bundle pip
antigen bundle lein
antigen bundle command-not-found
antigen bundle autojump
antigen bundle brew
antigen bundle common-aliases
antigen bundle compleat
antigen bundle git-extras
antigen bundle git-flow
antigen bundle npm
antigen bundle osx
antigen bundle web-search
antigen bundle z
antigen bundle zsh-users/zsh-syntax-highlighting

antigen bundle zsh-users/zsh-history-substring-search ./zsh-history-substring-search.zsh

# Load the theme.
antigen theme gnzh

# Tell antigen that you're done.
antigen apply

source /Users/me/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh

```
