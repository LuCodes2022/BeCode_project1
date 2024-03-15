# BeCode_project1
first BeCode solo networking project
- This project is created to learn how to create a simple network with access to the Internet.
- I have simulated said access by creating a second network with a router a switch and a server.
- We also needed a network with three PCSs, a switch, and a router
- Therefore my project has three networks technically, one for the PCs and the first router, one for the two routers, and one for the router switch and server.

How is network 10.1.1.0 connected?

- the networks all use copper straight-through
- this one has a total of four wires
- the first is connected to PC-Robert-s fastethernet 0/0(with IP 10.1.1.2) to the switch's fastethernet 0/1.
- the second is connected to PC-Camille FastEthernet 0/0 (IP 10.1.1.3) to the switch's FastEthernet 0/2.
- The third is connected to PC-Renaud FastEthernet 0/0 (IP 10.1.1.4)to the switch's FastEthernet 0/3.
- Finally the last, but not least important, is connected to the switch's GigaEthernet 0/1 to the router-0's GigaEthernet 0/0(IP 10.1.1.1).

How is network 192.168.0.0 connected?

- We have one copper straight-through cable in this network.
- router-0's GigaEthernet 0/1 (IP 192.168.0.1)is connected to router-ISP's GigaEthernet 0/1 (IP 192.168.0.2).
  
How is network 8.8.8.0 connected? 

- This network has two copper straight-through wires.
- The first is connected to router-ISP's GigaEthernet 0/0 (IP 8.8.8.1) to the switch's GigaEthernet 0/1.
- Finally, the switch's FastEthernet 0/1 is connected to the wwww.catsruletheworld.com server's FastEthernet 0/0 (IP 8.8.8.8).

Things I am still working on

- finishing this file to be as detailed about what I did for this project as possible.

Things I am considering

- finding simpler ways to emulate the internet and have a simpler network.
