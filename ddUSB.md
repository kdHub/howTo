- open terminal
- identify your usb drive
```lsusb -v``` or
```df -h | less``` use q to quit df
- format ```sudo mkfs.ext4 /dev/sdx```
- dd to usb drive once identified
```dd bs=4M if=tails-i386-2.5.iso of=/dev/sdb && sync```
