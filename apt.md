# Install
```
sudo apt install <package>
```
# Location of install package
```
sudo apt content <package>
```
# Find dependencies of package
```
sudo apt depends <package>
```
# Search for package
```
sudo apt search <package>
```
# View info about package
```
sudo apt show <package>
```
# Verify package for any broken dependency
During package installation can get errors because of broken package dependencies

So can check using command this
```
sudo apt check firefox
```
# List of recommended missing packages for given package
```
sudo apt recommends <package>
```
# Check installed package version
```
sudo apt version <package>
```
# Update system packages
Helps to download and update package lists from different repos
```
sudo apt update
```
# Upgrade system
Installs new versions for all packages in system
```
sudo apt upgrade
```
# Remove unused packages
After removing package, some dependencies can remain => use autoremove to remove them
```
sudo apt autoremove
```
# Clean old repo of downloaded packages
```
sudo apt autoclean
or 
sudo apt clean
```
# Remove package
```
sudo apt purge <package>
```
# Install .deb package
```
sudo apt deb <package.deb>
```
