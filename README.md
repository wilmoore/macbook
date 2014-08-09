# Developer System Setup for Mac OS X

> Prepares a Mac running OS X Mavericks (or higher) for polyglot software development. Similar to Boxen, but easier for me to grok (I'm a simple man).

## 1. Remap the CAPS LOCK key to CONTROL

If you are using the VIM or Emacs editor, you'll want to do this:

1. COMMAND + SPACE (to open spotlight).
2. Type `System Preferences` (then press enter), then `Keyboard` (into the search box).
3. Press the __Modifier Keys…__ button (bottom right corner).
4. Change the action for **CAPS LOCK** Key to **Control**.

## 2. Install Xcode and the command-line developer tools [![Xcode - Apple](http://r.mzstatic.com/images/web/linkmaker/badge_macappstore-lrg.gif)](https://itunes.apple.com/us/app/xcode/id497799835?mt=12&uo=4)

Type the following command in a terminal:

        % xcode-select --install

   ![](https://cloudup.com/cxrqLVUkX6f+)

Choose "Get Xcode" and the **App Store** will open displaying an option to install **Xcode**. You may proceed by selecting "Install" for the Xcode Command Line Tools; however, I recommend getting the full "Xcode".

## 3. Agree to the Xcode/iOS license

    % sudo xcodebuild -license

## 4. Install Homebrew

    % bash < <(curl -sL https://raw.github.com/wilmoore/homebrew-home/master/install)

## 5. Install ZSH

    % bash < <(curl -sL https://raw.github.com/wilmoore/homebrew-home/master/activate-homebrew-zsh)

## 6. Install Dotfiles

    % bash < <(curl -sL https://raw.github.com/wilmoore/dotfiles/master/setup)

## 7. Install Software from Brewfile(s)

[Example .brewfile](http://git.io/vrgfLw)

    % brew bundle-dir

## 8. Install Ruby, Node

    % ruby-install --rubies-dir $XDG_DATA_HOME/rubies ruby
    % nvm install 0.11

NOTE: other programming languages are taken care of via the Brewfile(s).

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

