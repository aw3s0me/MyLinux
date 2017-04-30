# Install Node.js
## Distro version (probably 4.*)
```
sudo apt-get update
sudo apt-get install nodejs
sudo apt-get install npm
```
## New versions (6.*)
```
curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -
sudo apt-get install -y nodejs
```

# Install most used CLI
## 1. Fix permissions (EACCES error)
taken from: https://docs.npmjs.com/getting-started/fixing-npm-permissions
### Option 1. Fixing permissions
```
npm config get prefix
sudo chown -R $(whoami) $(npm config get prefix)/{lib/node_modules,bin,share}
```
### Option 2. Change npm directory
    Make a directory for global installations:

     mkdir ~/.npm-global

    Configure npm to use the new directory path:

     npm config set prefix '~/.npm-global'

    Open or create a ~/.profile file and add this line:

     export PATH=~/.npm-global/bin:$PATH

    Back on the command line, update your system variables:

     source ~/.profile
## Angular CLI
`npm install -g @angular/cli`
## Typescript
`npm install -g typescript`
