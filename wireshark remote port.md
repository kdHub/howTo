ssh -l root 66170510a3cf.sn.mynetname.net tcpdump -U -s0 -w - -i eth0 'port 22' | wireshark -k -i -

using plink and windows
https://ask.wireshark.org/questions/23609/remote-capture-via-ssh-and-pipe
