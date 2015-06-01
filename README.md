# Mac OS X setup for developers

> Prepares a Mac running OS X Mavericks for polyglot software development.

## 1. Install Xcode and the command-line developer tools

Type the following command in a terminal, then choose "Get Xcode" and the **App Store** will open displaying an option to install **Xcode**:

        % xcode-select --install

   ![](https://cloudup.com/cq4or0NPqnD+)

Once **Xcode** installation is complete, repeat the above command but this time, choose "Install" for the Xcode Command Line Tools.

        % xcode-select --install

   ![](https://cloudup.com/cq4or0NPqnD+)

### Items of note

- You will need a free Apple ID in order to proceed.
- This takes a while so go grab your favorite beverage, visit the restroom, check email/irc, then come back.

## 2. Agree to the Xcode/iOS license

Type the following command in a terminal then follow the prompts to accept the license agreements:

    % sudo xcodebuild -license

You may test that all is well by typing the following in a terminal:

    % make

Assuming there is no `makefile` in your current directory, you should see the following output:

    make: *** No targets specified and no makefile found.  Stop.

## 3. Install Homebrew and Git

    % bash < <(curl -sL https://raw.github.com/wilmoore/homebrew-home/master/install)

NOTE: While this is the same homebrew you'd get from [brew.sh](http://brew.sh), this one simply installs to `$HOME/.homebrew` for [reasons outlined here](https://github.com/wilmoore/homebrew-home/wiki/Rationale) and installs homebrew provided `git(1)`.

## 4. Install ZSH

    % bash < <(curl -sL https://raw.github.com/wilmoore/homebrew-home/master/activate-homebrew-zsh)

You may test that all is well by typing the following in a __NEW__ terminal (window or tab):

    % echo $SHELL

Assuming everything went well, you should see a path output that ends with `zsh`:

## 5. Shell Configuration

### Install Dotfiles

    % bash < <(curl -sL https://raw.github.com/wilmoore/dotfiles/master/setup)

### Install Terminal Theme

    % open "$HOME/.config/terminal/modified/terminal-ocean-dark-base16.terminal"

- A new terminal window will open,  
- Manually navigate to the **Preferences...** pane
- Select __terminal-ocean-dark-base16__
- Hit the **Default** button
- Exit Terminal

### Install Powerline

    % pip install --user git+git://github.com/Lokaltog/powerline

## 6. Install Software

    % software

## 8. Install Vim Plugins

    % vim +NeoBundleInstall +qall

## 9. Initialize Basic Mac OS X Settings

    % ~/.config/init/macbook

## 10. Mac OS X Settings and Preferences

    % cd ~
    % curl --user "wilmoore:???" -L# https://github.com/wilmoore/macbook-settings/archive/master.tar.gz | tar xz --strip-components=1 --exclude=README.md

## References

- [dotfiles]
- [homebrew]

## Inspiration

- [2011 Rubyist’s guide to a Mac OS X development environment](http://robots.thoughtbot.com/post/8700977975/2011-rubyists-guide-to-a-mac-os-x-development)
- [boxen](https://github.com/boxen/our-boxen)

## LICENSE

  MIT

[dotfiles]: https://github.com/wilmoore/dotfiles
[homebrew]: https://github.com/wilmoore/homebrew-home

