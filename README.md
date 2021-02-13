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
