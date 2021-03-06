TODO: move all this to boxen
TODO: look into using rake to handle dotfiles. see: https://github.com/r00k/dotfiles

# Home & Config Notes

## OSX 10.8.4

### HomeBrew

Simple install using ruby

    ruby -e "$(curl -fsSL https://raw.github.com/mxcl/homebrew/go)"

After install setup $PATH. Move `/usr/local/bin` from the bottom to the top of `/etc/paths`
 so that homebrew apps take priority.

### iTerm2

TODO
import color scheme from ~/.iTerm2/Solarized-Dark.itermcolors
select scheme from dropdown


### NPM/Node

TODO

### PHP
TODO
    brew install php?

### Powerline

_Make sure python is installed and you have reloaded your terminal. `$ which pip` should_
_show `/usr/local/bin/php`._
_Make sure vim is installed as described below_

Install using pip.

    pip install git+git://github.com/Lokaltog/powerline
    mkdir ~/.config/powerline
    cp -R /usr/local/lib/python2.7/site-packages/powerline/config_files/* ~/.config/powerline

_make sure you have the status bar visible in your .vimrc `set ls=2`. I spent a few hours_
_scratching my head over that one_

_the "--user" flag should not be used during pip install if python is installed with brew_
_(despite with the docs say)._

[source(docs)](https://powerline.readthedocs.org/en/latest/installation/osx.html#installation-osx),
[source(gh issue)](https://github.com/Lokaltog/powerline/issues/39)

### Python

#### Install

Install using brew, see note about `/usr/local/bin` in the HomeBrew -> $PATH section above.

    $ brew install python
    $ pip install --upgrade pip
    $ pip install --upgrade setuptools

[source](https://github.com/mxcl/homebrew/wiki/Homebrew-and-Python)

### Ruby

#### Install RVM with stable Ruby

    $ \curl -L https://get.rvm.io | bash -s stable --ruby

*There is a backslash before curl. This prevents misbehaving if you have aliased it with*
*configuration in your ~/.curlrc file.*

#### For a progress bar when downloading RVM / Rubies:__

    $ echo progress-bar >> ~/.curlrc

[source](https://rvm.io/rvm/install)

#### Installing rdoc

    $ rvm docs generate

Then use the "ri" command to look up stuff in the ruby api

### [Mac]Vim

Install using brew

    $ brew install vim --override-system-vim;

Install Ctags for autocompletion support

    $ brew install ctags

Install [silver searcher](https://github.com/ggreer/the_silver_searcher) for faster searches in vim

    $ brew install the_silver_searcher

_Useful commands_

    :w !sudo tee %               "save a file you edited without needed permissions
    :w !sudo tee > /dev/null %   "same as above but hide stdout
    :so %                        "reload config"


### ZSH

    $ curl -L https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh | sh
    $ brew install autojump git-extras

