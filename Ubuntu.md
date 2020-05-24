# Ubuntu <!-- omit in toc -->

- [Login to my remote desktop](#login-to-my-remote-desktop)
- [Switch to non-GUI Environment](#switch-to-non-gui-environment)
- [Full update & upgrade](#full-update--upgrade)
- [Uninstall package](#uninstall-package)
- [Switch between versions](#switch-between-versions)
- [Delete old linux image](#delete-old-linux-image)

---

## Login to my remote desktop

```bash
ssh username@xxx.xxx.xxx.xxx
```

---

## Switch to non-GUI Environment

**ctrl** + **alt** + **f2**

---

## Full update & upgrade

```zsh
sudo apt-get update
sudo apt-get upgrade
sudo apt dist-upgrade
sudo do-release-upgrade
```

---

## Uninstall package

```bash
# List all packages if you want
dpkg --list 'gi*'

# Just remove
sudo apt-get remove --purge gimp

# Or compete remove
sudo apt-get purge --auto-remove gimp
```

---

## Switch between versions

```sh
sudo update-alternatives --set php /usr/bin/php5.6
```

---

## Delete old linux image
  
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
