---
title: Install Ruby
stub: ruby
section: software
section_order: 3
---

{:.py-4 .mt-4 #ruby}
***

## 3. Install Ruby

[Ruby](https://www.ruby-lang.org/en/){:target="_blank" rel="noopener"} is a programming language popular with web applications.
**_You do not need to know anything about Ruby_** to use CollectionBuilder, but you do need it to run Jekyll on your system!

Jekyll requires a Ruby version 2.5.0 or greater.

{% capture win-ruby %}
Use [RubyInstaller for Windows](https://rubyinstaller.org/){:target="_blank" rel="noopener"}.

- First, [download](https://rubyinstaller.org/downloads/){:target="_blank" rel="noopener"} the suggested stable version "WITH DEVKIT" (as of this writing, Ruby+Devkit 2.7.X (x64)) and double click to install. Use the install defaults, but make sure "Add Ruby executables to your PATH" is checked. On the final step, ensure the box to start the MSYS2 DevKit is checked.

- Second, the installer will open a terminal window with options to install MSYS2 DevKit components. Choose option 3, "MSYS2 and MINGW development toolchain", or simply press ENTER to install all the necessary dependencies. The installer will proceed through a bunch of steps outputting a bunch of text in the terminal window -- *eventually*, this will conclude and you should see a message with success in it. If the window doesn't close, press Enter again or manually close it. (The installer can be restarted by typing `ridk install` into a command prompt)

- Having trouble? Need more detail? See [How to Install Ruby on Windows](https://lib-static.github.io/howto/howtos/installrubywindows.html){:target="_blank" rel="noopener"} for help.
{% endcapture %}
{% include bootstrap/card.md text=win-ruby header="Ruby on Windows" %}

{% capture mac-ruby %}
Installing Ruby on Mac can be difficult, but don't be deterred! If the method below doesn't work for you check out [How to Install Ruby on a Mac](https://lib-static.github.io/howto/howtos/installrubymac.html){:target="_blank" rel="noopener"} for more detail and other options.

OS X has a version of Ruby installed by default, but recommended practice is to set up a separate Ruby development environment.
To do this, follow the instructions below, which outline the steps to install Ruby using [rbenv](https://github.com/rbenv/rbenv){:target="_blank" rel="noopener"}.

#### Get the Xcode Command Line Tools First

- Ensure you have Xcode Command Line Tools, so that you can work with Ruby (and Git, etc.).
- To do this, open your terminal by clicking `Command (⌘) + Spacebar`, typing `terminal` into the spotlight box that appears, and pressing `Enter`.
- Type `xcode-select --install` into the terminal window and press `Enter` to start the installer. Note: this may take some time to install.

#### Use rbenv to Install Ruby

1. **Install Homebrew**
    - You'll need to use Homebrew to install rbenv. To install Homebrew, follow these steps:
        - Open the [Homebrew](https://brew.sh/){:target="_blank" rel="noopener"} webpage in your browser.
        - Open your terminal by clicking `Command (⌘) + Spacebar`, typing `terminal` into the spotlight box that appears, and pressing `Enter`.
        - Once inside your terminal, copy the script in the box underneath "Install Homebrew" on the [Homebrew](https://brew.sh/){:target="_blank" rel="noopener"} webpage. Paste this script you just copied into the terminal prompt and press `Enter`.
        - You'll then be prompted to press `Enter` once more to continue the install.

2. **Install rbenv**
    - Copy and paste the command `brew install rbenv` into your terminal prompt and press `Enter`. This installation might take a while.
    - Once rbenv has been installed, copy and paste `rbenv init` into the terminal prompt and press `Enter`.
    - Depending on whether you are using a [zsh](#zsh) or [bash](#bash) shell, follow the appropriate instructions below to finish the rbenv installation.

{% capture zsh %}
**If using the zsh environment:**

To complete the installation you will need to modify two configuration files:
- Open your zsh environment file with the terminal's text editor, nano, by copying and pasting `nano ~/.zshenv` into the terminal prompt and pressing `Enter`.
- Your terminal should switch to a nano text editor screen that includes a path to .zshenv at the top.
- Use the down arrow on your keyboard to move to the end of the text file.
- Paste `export PATH="$HOME/.rbenv/bin:$PATH"` at the end of the file.
- Press `Control` + `x` to exit and save the profile. You'll see a message at the bottom of your screen asking whether you want to save the file.
- Press the `y` key on your keyboard to specify yes, you want to save.
- Press `Enter` to finish saving the file and exit nano.
- Open your zsh configuration file with the terminal's text editor, nano, by copying and pasting `nano ~/.zshrc` into the terminal prompt and pressing `Enter`.
- Your terminal should switch to a nano text editor screen that includes a path to .zshrc at the top.
- Use the down arrow on your keyboard to move to the end of the text file.
- Paste the following two lines at the end of the file
```
source $HOME/.zshenv
eval “$(rbenv init – zsh)"
```
- Press `Control` + `x` to exit and save the file. You'll see a message at the bottom of your screen asking whether you want to save the file.
- Press the `y` key on your keyboard to specify yes, you want to save.
- Press `Enter` to finish saving the file and exit nano.
{% endcapture %}
{:#zsh}
{% include bootstrap/alert.md text=zsh color="info" %}

{% capture bash %}
**If using the bash environment:**

The program will ask you to edit your bash profile. To do this, follow these instructions:
- Open your bash profile with the terminal's text editor, nano, by copying and pasting  `nano ~/.bash_profile` into the terminal prompt and pressing `Enter`. 
- Your terminal should switch to a nano text editor screen that includes a path to .bash_profile at the top. 
- Use the down arrow on your keyboard to move to the end of the text file.
- Paste `eval "$(rbenv init -)"` at the end of the profile's text.
- Press `Control` + `x` to exit and save the file. You'll see a message at the bottom of your screen asking whether you want to save the file.
- Press the `y` key on your keyboard to specify yes, you want to save.
- Press `Enter` to finish saving the file and exit nano.
{% endcapture %}
{:#bash}
{% include bootstrap/alert.md text=bash color="success" %}

**Install Ruby**
- Back in your terminal, install the latest version of ruby by copy/pasting or writing, `rbenv install 2.7.1` and pressing `Enter`.

{:.alert .alert-warning .my-3}
Note: 2.7.1 is the latest solid version as of this writing; if you are reading this past August 2020, you may need to check the "Stable Releases" section on [the download Ruby page](https://www.ruby-lang.org/en/downloads/){:target="_blank" rel="noopener"} and install the latest stable version.

- Now let's set that version as your global Ruby version by entering `rbenv global 2.7.1` into the terminal prompt and pressing `Enter`.
- Finally, we're going to rehash, just to be safe: copy and paste the command `rbenv rehash` into your prompt and pressing `Enter`.
- Now let's see if that worked.
    - Quit your terminal by right clicking (`Control + click`) its icon in your applications menu, and selecting `Quit` from the options that appear.
    - Then reopen your terminal by clicking `Command (⌘) + Spacebar`, typing `terminal` into the spotlight box that appears, and pressing `Enter`.
    - Type `ruby -v` into the terminal prompt, and press `Enter`.
    - If your terminal indicates that you have Ruby 2.7.0 or higher installed, you've done it!

{:.alert .alert-danger}
If this installation did not work, see our more detailed guide, [How to Install Ruby on a Mac](https://lib-static.github.io/howto/howtos/installrubymac.html){:target="_blank" rel="noopener"}, check out the [Jekyll install on mac docs](https://jekyllrb.com/docs/installation/macos/), or try Googling any error message or other hindrance you encountered.
{% endcapture %}
{% include bootstrap/card.md text=mac-ruby header="Ruby on Mac" %}

{% capture ruby-lin %}
Ruby can be installed via most distro's repositories or [snap package](https://snapcraft.io/ruby){:target="_blank" rel="noopener"}, however, it is more up-to-date and best practice to use a version manager such as [RVM](http://rvm.io/){:target="_blank" rel="noopener"} or [rbenv](https://github.com/rbenv/rbenv){:target="_blank" rel="noopener"}.

- First, ensure you have build tools Make and GCC installed (on Ubuntu get them with `sudo apt install build-essential`).
- Follow the instructions on [RVM install](https://rvm.io/rvm/install){:target="_blank" rel="noopener"}.
- For more information and other methods, see [How to Install Ruby on Linux](https://lib-static.github.io/howto/howtos/installrubylinux.html){:target="_blank" rel="noopener"}.
{% endcapture %}
{% include bootstrap/card.md text=ruby-lin header="Ruby on Linux" %}
