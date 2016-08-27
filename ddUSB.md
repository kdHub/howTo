- open terminal
- identify your usb drive
```lsusb -v```
```df -h | less```
- dd to usb drive once identified
```dd bs=4M if=tails-i386-2.5.iso of=/dev/sdb && sync```
