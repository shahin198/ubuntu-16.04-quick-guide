# ubuntu-16.04-quick-guide
# Makefile tutorial
https://www.youtube.com/watch?v=i3tYp88YHbI

# how to set environment variables
```
nano .profile
nano .bashrc
sudo nano /etc/environment
```

# Clean
```
sudo apt autoclean
sudo apt-get clean
sudo apt autoremove

```
# Sublime text3 editor
```
wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -
echo "deb https://download.sublimetext.com/ apt/stable/" | sudo tee /etc/apt/sources.list.d/sublime-text.list
sudo apt-get update
sudo apt-get install sublime-text
```
# audio reset
```
sudo alsa force-reload
```
# view GPU Detail
```
nvidia-smi
```
Reader 1: Chicony HP Skylab USB Smartcard Keyboard [HP Skylab Smartcard Reader] (18031600000399) 01 00
  Card state: Card inserted, 
  ATR: 3B 6E 00 00 80 31 80 66 B1 A3 01 01 21 0A 83 00 90 00

ATR: 3B 6E 00 00 80 31 80 66 B1 A3 01 01 21 0A 83 00 90 00
+ TS = 3B --> Direct Convention
+ T0 = 6E, Y(1): 0110, K: 14 (historical bytes)
  TB(1) = 00 --> VPP is not electrically connected
  TC(1) = 00 --> Extra guard time: 0
+ Historical bytes: 80 31 80 66 B1 A3 01 01 21 0A 83 00 90 00
  Category indicator byte: 80 (compact TLV data object)
    Tag: 3, len: 1 (card service data byte)
      Card service data byte: 80
        - Application selection: by full DF name
        - EF.DIR and EF.ATR access services: by GET RECORD(s) command
        - Card with MF
    Tag: 6, len: 6 (pre-issuing data)
      Data: B1 A3 01 01 21 0A
    Tag: 8, len: 3 (status indicator)
      LCS (life card cycle): 00 (No information given)
      SW: 9000 (Normal processing.)

Possibly identified card (using /home/nybsys/.cache/smartcard_list.txt):
3B 6E 00 00 80 31 80 66 B1 A3 01 01 21 0A 83 00 90 00
	French "Livret A" issued by "La banque postale" (Bank)

# Audio recorder
```
sudo add-apt-repository ppa:audio-recorder/ppa
sudo apt update; sudo apt install audio-recorder
```
# jupyter help line
```
Esc + m cell view markdown
image add
![title](img/picture.png)
and shift +Enter
```
# paint
```
sudo apt-get install kolourpaint4

```
# Screen recoder
```
sudo apt install vokoscreen

```
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
# Pip3 remove
```
sudo apt remove python3-pip
sudo apt purge python3-pip
sudo apt autoremove
```
python3 get-pip.py pip==10.0.1 --user

delete  swapfile
```
sudo swapoff -a -v
```
```
$apt-get install python-pip
$which pip
/usr/bin/pip

$pip install -U pip
$which pip
/usr/bin/pip

$hash -r
$which pip
/usr/local/bin/pip
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
# install .sh
```


Give execute permission to your script:

chmod +x /path/to/yourscript.sh

And to run your script:

/path/to/yourscript.sh

Since . refers to the current directory: if yourscript.sh is in the current directory, you can simplify this to:

./yourscript.sh


```
 # python script run background

Use the shebang line in your python script. Make it executable using the command,

chmod +x test.py

Use no hangup to run a program in background even if you close your terminal.

nohup /path/to/test.py &

Do not forget to use & to put it in background.

To see the process again, use in terminal,

ps ax | grep test.py

