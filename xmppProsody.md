https://prosody.im/download/package_repository

On rasbian i added the source and gpg key. 
```
wget https://prosody.im/files/prosody-debian-packages.key -O- | sudo apt-key add -
```
```
sudo nano /etc/apt/sources.list
```
```
deb http://packages.prosody.im/debian jessie main
```

apt-get update && apt-get upgrade
```
Get:1 http://packages.prosody.im/debian/ jessie/main prosody armhf 0.9.10-1~jessie1 [191 kB]
Fetched 191 kB in 1s (151 kB/s)       
(Reading database ... 50076 files and directories currently installed.)
Preparing to unpack .../prosody_0.9.10-1~jessie1_armhf.deb ...
Unpacking prosody (0.9.10-1~jessie1) over (0.9.7-2+deb8u3) ...
```
