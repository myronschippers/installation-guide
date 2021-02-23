# Installation Guide

Local development setup installation guides.

## Git Version Control on Mac

## Node.js with NVM

Install XCode on MacOS.

```zsh
xcode-select --install
```

Use touch to create a “bash-profile” on your machine.

```zsh
touch ~/.bash_profile
```

Download NVM via...

...wget

```zsh
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.2/install.sh | bash
```

or

...curl

```zsh
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.32.1/install.sh | bash
```

Refresh terminal's command path.

```zsh
source ~/.nvm/nvm.sh
```

**RESATART Terminal**

Check which version of NVM got installed.

```zsh
nvm --version
```

## Using NVM

Check available node Versions with NVM

```zsh
nvm ls-remote
```

Install specific version of Node.js

```zsh
nvm install 14.15.5
```

Check install of Node & NPM

```zsh
node -v
```

```zsh
npm -v
```

## PostgreSQL

```
brew install postgresql
```

```
brew services start postgresql
psql postgres
```

update postgresql version

```
brew upgrade postgresql
brew postgresql-upgrade-database
brew services restart postgresql
```

Go Into PostgreSQL

```
psql postgres
```

Download Database GUI
[TablePlus](https://tableplus.com/)

## Postico

```
brew install --cask postico
```

## VSCode Extensions

```
Bracket Pair Colorizer 2

Code Spell Checker

Color Highlight

file-icons

Git Blame

Highlight Matching Tag

HTML Format

indent-rainbow

IntelliSense for CSS class names in HTML

lit-html

Live Share

Trailing Spaces

Prettier - Code formatter
```

Open up `settings.json` and add the following after loading the extension "**Prettier - Code formatter**"

```json
{
  "prettier.requireConfig": false,
  "prettier.singleQuote": true,
  "prettier.trailingComma": "es5",
  "prettier.tabWidth": 2,
  "prettier.ignorePath": "~/.prettier.ignore",

  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true,
  "editor.tabSize": 2,
  "editor.detectIndentation": false
}
```

## Python Environment on Local MacOS

**Referenced:**

- [The right and wrong way to set Python 3 as default on a Mac](https://opensource.com/article/19/5/python-3-default-mac)
- [pyenv auto installer](https://github.com/pyenv/pyenv-installer)

**Installation ERRORs**

- [Python Development on macOS with pyenv](https://medium.com/python-every-day/python-development-on-macos-with-pyenv-2509c694a808)
- [How to set up Python environment on your Mac](https://levelup.gitconnected.com/how-to-set-up-python-environment-on-your-mac-560ebf9324ed)
- [Install Issue Log 1643](https://github.com/pyenv/pyenv/issues/1643)
- [Install Issue Log 1737](https://github.com/pyenv/pyenv/issues/1737)

According to [Moshe Zadka](https://opensource.com/users/moshez)...

> "The basic premise of all Python development is to never use the system Python. You do not want the Mac OS X 'default Python' to be 'python3.' You want to never care about default Python."

Should install and use Python for local development using [pyenv](https://github.com/pyenv/pyenv).

In this I am using **Homebrew**. There are other ways but I like my **Homebrew**.

### Step 1. Install pyenv

```shell
$ brew update
```

```shell
$ brew install pyenv
🍺  /usr/local/Cellar/pyenv/1.2.10: 634 files, 2.4MB
```

### Step 2. Install Python

```shell
$ pyenv install 3.7.3
python-build: use openssl 1.0 from homebrew
python-build: use readline from homebrew
Downloading Python-3.7.3.tar.xz...
-> https://www.python.org/ftp/python/3.7.3/Python-3.7.3.tar.xz
Installing Python-3.7.3...
## further output not included ##
```

### Step 3. Set your global default

```
$ pyenv global 3.7.3
# and verify it worked
$ pyenv version
3.7.3 (set by /Users/mbbroberg/.pyenv/version)
```


