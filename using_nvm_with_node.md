NODE JS TIPS
======

USING NVM
------

Go to https://nodejs.org/en/ to check for latest version. It will show latest stable release and latest release.

[NVM Repository](https://github.com/nvm-sh/nvm#install-script)  

```
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.34.0/install.sh | bash
```

```
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
```

```
command -v nvm
```
should out put `nvm` which shows a successful installation  

`nvm ls` will show a list of node installations  

`nvm install 9.11.1`  

`nvm install 8.11.1`  

`nvm alias default 9.11.1` sets default to `node version 9.11.1`  

`nvm use 9.11.1` sets to use `node version 9.11.1`  

`nvm -H` shows full list of commands



