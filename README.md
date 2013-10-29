# Developer System Setup for Mac OS X

Prepares a Mac running OS X Mountain Lion for polyglot software development with idempotency (i.e. run it as many times as you like...no harm will be done).

## Install

### 1. Get XCode

[![Xcode - Apple](http://r.mzstatic.com/images/web/linkmaker/badge_macappstore-lrg.gif)](https://itunes.apple.com/us/app/xcode/id497799835?mt=12&uo=4)

### 2. Download "Command Line Tools"
  
  XCode > Preferences > Downloads

### 3. Run Setup

    % bash < <(curl -s https://raw.github.com/wilmoore/system/master/setup)

## What's in here?

- Mac OSX system updates
- dotfiles from `github.com/wilmoore/dotfiles`
- homebrew
    - ag, tree, wget, watch
    - ctags, tmux, git, reattach-to-user-namespace
    - vim macvim vimpager
    - phantomjs
- version managers for programming languages
    - nvm / Node.js
    - chruby / Ruby
    - php-version / PHP

## Inspiration

- [2011 Rubyist’s guide to a Mac OS X development environment](http://robots.thoughtbot.com/post/8700977975/2011-rubyists-guide-to-a-mac-os-x-development)
- [cowboy/dotfiles](https://github.com/cowboy/dotfiles)
- [pengwynn/dotfiles](https://github.com/pengwynn/dotfiles)
- [meskyanichi/dotfiles](https://github.com/meskyanichi/dotfiles)
- [boxen](https://github.com/boxen/our-boxen)

## LICENSE

  MIT
