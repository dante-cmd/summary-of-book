# IP Addresses

The Internet Protocol is a set of rules for communication over the internet, such as sending mail, streaming video, or connecting to a website

An IP address, or Internet Protocol address, is a series of numbers that identifies any device on a network. Computers use IP addresses to communicate with each other both over the internet as well as on other networks

On the Internet, each `host` has a unique IP address, represented by a 32-bit number (this is a dot dotation gives the decimal value (0 to 255) of each byte).

An IP address serves two principal functions: it *identifies the host*, or more specifically its network interface, and it provides the *location of the host in the network*, and thus the capability of establishing a path to that host. 

Its role has been characterized as follows: "A name indicates what we seek. An address indicates where it is. A route indicates how to get there." The header of each IP packet contains the IP address of the sending host and that of the destination host.

Two versions of the Internet Protocol are in common use on the Internet today. `IPv4` and `IPv6`

* `192.168.0.111`, 
* In bits [`011000000`, `010101000`, `00000000`, `01101111`]


The parts of your IP address:

An IP address has two parts: the *network ID*, comprising the first three numbers of the address, and a *host ID*, the fourth number in the address. So on your home network — 192.168.1.1, for example – 192.168.1 is the network ID, and the final number is the host ID.

The Network ID indicates which network the device is on. The Host ID refers to the specific device on that network.

The dot notation is easy on machines but hard on users. Therefore, each host also has a unique *domain-based name* composed of words e.g. `https://cs50.harvard.edu/x/2022`. This let to the entire Internet host namespace is recursively divided into disjoint domains, called the generic *top-level domain* (TLD).
* `org` (nonprofit organizations)
* `gov` (government offices)
* `mil` (military installations)
* `com` (commercial outfits)
* `edu` (education institutions)
* `net` (network service providers)
* `pe` (peru country)

Within a local domain (e.g., cs.kent.edu), you can refer to computers by their host name alone (e.g., loki, dragon, tiger), but the full address must be used for hosts outside.

A full domain name is formed by connecting all names leading from the host name to the root of the DNS tree.

$$\text{cs50} \rightarrow \text{harvard} \rightarrow \text{edu}$$

The `ICANN` accredits domain name registrars, which register domain names for clients so they stay *unique* (we pay by that)

The `domain name` is first translated (matched) to a numerical IP address before being used. An example is in [SuperSimpleDev](https://www.youtube.com/watch?v=p1QU3kLFPdg).

Data on the Internet are sent and received in *packets*. A packet envelops transmitted data with address information so the data can be routed through intermediate computers on the network. Because there are multiple routes from the source to the destination host, the Internet is very reliable and can operate even if parts of the network are down.

## Subnetwork

A subnetwork or `subnet` is a logical subdivision of an IP network.  The practice of dividing a network into two or more networks is called *subnetting*.

Computers that belong to the same subnet are addressed with an identical most-significant bit-group in their IP addresses

The IP address is divided into two fields: *routing prefix* and *host identifier* (this is an identifier for a specific host)

The *routing prefix* may be expressed in `Classless Inter-Domain Routing (CIDR)` notation written as the first address of a network, followed by a slash character `(/)`, and ending with the bit-length of the prefix. 

For example, 198.51.100.0/24 is the prefix of the Internet Protocol version 4 network starting at the given address, having 24 bits allocated for the network prefix, and the remaining 8 bits reserved for host addressing. Addresses in the range 198.51.100.0 to 198.51.100.255 belong to this network

> Routing
> 
> Routing is the process of selecting a path for traffic in a network or between or across multiple networks. 
