# Mac OS X setup for developers

> Prepares a Mac running OS X Mavericks for polyglot software development.

## 1. Remap the CAPS LOCK key to CONTROL

If you are using the VIM or Emacs editor, you'll want to do this:

1. COMMAND + SPACE (to open spotlight).
2. Type `System Preferences` (then press enter), then `Keyboard` (into the search box).
3. Press the __Modifier Keys…__ button (bottom right corner).
4. Change the action for **CAPS LOCK** Key to **Control**.

## 2. Install Xcode and the command-line developer tools

Type the following command in a terminal:

        % xcode-select --install

   ![](https://cloudup.com/cxrqLVUkX6f+)

Choose "Get Xcode" and the **App Store** will open displaying an option to install **Xcode**. You may proceed by selecting "Install" for the Xcode Command Line Tools; however, I recommend getting the full "Xcode".

### Items of note

- You will need a free Apple ID in order to proceed.
- This takes a while so go grab your favorite beverage, visit the restroom, check email/irc, then come back.

## 3. Agree to the Xcode/iOS license

Type the following command in a terminal then follow the prompts to accept the license agreements:

    % sudo xcodebuild -license
    
You may test that all is well by typing the following in a terminal:

    % make
    
Assuming there is no `makefile` in your current directory, you should see the following output:

    make: *** No targets specified and no makefile found.  Stop.

## 4. Install Homebrew and Git

    % bash < <(curl -sL https://raw.github.com/wilmoore/homebrew-home/master/install)
    
NOTE: While this is the same homebrew you'd get from [brew.sh](http://brew.sh), this one simply installs to `$HOME/.homebrew` for [reasons outlined here](https://github.com/wilmoore/homebrew-home/wiki/Rationale) and installs homebrew provided `git(1)`.

## 5. Install ZSH

    % bash < <(curl -sL https://raw.github.com/wilmoore/homebrew-home/master/activate-homebrew-zsh)

You may test that all is well by typing the following in a __NEW__ terminal (window or tab):

    % echo $SHELL

Assuming everything went well, you should see a path output that ends with `zsh`:

## 6. Shell Configuration

### Install Dotfiles

    % bash < <(curl -sL https://raw.github.com/wilmoore/dotfiles/master/setup)

### Install Powerline

    % pip install --user git+git://github.com/Lokaltog/powerline

## 7. Install Software from Brewfile(s)

[See My .brewfile](http://git.io/vrgfLw)

    % brew bundle-dir

## 8. Install Ruby, Node

    % ruby-install --rubies-dir $XDG_DATA_HOME/rubies ruby
    % nvm install 0.11

NOTE: other programming languages are taken care of via the Brewfile(s).

## 9. Install Vim Plugins

    % vim +NeoBundleInstall +qall

## 10. Manual Configurations

Open the following programs and set them to start on login:

- slate
- ...

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

