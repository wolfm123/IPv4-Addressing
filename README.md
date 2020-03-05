# IPv4-Addressing
Python program to help students learn IPv4 addressing and subnetting
Provide  feedback to graziani@cabrillo.edu

Example

*****************************************************************************

Welcome to Rick's Subnet Calculator - Demonstration Mode

Part 1: Major Network
1. You are prompted for an IPv4 address and subnet mask.
2. Displays the IPv4 address, subnet mask, network address, first host,
   last host and broadcast addresses in binary and dotted decimal.
3. Displays additional information such as the number of network bits,
   host bits and the number of hosts addresses for this network.
4. Generates an example of a host address on this network (optional).

Part 2: Subnetting (optional)
1. You are prompted for a new subnet mask to subnet the network.
2. Displays the IPv4 address, subnet mask, network address, first host,
   last host and broadcast addresses in binary and dotted decimal.
3. Displays additional information such as the number of network bits,
   host bits, the number of subnets, and the number of hosts per subnet.
4. Generates an example of a host address on this network (optional).

Part 3: Subnet List (optional)
1. Generates a list of all subnets.

Note: Use control-C to exit at any time.


Note: The program ipv4-addressing-test.pl can be used to test your knowledge

Part 1: Major Network
-----------------------

Enter an IPv4 address: 192.168.1.10
Enter the current subnet mask: 255.255.255.0

        IPv4 address in binary:          11000000 10101000 00000001 00001010
        Subnet mask in binary:           11111111 11111111 11111111 00000000

This is a HOST address. There are not all 0s nor all 1s in the host portion.
Press enter to continue... 

IPv4 address:    11000000 10101000 00000001 00001010
Subnet mask:     11111111 11111111 11111111 00000000
                 -----------------------------------    Copy the network bits:
Network:         11000000 10101000 00000001 00000000    Network + Host (all 0s)
First host:      11000000 10101000 00000001 00000001    Network + Host (all 0s + 1)
Last host:       11000000 10101000 00000001 11111110    Network + Host (all 1s + 0)
Broadcast:       11000000 10101000 00000001 11111111    Network + Host (all 1s)

Number of network bits:  24 bits or /24
Number of host bits:  8 bits
Number of hosts :  2^8 - 2 = 254 hosts

Addresses in dotted decimal notation:
Network address is: 192.168.1.0
First host is: 192.168.1.1
Last host is: 192.168.1.254
Broadcast address is: 192.168.1.255


Generate a random IPv4 host address from subnet? (y/n)y
Random IPv4 host address for this network is: 192.168.1.241
Generate a random IPv4 host address from subnet? (y/n)n

Part 2: Subnetting (optional)
--------------------------------

Do you want to subnet this network? (y/n)y

The current network address and subnet mask are:
        Network address:         192.168.1.0     11000000 10101000 00000001 00000000
        Subnet mask:             255.255.255.0   11111111 11111111 11111111 00000000

The new subnet mask must have additional 1 bits by borrowing bits from the host address.

Enter a different subnet mask to subnet the previous network: 255.255.255.240
        Previous subnet mask:    255.255.255.0   11111111 11111111 11111111 00000000
        Your new subnet mask:    255.255.255.240         11111111 11111111 11111111 11110000

This is a valid subnet mask because it has 4 more bit(s) than the current network mask.

        IPv4 address in binary:          11000000 10101000 00000001 00001010
        Subnet mask in binary:           11111111 11111111 11111111 11110000

This is a HOST address. There are not all 0s nor all 1s in the host portion.
Press enter to continue...

IPv4 address:    11000000 10101000 00000001 00001010
Subnet mask:     11111111 11111111 11111111 11110000
                 -----------------------------------    Copy the network bits:
Network:         11000000 10101000 00000001 00000000    Network + Host (all 0s)
First host:      11000000 10101000 00000001 00000001    Network + Host (all 0s + 1)
Last host:       11000000 10101000 00000001 00001110    Network + Host (all 1s + 0)
Broadcast:       11000000 10101000 00000001 00001111    Network + Host (all 1s)

Number of network bits:  28 bits or /28
Number of subnet bits:  4 bits
Number of subnets:  2^4 = 16 subnets
Number of host bits:  4 bits
Number of hosts per subnet:  2^4 - 2 = 14 hosts per subnet

Addresses in dotted decimal notation:
Network address is: 192.168.1.0
First host is: 192.168.1.1
Last host is: 192.168.1.14
Broadcast address is: 192.168.1.15


Generate a random IPv4 host address from subnet? (y/n)y
Random IPv4 host address for this network is: 192.168.1.9
Generate a random IPv4 host address from subnet? (y/n)n

Part 3: Subnet List
-----------------------

For a listing of ALL SUBNETS, press any key to continue...

Subnets in dotted decimal and binary
Subnets: Common network bits (the same) - Subnet (increment by 1) - Host (all 0s)
-----------------------------------------------------------------------------------
192.168.1.0      110000001010100000000001 0000 0000
192.168.1.16     110000001010100000000001 0001 0000
192.168.1.32     110000001010100000000001 0010 0000
192.168.1.48     110000001010100000000001 0011 0000
192.168.1.64     110000001010100000000001 0100 0000
192.168.1.80     110000001010100000000001 0101 0000
192.168.1.96     110000001010100000000001 0110 0000
192.168.1.112    110000001010100000000001 0111 0000
192.168.1.128    110000001010100000000001 1000 0000
192.168.1.144    110000001010100000000001 1001 0000
192.168.1.160    110000001010100000000001 1010 0000
192.168.1.176    110000001010100000000001 1011 0000
192.168.1.192    110000001010100000000001 1100 0000
192.168.1.208    110000001010100000000001 1101 0000
192.168.1.224    110000001010100000000001 1110 0000
192.168.1.240    110000001010100000000001 1111 0000

IPv6 is so much easier!

