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
```
sudo vim ~/.bashrc
Then execute the command below to make the change take effect:
source ~/.bashrc
```
# Node Js Update
```
sudo npm cache clean -f
sudo npm install -g n
sudo n stable
```
# Sqlite3 browser
```
Ubuntu and Derivatives
Stable release

For Ubuntu and derivaties, @deepsidhu1313 provides a PPA with our latest release here:

    https://launchpad.net/~linuxgndu/+archive/ubuntu/sqlitebrowser

To add this ppa just type in these commands in terminal:

   sudo add-apt-repository -y ppa:linuxgndu/sqlitebrowser

Then update the cache using:

   sudo apt-get update

Install the package using:

   sudo apt-get install sqlitebrowser

Ubuntu 14.04.X, 15.04.X, 15.10.X and 16.04.X are supported for now (until Launchpad decides to discontinue building for any series).

Ubuntu Precise (12.04) and Utopic (14.10) are not supported:

    Precise doesn't have a new enough Qt package in its repository by default, which is a dependency
    Launchpad doesn't support Utopic any more, as that has reached its End of Life
```
