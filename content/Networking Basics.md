Handshake - A request send to a destination to access it

#### **_IP Adress_**

- IP v4 shows your IP address in decimals
- IP v6 shows your IP address in hexadecimal
- IPv4 starting from 192.168 are all private IP addresses
- Large corporations use IP address starting from 10.0

#### **_MAC adress_**

The first 3 octets of MAC dress tell you about the vendor/company


To know how IP adress and MAC adress ## play a role in networking see [[OSI Canvas.canvas|OSI Canvas]]

#### **_TCP_**

- This is the main information transfer protocol and secure
- Used by almost all connections (browser, internet traffic, HTTP, FTP, telnet)
- Uses 3 way - handshake
- For 3 way - handshake usually the messages request is SYN and response is SYN/ACK and then you send an ACK to establish connections
- So basically TCP will know if data gets stolen is the middle

#### **_UDP_**

- Used for instant/fast connection (DNS etc..)
- Does not use handshake
- UDP doesn’t care about what happens to the data midway



#### **Common Ports**

#### TCP :

| **Protocol** | **Port**  | **Function**                       |
| ------------ | --------- | ---------------------------------- |
| **FTP**      | 21        | Uploads or access file in a server |
| **Telnet**   | 23        | Used to log-in remotely            |
| **SSH**      | 22        | Same as Telnet but crypted         |
| **DNS**      | 53        | Converts domain name to IP adress  |
| **HTTP**     | 80        | Web adress                         |
| **HTTPS**    | 443       | HTTP but crypted                   |
| **SMB**      | 139 / 445 | File sharing                       |

#### UDP :

| **Protocol** | **Port** | **Function**                                               |
| ------------ | -------- | ---------------------------------------------------------- |
| **DNS**      | 53       | Converts domain name to IP adress                          |
| **DHCP**     | 67 / 68  | It provides the IP addresses to devices across the network |

#### **OSI MODEL** 

| **Level**       | **Property**   | **Devices**                                      |
| --------------- | -------------- | ------------------------------------------------ |
| **Level 1**     | Physical       | Wires, cables                                    |
| **Level 2**     | Data Link      | MAC address, Switches, Router, Wifi Access cards |
| **Level 3**     | Network        | IP address, Router, Hosts, IOT devices           |
| **Level 4**     | Transport      | Ports, TCP, UDP                                  |
| **Level 5**     | Session        | Session Management                               |
| **Level 6 & 7** | —————————————— | ——————————————                                   |

#### **GET and POST request** 

| **GET request**                                                             | **POST request**                                                                |
| --------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| This request usually modifies the URL                                       | This request doesn’t change the URL                                             |
| Parameters are visible in the URL, making it less secure for sensitive data | Parameters are not visible in the URL, making it more secure for sensitive data |
| Used to retrieve data from a server                                         | Used to send data to the server to create or update resources                   |
| Usually used in search pages                                                | Usually used to store usernames and passwords                                   |

#### **Other Protocols** :

- **DNS** - It converts Domain Names into IP addresses
      Ex - [www.google.com](http://www.google.com) —> 121.29.8.9

- **ARP** - It is used to get a computers MAC address and consists of senders MAC
	address, ARP is send to every computer on the network

- **Subnet mask** - It is used to divide a IP address into 2 parts :                       
  Its network address and host address
  
   Ex - IP address 121.29.8.9 subnet mask 255.255.255.0 means
     Network address is 121.29.8.0 and host address is .9
 