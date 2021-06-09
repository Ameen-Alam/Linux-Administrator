# Traceroute


Traceroute is a network diagnostic tool used to track in real-time the pathway taken by a packet on an IP network from source to destination, reporting the IP addresses of all the routers it pinged in between. Traceroute also records the time taken for each hop the packet makes during its route to the destination.

Traceroute most commonly uses Internet Control Message Protocol (ICMP) echo packets with variable time to live (TTL) values. The response time of each hop is calculated. To guarantee accuracy, each hop is queried multiple times (usually three times) to better measure the response of that particular hop. Traceroute uses ICMP messages and TTL fields in the IP address header to function. Traceroute tools are typically included as a utility by operating systems such as Windows and Unix. Traceroute utilities based on TCP are also available.


#### What is Traceroute Used For?

Traceroute is a useful tool for determining the response delays and routing loops present in a network pathway across packet switched nodes. It also helps to locate any points of failure encountered while en route to a certain destination.

However, in the Internet, Traceroute messages are often blocked by routers in various Autonomous Systems (AS), making Traceroute highly inaccurate in many cases.


##### Linux or MAC
$ traceroute domain.com
$ traceroute IP

##### Windows 

$ tracert domain.com
$ tracert IP