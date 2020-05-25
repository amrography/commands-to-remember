# Ubuntu <!-- omit in toc -->

- [Global](#global)
  - [Login to my remote desktop](#login-to-my-remote-desktop)
  - [Switch to non-GUI Environment](#switch-to-non-gui-environment)
  - [Full update & upgrade](#full-update--upgrade)
  - [Uninstall package](#uninstall-package)
  - [Switch between versions](#switch-between-versions)
  - [Delete old linux image](#delete-old-linux-image)
- [Php](#php)
  - [Set default php](#set-default-php)
  - [Install specific php module with version](#install-specific-php-module-with-version)
  - [Activate php module](#activate-php-module)
  - [Activate apache2 with php version](#activate-apache2-with-php-version)

## Global

### Login to my remote desktop

```bash
ssh username@xxx.xxx.xxx.xxx
```

### Switch to non-GUI Environment

`ctrl + alt + f2`

### Full update & upgrade

```zsh
sudo apt-get update
sudo apt-get upgrade
sudo apt dist-upgrade
sudo do-release-upgrade
```

### Uninstall package

```bash
# List all packages if you want
dpkg --list 'gi*'

# Just remove
sudo apt-get remove --purge gimp

# Or compete remove
sudo apt-get purge --auto-remove gimp
```

### Switch between versions

```sh
sudo update-alternatives --set php /usr/bin/php5.6
```

### Delete old linux image
  
```bash
# Check current image name
uname -r

# List all images
dpkg --list 'linux-image-*'

# Remove all the kernels below the current one
sudo apt-get purge linux-image-x.x.x.x-genrice

# Update gurb2
sudo update-gurb2

# Reboot
sudo reboot
```

---

## Php

### Set default php

```shell
sudo update-alternatives --set php /usr/bin/php5.6
```

### Install specific php module with version

`sudo apt-get install php7.3-dom`

### Activate php module

`sudo phpenmod mbstring`

### Activate apache2 with php version

```shell
sudo a2enmod php7.1
sudo systemctl restart apache2
```
