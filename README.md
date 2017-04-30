# MyLinux

## Packages

### Multi-tab terminal

```shell
sudo apt-get install xdotool
```

ctrl+shift+t - open new tab

### Copying to clipboard
```shell
sudo apt-get install xsel
xsel --clipboard < new-clipboard-contents.txt
xsel --clipboard > current-clipboard-contents.txt
```

### Unzip
```
sudo apt-get install unzip
unzip file.zip -d destination_folder
```

### SDKMAN
```
sudo apt install unzip
curl -s "https://get.sdkman.io" | bash
source "$HOME/.sdkman/bin/sdkman-init.sh"

```

### Gradle (need to install SDKMAN first)
```
sdk install gradle 3.4.1
```
