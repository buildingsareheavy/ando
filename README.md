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

blueprints:

```sh
cd ando

// Basic Setup
sh goAndo

// Login Setup
sh goAndo 2>&1 | tee ~/ando.log
```

Just follow the prompts and you’ll be fine. 👌

:warning: Warning: I advise against running [this script](goAndo) unless you understand what it’s doing to your computer.

I created this based on my own preferences; your mileage may vary.

Once the script is done, quit and relaunch Terminal.

It is highly recommended to run the script regularly to keep your computer up to date.

Your last `sh goAndo` run will be saved to `~/ando.log`. To review it, run `less ~/ando.log`.

That's it!

## What it sets up

The setup process will install:

<details>
<summary>Basic Tools:</summary>

- [XCode Command Line Tools](https://developer.apple.com/xcode/downloads/) for developer essentials.
- [Bash-it](https://github.com/Bash-it/bash-it/), for a more powerful bash.
- [Git](https://git-scm.com/) for version control
- [Homebrew](http://brew.sh/) for managing operating system libraries.
  </details>

<details>
<summary>Package Managers:</summary>

- [NVM](https://github.com/creationix/nvm/) for managing and installing multiple versions of [Node.js](http://nodejs.org/) and [npm](https://www.npmjs.org/)
- [Rbenv](https://github.com/sstephenson/rbenv) for managing versions of Ruby
- [Yarn](https://yarnpkg.com/en/) for managing JavaScript packages
  </details>

<details>
<summary>CLI Tools & Utilities:</summary>

- [Gulp](https://gulpjs.com/) the streaming build system.
- [Hub](http://hub.github.com/) for interacting with the GitHub API.
- [mas](https://github.com/mas-cli/mas) Mac App Store command line interface.

- 11ty

- Gatsby

- Vue

- Gridsome

- Netlify

- WP CLI

</details>

### Apps

<details>
<summary>App Store</summary>

- [Amphetamine](https://apps.apple.com/us/app/amphetamine/id937984704?mt=12) is a powerful keep-awake utility.
- [Be Focused - Focus Timer](https://code.visualstudio.com/) is a pomodoro style focus timer for work and study.
  </details>

<details>
<summary>Development</summary>

- [Hyper](https://hyper.is/) for an alternative terminal.
- [Visual Studio Code](https://code.visualstudio.com/) IDE.
- [MAMP](https://www.mamp.info/en/) for PHP / Wordpress development.
- ZSH because why would you settle for bash?
  </details>

<details>
<summary>Miscellaneous</summary>

- [Spotify](https://www.spotify.com/) for music.
- [Franz](https://meetfranz.com/) for chat.
  </details>

<details>
<summary>Browsers</summary>

- [Firefox Developer Edition](https://www.mozilla.org/en-US/firefox/developer/) is my main web browser for development. It has the best CSS tools built in.
- [Firefox](https://www.mozilla.org/en-US/firefox/new/) for web browsing and testing.
- [Google Chrome](https://www.google.com/chrome/browser/desktop/) for fast and free web browsing.
- [Microsoft Edge Dev](https://developer.microsoft.com/en-us/microsoft-edge/) for testing.

  </details>

<sub>See [`materials`](materials) for the full list of apps that will be installed. Adjust it to your personal taste.</sub>

It should take less than 20 minutes to install (depends on your machine).

## Known Issues

Cask does not recognize applications installed outside of Homebrew Cask – in the case that the script fails, you can either remove the application from the install list or uninstall the application causing the failure and try again.

## Acknowledgements

This code is heavily based on and copied from: [Mina Markham's](https://github.com/minamarkham) [formation](https://github.com/minamarkham/formation)

## 📜 License

Ando is free software, and may be redistributed under the terms specified in the [LICENSE] file.

[license]: LICENSE
