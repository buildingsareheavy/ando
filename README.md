# ANDO
Ando is a shell script to set up a macOS laptop for clean and simple front-end web development environment.

![Tadao Ando](assets/ando.jpg)
> [Tadao Ando](https://en.wikipedia.org/wiki/Tadao_Ando) is a a Japanese self-taught architect whose style emphasizing nothingness and empty space to represent the beauty of simplicity.

Ando can be run multiple times on the same machine safely. It installs, upgrades, or skips packages based on what is already installed on the machine.

## Install

Download the script:

```sh
git clone git@github.com/buildingsareheavy/ando.git && cd ando
```

Review the script (please don't run scripts you don't understand):

```sh
less concrete
```

concrete:

```sh
cd ando
./concrete 2>&1 | tee ~/concrete.log
```
Just follow the prompts and you’ll be fine. 👌

:warning: Warning: I advise against running [this script](concrete) unless you understand what it’s doing to your computer.

I created this based on my own preferences; your mileage may vary.

Once the script is done, quit and relaunch Terminal.

It is highly recommended to run the script regularly to keep your computer up to date.

Your last `ando` run will be saved to `~/concrete.log`. To review it, run `less ~/concrete.log`.

That's it! 

## What it sets up
The setup process will install:

<details>
<summary>Basic Tools:</summary>

* [XCode Command Line Tools](https://developer.apple.com/xcode/downloads/) for developer essentials.
* [Bash-it](https://github.com/Bash-it/bash-it/), for a more powerful bash.
* [Git](https://git-scm.com/) for version control
* [Homebrew](http://brew.sh/) for managing operating system libraries.
</details>

<details>
<summary>Package Managers:</summary>

* [NVM](https://github.com/creationix/nvm/) for managing and installing multiple versions of [Node.js](http://nodejs.org/) and [npm](https://www.npmjs.org/)
* [Rbenv](https://github.com/sstephenson/rbenv) for managing versions of Ruby
* [Yarn](https://yarnpkg.com/en/) for managing JavaScript packages
</details>

<details>
<summary>CLI Tools & Utilities:</summary>

* [Gulp](https://gulpjs.com/) the streaming build system
* [Hub](http://hub.github.com/) for interacting with the GitHub API
* [mas](https://github.com/mas-cli/mas) Mac App Store command line interface


</details>

### Apps


<details>
<summary>Development</summary>

* [Hyper](https://hyper.is/) for an alternative terminal.
* [Visual Studio Code](https://code.visualstudio.com/) IDE
</details>


<details>
<summary>Utilities</summary>

* [1Password](https://1password.com/) for password management.
* [Dropbox](https://www.dropbox.com) for cloud file storage.
* [Divvy](http://mizage.com/divvy/) for better window management.
* [Encrypto](https://macpaw.com/encrypto) for securing files.
* [ExpressVPN](https://www.expressvpn.com/) for privacy.
* [HyperDock](https://bahoom.com/hyperdock/)
* [Karabiner](https://pqrs.org/osx/karabiner/) for keyboard mapping.
* [Renamer](https://renamer.com/) for easy file renaming.
</details>

<details>
<summary>Miscellaneous</summary>

* [Spotify](https://www.spotify.com/) for music.
</details>

<details>
<summary>Browsers</summary>

* [Chrome](https://www.google.com/chrome/browser/desktop/) for fast and free web browsing.
* [Firefox](https://www.mozilla.org/en-US/firefox/new/) for web browsing and testing.
</details>

<sub>See [`materials`](materials) for the full list of apps that will be installed. Adjust it to your personal taste.</sub>

It should take less than 20 minutes to install (depends on your machine).

## ✨ Just add `~/.ornamentation`

Your `~/.ornamentation` is added at the end of the `ando` script. Put your customizations there.
For example:

```sh
#!/usr/bin/env bash

SETUP_ROOT=$HOME/.setup

NERDFONTS_RELEASE=$(curl -L -s -H 'Accept: application/json' https://github.com/ryanoasis/nerd-fonts/releases/latest)
NERDFONTS_VERSION=$(get_github_version $NERDFONTS_RELEASE)

DIRECTORIES=(
    $HOME/Desktop/code
    $HOME/Desktop/design
    $HOME/Desktop/*dump
    $HOME/Desktop/GIFs
    $HOME/Desktop/projects
    $HOME/Desktop/screenshots
)

NERDFONTS=(
    SpaceMono
    Hack
    AnonymousPro
    Inconsolata
)

step "Making directories…"
for dir in ${DIRECTORIES[@]}; do
    mkd $dir
done

step "Installing fonts…"
for font in ${NERDFONTS[@]}; do
    if [ ! -d ~/Library/Fonts/$font ]; then
        printf "${indent}  [↓] $font "
        wget -P ~/Library/Fonts https://github.com/ryanoasis/nerd-fonts/releases/download/$NERDFONTS_VERSION/$font.zip --quiet;unzip -q ~/Library/Fonts/$font -d ~/Library/Fonts/$font
        print_in_green "${bold}✓ done!${normal}\n"
    else
        print_muted "${indent}✓ $font already installed. Skipped."
    fi
done
```

Write your customizations such that they can be run safely more than once.
See the `concrete` script for examples.

`ando` functions such as `step` and `link` can be used in your `~/.ornamentation`.

## Known Issues
Cask does not recognize applications installed outside of Homebrew Cask – in the case that the script fails, you can either remove the application from the install list or uninstall the application causing the failure and try again.

## Acknowledgements

This code is heavily based on and copied from: [Mina Markham's](https://github.com/minamarkham) [formation](https://github.com/minamarkham/formation)


## 📜  License

Ando is free software, and may be redistributed under the terms specified in the [LICENSE] file.

[LICENSE]: LICENSE
