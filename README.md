# Linux Administration

Linux is a tried-and-true, open-source operating system released in 1991 for computers, but its use has expanded to underpin systems for cars, phones, web servers and, more recently, networking gear

<!-- ### SSH Linux

[SSH](./ssh/README.md)

### Check if a server is up and running

[Server Up Running](./server-up-running/README.md)

### Unix-Linux-Shell-Variables

[Unix-Linux-Shell-Variables](./Unix-Linux-Shell-Variables/README.md)

### Parsing bash script options with getopts

[Parsing-bash-script-options-getopts](./Parsing-bash-script-options-getopts/README.md)

### Cloud-Network-Monitoring

[Cloud-Network-Monitoring](./Cloud-Network-Monitoring/README.md) -->




----------------------------------------------------------------


## Network-Tools

1. #### [Traceroute](./Traceroute/README.md)
    Traceroute is a network diagnostic tool used to track in real-time the pathway taken by a packet on an IP network from source to destination, reporting the IP addresses of all the routers it pinged in between. Traceroute also records the time taken for each hop the packet makes during its route to the destination.

    [caveats-of-popular-network-tools-traceroute](https://www.thousandeyes.com/blog/caveats-of-popular-network-tools-traceroute/)


1. #### [NetFlow](./NetFlow/README.md)
    NetFlow is a protocol developed by Cisco Systems to record all IP traffic flows traversing a router or switch that is NetFlow enabled. It generates statistics inside these devices at the interface level and sends this information in UDP-based flow records to an external element called a flow collector—a program running on a server where the traffic statistics can be stored for load balancing analysis.

1. #### [SNMP](https://www.thousandeyes.com/learning/techtorials/snmp-simple-network-management-protocol)

1. #### [Synthetic APM](https://www.thousandeyes.com/learning/techtorials/synthetic-apm)

1. #### [ICMP](https://www.thousandeyes.com/blog/limitations-of-icmp-based-network-measurements/)

1. #### [Spotlight](https://www.quest.com/products/spotlight-on-unix-linux/)

    Real-time diagnostics of Unix/Linux problems

    Identify congested areas and swiftly respond to issues before they impact users with this performance and diagnostics resolution tool. Get real-time data flow from Solaris, AIX, HPUX, and Unix/Linux operating systems (including I/O subsystem, cache and kernel information). Create thresholds with an automatically generated set of normal baseline activity for each system, and send alerts about impending problems.


1. #### [SolarWinds](https://www.troublesnoop.com/what-is-solarwinds-tool/)


1. #### [Linux visudo command](https://www.computerhope.com/unix/visudo.htm)


1. #### [namespaces(7) — Linux manual page](https://man7.org/linux/man-pages/man7/namespaces.7.html)


1. #### [CGROUPS](https://www.kernel.org/doc/Documentation/cgroup-v1/cgroups.txt)

1. #### [Linux Extended BPF (eBPF) Tracing Tools](https://www.brendangregg.com/ebpf.html)



-------------------------

## Pentesting Tools



-------------------------

### Documentation

1. [Syslog and Klog](https://annvix.com/syslog_and_klog#:~:text=syslogd%20is%20a%20system%20logging,via%20the%20%2Fetc%2Fsyslog)

2. [The magic behind configure, make, make install](https://thoughtbot.com/blog/the-magic-behind-configure-make-make-install)

-------------------------

### Questions

1. What's the difference of dmesg output and /var/log/messages ?

    dmesg prints the contents of the ring buffer. This information is also sent in real time to syslogd or klogd, when they are running, and ends up in /var/log/messages; when dmesg is most useful is in capturing boot-time messages from before syslogd and/or klogd started, so that they will be properly logged.

    [whats-the-difference-of-dmesg-output-and-var-log-messages](https://unix.stackexchange.com/questions/35851/whats-the-difference-of-dmesg-output-and-var-log-messages)

2. How To Solve “XFS: Filesystem has duplicate UUID – can’t mount”

    $ sudo mount -o rw,nouuid /dev/sda3  /mnt

    $ sudo xfs_admin -U generate /dev/sda3
