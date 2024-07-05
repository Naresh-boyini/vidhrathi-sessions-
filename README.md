\# Network Ports and Basic Network Tools

\## Table of Contents

\- \[Introduction to Network Ports\](#introduction-to-network-ports)

\- \[States of Network Ports\](#states-of-network-ports)

\- \[Basic Networking Tools\](#basic-networking-tools)

\- \[Examples and Usage\](#examples-and-usage)

\---

\## Introduction to Network Ports

Network ports are virtual points where network connections start and end. They play a crucial role in distinguishing different types of traffic on the same physical network connection. Each port is identified by a number, ranging from 0 to 65535, and is used by various network protocols to manage data transmission effectively.

Common use cases for network ports include web traffic (HTTP/HTTPS), email communication (SMTP), and file transfer (FTP).

\---

\## States of Network Ports

\### Listening Ports

Listening ports are ports that are waiting for incoming connections. They are typically associated with server applications.

\- \*\*Example:\*\* A web server listening on port 80 or 443 for HTTP/HTTPS traffic.

\### Closed Ports

Closed ports are ports that are not being used by any application and are not listening for connections.

\- \*\*Example:\*\* A port that is not assigned to any service or application will be closed.

\### Open Ports

Open ports are ports that are actively being used by applications for communication.

\- \*\*Example:\*\* A port used by a running application, like a web server or an FTP server.

\---

\## Basic Networking Tools

\### Hostname

Hostname command is used to view the hostname of the machine and to set the hostname.

\- \*\*Common Commands:\*\*

\- \`hostname\`: View the hostname of the machine.

\- \`sudo hostname temp.com\`: Set a new hostname for the machine.

\### Host

Host command is for the reverse lookup of IP or a DNS name.

\- \*\*Common Commands:\*\*

\- \`host 8.8.8.8\`: Find the DNS attached with an IP.

\- \`host devopscube.com\`: Find the IP address associated with the domain name.

\### Ping

The ping networking utility is used to check if the remote server is reachable or not.

\- \*\*Common Commands:\*\*

\- \`ping devopscube.com\`: Ping a domain.

\- \`ping 8.8.8.8\`: Ping an IP address.

\- \`ping -c 1 devopscube.com\`: Limit the ping output.

\### Curl

Curl utility is primarily used to transfer data from or to a server.

\- \*\*Common Commands:\*\*

\- \`curl -v telnet://192.168.33.10:22\`: Check connectivity on port 22 using telnet.

\- \`curl ftp://ftptest.net\`: Check FTP connectivity.

\- \`curl http://devopscube.com -I\`: Troubleshoot web server connectivity.

\### Wget

The wget command is primarily used to fetch web pages.

\- \*\*Common Commands:\*\*

\- \`wget -e use\_proxy=yes http\_proxy= http://externalsite.com\`: Troubleshoot proxy server connections.

\- \`wget www.google.com\`: Check if a website is up by fetching the files.

\### Ip (Ifconfig)

ip command is used to display and manipulate routes and network interfaces. ip command is the newer version of ifconfig.

\- \*\*Common Commands:\*\*

\- \`ip addr\`: Display network devices and configuration.

\- \`ip a | grep eth0 | grep "inet" | awk -F" " '{print $2}'\`: Get the IP address of eth0 network interface.

\- \`ip a show eth0\`: Get details of a specific interface.

\- \`ip route\`: List the routing tables.

\### Arp

ARP (Address Resolution Protocol) shows the cache table of local networks’ IP addresses and MAC addresses that the system interacted with.

\- \*\*Common Commands:\*\*

\- \`arp\`: Display the ARP cache table.

\### Ss (Netstat)

The ss command is a replacement for netstat. You can get more information than netstat command.

\- \*\*Common Commands:\*\*

\- \`ss\`: List all the TCP, UDP, and Unix socket connections.

\- \`ss -ta\`: Filter out TCP connections.

\- \`ss -ua\`: Filter out UDP connections.

\- \`ss -xa\`: Filter out Unix socket details.

\- \`ss -lt\`: List all listening ports.

\- \`ss -t -r state established\`: List all established ports.

\- \`ss -t -r state listening\`: List all sockets in listening state.

\### Traceroute

traceroute is a network troubleshooting utility. Using traceroute you can find the number of hops required for a particular packet to reach the destination.

\- \*\*Common Commands:\*\*

\- \`traceroute google.com\`: Trace the route to google.com.

\### Mtr

The mtr utility is a network diagnostic tool to troubleshoot the network bottlenecks. It combines the functionality of both ping and traceroute.

\- \*\*Common Commands:\*\*

\- \`mtr google.com\`: Shows the traceroute output in real-time.

\- \`mtr -n --report google.com\`: Generate a report.

\### Dig

If you have any task related to DNS lookup, you can use “dig” command to query the DNS name servers.

\- \*\*Common Commands:\*\*

\- \`dig twiter.com ANY\`: Get all DNS records and TTL information.

\- \`dig google.com ANY +short\`: Get the output without verbose.

\- \`dig www.google.com A +short\`: Get the A record for the particular domain name.

\- \`dig google.com CNAME +short\`: Get the CNAME record.

\- \`dig google.com MX +short\`: Get the MX record.

\- \`dig google.com TXT +short\`: Get the TXT record.

\- \`dig google.com NS +short\`: Get the NS record.

\- \`dig -x 8.8.8.8\`: Perform a reverse DNS lookup.

\### Nslookup

Nslookup (Name Server Lookup) utility is used to check the DNS entries.

\- \*\*Common Commands:\*\*

\- \`nslookup google.com\`: Check the DNS records of a domain.

\- \`nslookup 8.8.8.8\`: Do a reverse lookup with the IP address.

\- \`nslookup -type=any google.com\`: Get all the DNS records of a domain name.

\### Nc (Netcat)

The nc (netcat) command is known as the swiss army of networking commands.

\- \*\*Common Commands:\*\*

\- \`nc -v -n 192.168.33.10 22\`: Check the connectivity of a service running on a specific port.

\### Telnet

The telnet command is used to troubleshoot the TCP connections on a port.

\- \*\*Common Commands:\*\*

\- \`telnet 10.4.5.5 22\`: Check port connectivity using telnet.

\### Route

The “route” command is used to get the details of the route table for your system and to manipulate it.

\- \*\*Common Commands:\*\*

\- \`route\`: List all routes.

\- \`route -n\`: Get the full output in numerical form.

\### Tcpdump

The tcpdump command is primarily used for troubleshooting network traffic.

\- \*\*Common Commands:\*\*

\- \`sudo tcpdump --list-interfaces\`List all network interfaces.

\`sudo tcpdump --list-interfaces\`

\- \`sudo tcpdump -i eth0\`: Capture packets on a specific interface.

\- \`sudo tcpdump -i eth0 -c 10\`: Limit the packet capturing.

\- \`sudo tcpdump -i any\`: Capture packets on all the interfaces.

\### Lsof

lsof is a command that would used in day to day linux troubleshooting.

\- \*\*Common Commands:\*\*

\- \`lsof\`: List all open files.

\- \`lsof -i :8080\`: Find the process ID associated with a port.

\---

\## Examples and Usage

\### Netstat Examples

\`\`\`sh

\# Display all active connections and listening ports

netstat -a

\# Display only TCP connections

netstat -t

\# Display only UDP connections

netstat -u

\# Trace the route to www.example.com

\`\`\`

traceroute www.example.com

\`\`\`

\# Get the IP address of example.com

\`\`\`

nslookup example.com

\`\`\`

\# Get the domain name for IP address 93.184.216.34

\`\`\`

nslookup 8.8.8.8

\`\`\`

\# Display all active interfaces

\`\`\`

ifconfig

\`\`\`

\# Activate the eth0 interface

\`\`\`

ifconfig eth0 up

\`\`\`

\# Deactivate the eth0 interface

\`\`\`

ifconfig eth0 down

\`\`\`

\# Display the current routing table

\`\`\`

route

\`\`\`

\# Add a route to 192.168.1.0/24 via gateway 192.168.1.1

\`\`\`

route add -net 192.168.1.0 netmask 255.255.255.0 gw 192.168.1.1

\`\`\`

\# Remove the route to 192.168.1.0/24

\`\`\`

route del -net 192.168.1.0 netmask 255.255.255.0

\`\`\`
