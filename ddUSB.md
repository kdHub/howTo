- open terminal
- identify your usb drive
```lsusb -v``` or
```df -h | less``` use q to quit df
- dd to usb drive once identified
```dd bs=4M if=tails-i386-2.5.iso of=/dev/sdb && sync```

A few handy sample usages with pv and less typing or more progress then other answers:

First you will need to install pv, with the command:

```sudo apt-get install pv```  </br>
Then some examples are:
```
pv -n /dev/urandom | dd of=/dev/null

or

sudo pv -tpreb source.iso | sudo dd of=/dev/BLABLA bs=4096 conv=notrunc,noerror
```
Note: the first sample is 5 characters less typing then dd if=/dev/urandom | pv | dd of=/dev/null.

http://www.cyberciti.biz/faq/linux-unix-dd-command-show-progress-while-coping/
