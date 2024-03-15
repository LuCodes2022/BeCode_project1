# BeCode_project1
first BeCode solo networking project
- This project is created to learn how to create a simple network with access to the Internet.
- I have simulated said access by creating a second network with a router a switch and a server.
- We also needed a network with three PCSs, a switch, and a router
- Therefore my project has three networks technically, one for the PCs and the first router, one for the two routers, and one for the router switch and server.

Before everything here are a few things we need to know for this exercise:

- How do we edit IP addresses and default gateways of ports on our hosts and routers?
  - to assign an IP address to one of the hosts click on them.
  - Then in the up written in blue choose config.
  - Then on the left click on the port that you want to assign an IP address to.
  - enter the IP address.
  - Do it until all the used ports have an assigned IP address to connect to your network.
  
- How do we set the default gateway?
  - After assigning a value to the port connected to the cable from the router to the switch, copy it.
  - Then close the tab and click on your hosts.
  - chose config in the menu on the top center.
  - in there you will see a space that says default gateway.
  - In there paste the IP from the router you copied earlier
  - do it for all the hosts in that network.
  - Voilà!
    
- How do we configure our routers?
  - We click on the routers, then select CLI from the menu up in the center.
  - Press enter
  - Type config t then press enter
  - Then enter int (name of port)
  - To assign a value to a port we enter ip add (IP) (subnet mask) 
  - Then type no shut
  - Now our routers should be mostly set up, we still need to route them to one another but we will see that later.

How is network 192.168.1.0 connected?

- the networks all use copper straight-through
- this one has a total of four wires
- the first is connected to PC-Robert-s fastethernet 0/0(with IP 192.168.1.10) to the switch's fastethernet 0/1.
- the second is connected to PC-Camille FastEthernet 0/0 (IP 192.168.1.11) to the switch's FastEthernet 0/2.
- The third is connected to PC-Renaud FastEthernet 0/0 (IP 192.168.1.12)to the switch's FastEthernet 0/3.
- The default gateway is the same for all the hosts, it is our router-0, so 192.168.1.1.
- Finally the last, but not least important, is connected to the switch's GigaEthernet 0/1 to the router-0's GigaEthernet 0/0(IP 192.168.1.1).

How is network 192.168.0.0 connected?

- We have one copper straight-through cable in this network.
- router-0's GigaEthernet 0/1 (IP 192.168.0.1)is connected to router-ISP's GigaEthernet 0/1 (IP 192.168.0.2).
  
How is network 8.8.8.0 connected? 

- This network has two copper straight-through wires.
- The first is connected to router-ISP's GigaEthernet 0/0 (IP 8.8.8.1) to the switch's GigaEthernet 0/1.
- The default gateway is 8.8.8.1 since it is our router-ISP's IP for this network.
- Finally, the switch's FastEthernet 0/1 is connected to the wwww.catsruletheworld.com server's FastEthernet 0/0 (IP 8.8.8.8).

How do the networks know how to communicate with each other?

- one of the earlier networks connects the two routers making it possible for them to share information.
- Therefore we need to tell the hosts of the other networks the routers are also a part of how to reach one another.
- For that, we have to tell each host the IP route to take.
- So we tell them the other network's IP, the subnet mask, and the IP of the port to use on router-0 to get there.
  - for network 8.8.8.0 we enter 192.168.1.0 255.255.255.0 192.168.0.1
  - for network 192.168.1.0 we enter 8.8.8.0 255.255.255.0 192.168.0.2

Things I am still working on

- explaining how to configure everything in cisco packet tracer

Things I am considering

- finding simpler ways to emulate the internet and have a simpler network.
