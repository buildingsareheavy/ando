# ANDO

A shell script for a clean and simple front-end web development environment on macOS.

![Tadao Ando](assets/ando.jpg)

> [Tadao Ando](https://en.wikipedia.org/wiki/Tadao_Ando) is a a Japanese self-taught architect whose style emphasizing nothingness and empty space to represent the beauty of simplicity.
>
> This script was inspired by his philosophy.

Ando is meant to run multiple times on the same machine. It installs, upgrades, or skips depending on what is already installed.

## Install

Download:

```sh
git clone https://github.com/buildingsareheavy/ando.git && cd ando
```

Review: (please don't run scripts you don't understand):

```sh
less blueprints
```

Run:

```sh
sh goAndo
```

Or Run with log:

```sh
sh goAndo 2>&1 | tee ~/ando.log
```

Your last `sh goAndo` run will be saved to `~/ando.log`. To review it, run `less ~/ando.log`.

Check and debug the log:

```sh
less ~/ando.log
```

**Warning: I advise against running [this script](goAndo) unless you understand what it’s doing to your computer.**

It is highly recommended to run the script regularly to keep your computer up to date.

## What it sets up

The setup process will install:

<details>
<summary>Basic Tools</summary>

- [XCode Command Line Tools](https://developer.apple.com/xcode/downloads/) for developer essentials.
- [Bash-it](https://github.com/Bash-it/bash-it/), for a more powerful bash.
- [NVM](https://github.com/creationix/nvm/) for managing and installing multiple versions of [Node.js](http://nodejs.org/) and [npm](https://www.npmjs.org/)
- [Homebrew](http://brew.sh/) for managing operating system libraries.
  </details>

<details>
<summary>Homebrew: Brews</summary>

- [Git](https://git-scm.com/) for version control.
- [Tig](https://jonas.github.io/tig/) is a text interface for Git repositories.
- [Mas](https://github.com/mas-cli/mas/) is a Mac App Store command line interface.
- [wget](https://www.gnu.org/software/wget/) is an internet file retriever.
- [Hub](https://hub.github.com/) adds GitHub support to git on the command-line.
- [ImageOptim-CLI](https://github.com/JamieMason/ImageOptim-CLI) to make batch optimisation of images part of your automated build process.
- [Rbenv](https://github.com/sstephenson/rbenv/) for managing versions of Ruby.
- [Yarn](https://yarnpkg.com/en/) for managing JavaScript packages.
- [ZSH](https://www.zsh.org/) is a UNIX shell (command interpreter).
- [ZSH Syntax Highlighting](https://github.com/zsh-users/zsh-syntax-highlighting/) Fish shell like syntax highlighting for zsh.
- [TheFuck](https://github.com/nvbn/thefuck/) helps programatically correct mistyped console commands.
- [WP-CLI](https://wp-cli.org/) is the command-line interface for WordPress. You can update plugins, configure multisite installations and much more, without using a web browser.
  </details>

<details>
<summary>Homebrew: Casks</summary>

- [Affinity Photo Beta](https://affinity.serif.com/en-us/photo/) is a raster graphics editor.
- [Affinity Designer Beta](https://affinity.serif.com/en-us/designer/) is a vector graphics editor.
- [Firefox](https://www.mozilla.org/en-US/firefox/new/) for web browsing and testing.
- [Firefox Developer Edition](https://www.mozilla.org/en-US/firefox/developer/) is my main web browser for development. Best CSS tools built in. Read more [here](https://www.smashingmagazine.com/2019/10/guide-new-experimental-css-devtools-firefox/).
- [Google Chrome](https://www.google.com/chrome/browser/desktop/) for fast and free web browsing.
- [Hyper](https://hyper.is/) for an alternative terminal.
- [ImageOptim](https://imageoptim.com/mac) to make batch optimisation of images part of your automated build process.
- [MAMP](https://www.mamp.info/en/) for PHP / Wordpress development.
- [Microsoft Edge Dev](https://developer.microsoft.com/en-us/microsoft-edge/) for testing.
- [Spotify](https://www.spotify.com/) for music.
- [Visual Studio Code](https://code.visualstudio.com/) IDE.
- [FONT: Dejavu Sans Mono](https://github.com/Homebrew/homebrew-cask-fonts/blob/master/Casks/font-dejavusansmono-nerd-font-mono.rb) for command-line font. Has glyph support for `git` and works well with [PowerLevel10K](https://github.com/romkatv/powerlevel10k) (a ZSH theme).
- [FONT: Victor Mono](https://github.com/Homebrew/homebrew-cask-fonts/blob/master/Casks/font-victor-mono.rb) for text editor font. Supports ligatures and has a nice cursive italic font, similar to [Dank Mono](https://dank.sh/) or [Fira Code](https://github.com/tonsky/FiraCode).
  </details>

<details>
<summary>App Store Apps</summary>

- [Amphetamine](https://apps.apple.com/us/app/amphetamine/id937984704?mt=12) is a powerful keep-awake utility.
- [Be Focused - Focus Timer](https://code.visualstudio.com/) is a pomodoro style focus timer for work and study.
- [Viper FTP Lite](https://apps.apple.com/us/app/viper-ftp-lite-ftp-client/id1001007066?mt=12) is a User-friendly and reliable Mac FTP/FTPS/SFTP/WebDav/AS3 client.
  </details>

<details>
<summary>NPM Packages</summary>

- [11ty](https://github.com/11ty/eleventy/) is a simpler static site generator.
- [ESLint](https://eslint.org/) linting utility for JavaScript.
- [Gatsby](https://www.gatsbyjs.org/) a static site generator built with React.
- [Gridsome](https://gridsome.org/) a static site generator built with Vue.
- [Gulp](https://gulpjs.com/) a task/build runner for development.
- [ImageOptim-CLI](https://github.com/JamieMason/ImageOptim-CLI) to make batch optimisation of images part of your automated build process.
- [Netlify](https://cli.netlify.com/) lets you deploy sites or configure continuous deployment straight from the command line.
- [MAMP-CLI](https://www.npmjs.com/package/mamp-cli) a command line interface for working with [MAMP](https://www.mamp.info/de/). It can start and stop your MAMP, but also easily switch the document root so that you can switch projects easily by using a favorite list.
- [Pa11y](https://pa11y.org/) a command-line interface which loads web pages and highlights any accessibility issues it finds. Useful for when you want to run a one-off test against a web page.
- [VSCE](https://github.com/microsoft/vscode-vsce) - The Visual Studio Code Extension Manager.
- [Vue-CLI](https://cli.vuejs.org/) for quickly scaffolding Single Page Applications.
- [yo](https://github.com/yeoman/yo) CLI tool for running [Yeoman](https://yeoman.io/) generators.
  </details>

<details>
<summary>ZSH Settings <span>(Prompted): For Initial Setup Only</span></summary>

- [Oh My ZSH](https://github.com/robbyrussell/oh-my-zsh/) a framework for managing your zsh configuration.
- [Powerlevel10K](https://github.com/romkatv/powerlevel10k) a ZSH theme.
  </details>

<details>
<summary>Dotfiles <span>(Prompted)</span></summary>

- **.zshrc** for customizing your [Oh-My-ZSH!](https://ohmyz.sh/) settings.
- **.hyper.js** for customizing your [Hyper](https://hyper.is/) terminal. _This is where the fonts color themes are held. Current theme is [New Moon](https://github.com/Tmeister/hyperterm-new-moon-theme)_.
- **.p10k.zsh** for customizing your [Powerlevel10K](https://github.com/romkatv/powerlevel10k) ZSH theme. _This is where the terminal theme is held. Like the arrows and git icons._
  </details>

<sub>See [`materials`](materials) for the full list of apps that will be installed. Adjust it to your personal taste.</sub>

It should take less than 20 minutes to install (depends on your machine).

## Post-Install

Open _VS Code_ and install the [Settings Sync](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync) extension.

In the extension settings under _Configuration_ click the _Login With Github_ button and follow instructions to connect.

**If Needed:**
Go to [https://gist.github.com/](https://gist.github.com/) and look for a gist called "_Cloud Settings_". Copy the ID in the URL to paste into "_Gist ID_".

This should sync all of your VSCode settings, extensions and preferences.

Open command palette and run `Sync: Download Settings`.

## Known Issues

If you are doing a completely fresh install and have not installed Xcode already, it will prompt you to do so and possibly say that Ando has failed. Install Xcode and run the script again.

Cask does not recognize applications installed outside of Homebrew Cask – in the case that the script fails, you can either remove the application from the install list or uninstall the application causing the failure and try again.

## Acknowledgements

Code was inspired, copied and modified from: [Mina Markham's](https://github.com/minamarkham) [formation](https://github.com/minamarkham/formation)

## 📜 License

Ando is free software, and may be redistributed under the terms specified in the [LICENSE] file.

[license]: LICENSE
