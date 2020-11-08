## Check if a server is up and running

id:3:initdefault:

If the inittab file is absent, create it and name it id:3, save and exit in order to boot into the third run level when you boot into the server, next time. Make use of the init3 command to rapidly set the server’s run level if you do not prefer to reboot after this change. If the server starts to run at init3, the following shell programs can be used to monitor what is happening inside.

1. iostat: Monitor the storage subsystem functioning like the disk utilization, Read/Write rate, etc.

2. meminfo: Memory information

3. free: Memory overview

4. mpstat: CPU activity

5. netstat: A variety of network-related information

6. nmon: Performance information (subsystems)

7. pmap: Amount of memory used by the server processors

8. ps, pstree: enlists the currently running processes

9. sar (system activity reporter): CPU utilization, storage device activity, etc.

10. s trace: diagnosing tool

11. tcpdump: network overview

12. top: monitors the active processes including CPU load, memory utilization, etc.

13. uptime: the time duration the server has been running and how many users are currently using it.

14. vmstat: monitor virtual memory like swap memory utilization report

15. dmesg: monitors and displays all the server errors.


### Some other useful commands to get some information regarding the server are:

1. runlevel – Information about the Present Run Level

2. netstat –a – View the Network sessions

3. netstat –rn – To see the gateways configured

4. who/finger – Users logged in detail

5. ps –ef – To have a look on the complete set of running process and the related files

6. sestatus – Verify SELINUX status

7. service iptables status – To check firewall status

8. ifconfig –a – To see the Network cards and configured IP Address


### PING

A ping command can be used in Linux to check if a server is up through the connection between two networks, whether in a LAN or WAN or on the internet, altogether.

Type “ping” in the command window after opening the terminal window
Keep a space and then type the required IP address to ping
Now press Enter and receive the replies if the site is up
Finally, Press Ctrl C to show the results after stopping the command

Carefully using all these commands, we can have a better check if a server is up and running by understanding the present status of Linux servers.



https://apachebooster.com/blog/how-to-check-if-a-server-is-up-and-running-or-down-in-linux/