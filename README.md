# Linux Administration

Linux is a tried-and-true, open-source operating system released in 1991 for computers, but its use has expanded to underpin systems for cars, phones, web servers and, more recently, networking gear

## SSH Linux

[SSH](./ssh/README.md)

## Check if a server is up and running

[Server Up Running](./server-up-running/README.md)




### Documentation

[Syslog and Klog](https://annvix.com/syslog_and_klog#:~:text=syslogd%20is%20a%20system%20logging,via%20the%20%2Fetc%2Fsyslog)

-------------------------

#### Questions

1. What's the difference of dmesg output and /var/log/messages ?

 dmesg prints the contents of the ring buffer. This information is also sent in real time to syslogd or klogd, when they are running, and ends up in /var/log/messages; when dmesg is most useful is in capturing boot-time messages from before syslogd and/or klogd started, so that they will be properly logged.

https://unix.stackexchange.com/questions/35851/whats-the-difference-of-dmesg-output-and-var-log-messages

2. How To Solve “XFS: Filesystem has duplicate UUID – can’t mount”

$ sudo mount -o rw,nouuid /dev/sda3  /mnt
$ sudo xfs_admin -U generate /dev/sda3

