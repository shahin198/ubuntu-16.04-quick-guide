# ubuntu-16.04-quick-guide
# rpm file install
Run this command to install alien and other necessary packages:
```
    sudo apt-get install alien dpkg-dev debhelper build-essential
```
To convert a package from rpm to debian format, use this command syntax. The sudo may not be necessary, but we’ll include it just in case.
```
    sudo alien packagename.rpm
```
To install the package, you’ll use the dpkg utility, which is the internal package management tool behind debian and Ubuntu.
```
    sudo dpkg -i packagename.deb
```

deb file install..
```
sudo apt install ./packagename.deb
```
# Show all crash
```
ls -l /var/crash/
```
# Remove crash
```
sudo rm /var/crash/*
```
# Solve Pip problem
```
sudo python3 -m pip uninstall pip && sudo apt install python3-pip --reinstall

```
python3 get-pip.py pip==10.0.1 --user

delete  swapfile
```
sudo swapoff -a -v
```
