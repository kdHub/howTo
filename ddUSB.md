- open terminal
- identify your usb drive
```lsusb -v``` or
```df -h | less``` use q to quit df
- format ```sudo mkfs.ext4 /dev/sdx```
- dd to usb drive once identified
```dd bs=4M if=tails-i386-2.5.iso of=/dev/sdb && sync```

A few handy sample usages with pv and less typing or more progress then other answers:

First you will need to install pv, with the command:

sudo apt-get install pv
Then some examples are:

pv -n /dev/urandom | dd of=/dev/null
pv -tpreb source.iso | dd of=/dev/BLABLA bs=4096 conv=notrunc,noerror
Note: the first sample is 5 characters less typing then dd if=/dev/urandom | pv | dd of=/dev/null.
