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
less blueprints
```

Run the script:

```sh
// Basic Setup
sh goAndo

// Log Setup
sh goAndo 2>&1 | tee ~/ando.log
```

Just follow the prompts and you’ll be fine. 👌

:warning: Warning: I advise against running [this script](goAndo) unless you understand what it’s doing to your computer.

Once the script is done, quit and relaunch Terminal.

It is highly recommended to run the script regularly to keep your computer up to date.

Your last `sh goAndo` run will be saved to `~/ando.log`. To review it, run `less ~/ando.log`.

That's it!

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
- [Rbenv](https://github.com/sstephenson/rbenv/) for managing versions of Ruby.
- [Yarn](https://yarnpkg.com/en/) for managing JavaScript packages.
- [ZSH](https://www.zsh.org/) is a UNIX shell (command interpreter).
- [ZSH Syntax Highlighting](https://github.com/zsh-users/zsh-syntax-highlighting/) Fish shell like syntax highlighting for zsh.
- [TheFuck](https://github.com/nvbn/thefuck/) helps programatically correct mistyped console commands.
  </details>

<details>
<summary>Homebrew: Taps</summary>

- [homebrew/cask-versions](https://github.com/Homebrew/homebrew-cask-versions) Alternate versions of [Homebrew](https://brew.sh/) Casks.  
  **This is so we can install Firefox Developer Edition**
- [homebrew/cask-fonts](https://github.com/Homebrew/homebrew-cask-fonts) Casks of Fonts.
  **This is so we can install Powerline and Nerd Fonts later**
  </details>

<details>
<summary>Homebrew: Casks</summary>

- [Firefox](https://www.mozilla.org/en-US/firefox/new/) for web browsing and testing.
- [Firefox Developer Edition](https://www.mozilla.org/en-US/firefox/developer/) is my main web browser for development. Best CSS tools built in. Read more [here](https://www.smashingmagazine.com/2019/10/guide-new-experimental-css-devtools-firefox/).
- [Franz](https://meetfranz.com/) for messaging.
- [Google Chrome](https://www.google.com/chrome/browser/desktop/) for fast and free web browsing.
- [Hyper](https://hyper.is/) for an alternative terminal.
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
- [Netlify](https://cli.netlify.com/) lets you deploy sites or configure continuous deployment straight from the command line.
- [Pa11y](https://pa11y.org/) a command-line interface which loads web pages and highlights any accessibility issues it finds. Useful for when you want to run a one-off test against a web page.
- [VSCE](https://github.com/microsoft/vscode-vsce) - The Visual Studio Code Extension Manager.
- [Vue-CLI](https://cli.vuejs.org/) for quickly scaffolding Single Page Applications.
- [WP-CLI](https://wp-cli.org/) is the command-line interface for WordPress. You can update plugins, configure multisite installations and much more, without using a web browser.
- [yo](https://github.com/yeoman/yo) CLI tool for running [Yeoman](https://yeoman.io/) generators.

  </details>

<details>
<summary>Dotfiles</summary>

- **.zshrc** for customizing your [Oh-My-ZSH!](https://ohmyz.sh/) settings.
- **.hyper.js** for customizing your (Hyper)[https://hyper.is/] terminal. _This is where the fonts color themes are held. Current theme is [New Moon](https://github.com/Tmeister/hyperterm-new-moon-theme)_.
- **.p10k.zsh** for customizing your (Powerlevel10K)[https://github.com/romkatv/powerlevel10k] ZSH theme. _This is where the terminal theme is held. Like the arrows and git icons._

-

  </details>

<sub>See [`materials`](materials) for the full list of apps that will be installed. Adjust it to your personal taste.</sub>

It should take less than 20 minutes to install (depends on your machine).

## Post-Install

Open _VS Code_ and install the [Settings Sync](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync) extension.

In the extension settings under _Configuration_ click the _Login With Github_ button and follow instructions to connect.

**If Needed:**
Go to [https://gist.github.com/](https://gist.github.com/) and look for a gist called "_Cloud Settings_". Copy the ID in the URL to paste into "_Gist ID_".

This should sync all of your VSCode settings, extensions and preferences.

## Known Issues

Cask does not recognize applications installed outside of Homebrew Cask – in the case that the script fails, you can either remove the application from the install list or uninstall the application causing the failure and try again.

## Acknowledgements

This code is heavily based on and copied from: [Mina Markham's](https://github.com/minamarkham) [formation](https://github.com/minamarkham/formation)

## 📜 License

Ando is free software, and may be redistributed under the terms specified in the [LICENSE] file.

[license]: LICENSE
