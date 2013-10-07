# System setup for polyglot developers

Automated system setup for developers with idempotency (i.e. run it as many times as you like...no harm will be done).

## What is this and who is it for?

If you've found boxen but were afraid of it because it seems complicated, this is probably for you. This is somewhat like boxen, but **without** a complicated configuration managament tool (i.e. Puppet) calling the shots. When I initially started this, I thought I was going to use ansible because it is much simpler than Puppet or Chef; however, I quickly realized, that was silly. Most of these installations are super simple, I'm only ever going to perform the install on a macbook (would you ever go from developing on a mac to anything else?), and even with a fancy tool, you'd have to find a special plugin or write it yourself to achieve idempotency (the main claim to fame of these CM tools).

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


## Install

    % bash < <(curl -s https://raw.github.com/wilmoore/system/master/setup)

## Inspiration

- [2011 Rubyist’s guide to a Mac OS X development environment](http://robots.thoughtbot.com/post/8700977975/2011-rubyists-guide-to-a-mac-os-x-development)
- [cowboy/dotfiles](https://github.com/cowboy/dotfiles)
- [pengwynn/dotfiles](https://github.com/pengwynn/dotfiles)
- [meskyanichi/dotfiles](https://github.com/meskyanichi/dotfiles)
- [boxen](https://github.com/boxen/our-boxen)

## LICENSE

  MIT
