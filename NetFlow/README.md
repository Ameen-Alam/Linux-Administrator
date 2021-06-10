# NetFlow

NetFlow is a protocol developed by Cisco Systems to record all IP traffic flows traversing a router or switch that is NetFlow enabled. It generates statistics inside these devices at the interface level and sends this information in UDP-based flow records to an external element called a flow collector—a program running on a server where the traffic statistics can be stored for load balancing analysis.

A NetFlow-enabled device identifies a flow as a unidirectional stream of packets defined by:

Input interface port
IP source addresses
IP destination addresses
Source port number
Destination port number
Layer 3 protocol field
Type of Service
NetFlow creates and tracks flow information or metadata for these unidirectional IP traffic flows in the in-memory cache on a NetFlow-supporting device. This metadata is used by multiple network administrators using software analysis tools to help them analyze network throughput, packet loss, traffic congestion, identify DDoS attacks, and other network monitoring use cases.


[get-start-cfg-nflow](https://www.cisco.com/c/en/us/td/docs/ios-xml/ios/netflow/configuration/15-mt/nf-15-mt-book/get-start-cfg-nflow.html)
