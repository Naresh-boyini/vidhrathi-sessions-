# Network Ports and Basic Network Tools

## Table of Contents
- [Introduction to Network Ports](#introduction-to-network-ports)
- [States of Network Ports](#states-of-network-ports)
- [Basic Networking Tools](#basic-networking-tools)
- [Examples and Usage](#examples-and-usage)

---

## Introduction to Network Ports

Network ports are virtual points where network connections start and end. They play a crucial role in distinguishing different types of traffic on the same physical network connection. Each port is identified by a number, ranging from 0 to 65535, and is used by various network protocols to manage data transmission effectively.

Common use cases for network ports include web traffic (HTTP/HTTPS), email communication (SMTP), and file transfer (FTP).

---

## States of Network Ports

### Listening Ports
Listening ports are ports that are waiting for incoming connections. They are typically associated with server applications.

- **Example:** A web server listening on port 80 or 443 for HTTP/HTTPS traffic.

### Closed Ports
Closed ports are ports that are not being used by any application and are not listening for connections.

- **Example:** A port that is not assigned to any service or application will be closed.

### Open Ports
Open ports are ports that are actively being used by applications for communication.

- **Example:** A port used by a running application, like a web server or an FTP server.

---

## Basic Networking Tools

### Netstat
`netstat` (network statistics) is a command-line tool that provides information about network connections, routing tables, interface statistics, masquerade connections, and multicast memberships.

- **Common Commands:**
  - `netstat -a`: Displays all active connections and listening ports.
  - `netstat -t`: Shows TCP connections.
  - `netstat -u`: Shows UDP connections.

### Traceroute
`traceroute` is a network diagnostic tool used to track the path packets take from the source to the destination.

- **Common Command:**
  - `traceroute <destination>`: Traces the route to the specified destination.

### Tracert
`tracert` is the Windows equivalent of `traceroute`.

- **Common Command:**
  - `tracert <destination>`: Traces the route to the specified destination.

### Nslookup
`nslookup` is a network administration command-line tool used for querying the Domain Name System (DNS) to obtain domain name or IP address mapping.

- **Common Commands:**
  - `nslookup <domain>`: Retrieves the IP address of the specified domain.
  - `nslookup <IP>`: Retrieves the domain name associated with the specified IP address.

### Ifconfig
`ifconfig` (interface configuration) is used to configure network interfaces in Unix and Linux systems.

- **Common Commands:**
  - `ifconfig`: Displays all active interfaces.
  - `ifconfig <interface> up/down`: Activates or deactivates a network interface.

### Route
`route` is used to view and manipulate the IP routing table.

- **Common Commands:**
  - `route`: Displays the current routing table.
  - `route add <destination> <gateway>`: Adds a route to the routing table.
  - `route del <destination>`: Removes a route from the routing table.

---

## Examples and Usage

### Netstat Examples
```sh
# Display all active connections and listening ports
netstat -a

```
# Display only TCP connections
```
netstat -t
```
# Display only UDP connections
```
netstat -u
```

# Trace the route to www.example.com
```
traceroute www.example.com
```

# Get the IP address of example.com
```
nslookup example.com
```
# Get the domain name for IP address 93.184.216.34
```
nslookup 8.8.8.8
```

# Display all active interfaces
```
ifconfig
```
# Activate the eth0 interface
```
ifconfig eth0 up
```
# Deactivate the eth0 interface
```
ifconfig eth0 down
```

# Display the current routing table
```
route
```
# Add a route to 192.168.1.0/24 via gateway 192.168.1.1
```
route add -net 192.168.1.0 netmask 255.255.255.0 gw 192.168.1.1
```

# Remove the route to 192.168.1.0/24
```
route del -net 192.168.1.0 netmask 255.255.255.0
```
