# Design and Implementation of an Enterprise Bank network

## Networking simulation software used:
Cisco Packet Tracer 8.2.2

## Scenario:
Radeon Company Ltd. is a US-owned company that deals with Banking and Insurance. The company intends to expand its services across the African continent having the first branch to be located in Nairobi, Kenya. The company has secured a four-story building to operate within the Kenyan capital city. Therefore, the company would like to allow sourcing knowledge from a group of final-year students from the local university to design and implement their company network. Assume you are among the students to take over this role, carefully read down the requirements then model the design and implement the network based on the company's needs. Each floor has departments as provided in the table below:

<img width="470" alt="image" src="https://github.com/user-attachments/assets/ef6f6915-0b19-4e4b-bc4b-f4feebb34796" />

## Requirements:

•	Use a software modeling tool to visualize the network topology (Use Hierarchical Network Design. Software Modelling Tools: MS Visio, Visual Paradigm, or Draw.io for modeling network design.

•	Use any of the following network simulation software to implement the above topology. Simulation software: Cisco Packet tracer or GNS3 for design and implementation.
  
•	Use OSPF as the routing protocol to advertise routes.

•	Each department is required to have a wireless network for the users.

•	Each department except the server room will be anticipated to have around 60 users both wired and wireless users.

•	Host devices in the network are required to obtain IPv4 addresses automatically.

•	Devices in all the departments are required to communicate with each other.

•	Create HTTP, and E-mail servers.

•	All devices in the network are expected to obtain an IP address dynamically from the dedicated DHCP servers located at the server room.

•	Configure SSH in all the routers for remote login.

•	Configure the basic configuration of the devices: Hostnames, Line Console and Enable passwords, Banner messages Disable domain IP lookup, encrypt all configured passwords.

•	Each department should be in a different VLAN and subnetwork; VLANs you will use in your case, e.g. 10, 20, 30, etc..

•	Planning of IP Addresses: You have been given 192.168.10.0 as the base address for this network. Do subnetting based on the number of hosts in every department as provided above. Identify subnet mask, useable IP address range, and broadcast address for each subnet.

•	End Device Configurations: Configure all the end devices in the network with the appropriate IP address based on the calculations above.

•	Configure port-security: Use sticky command to obtain MAC Address and Violation mode of the shutdown.

•	Test and Verifying Network Communication.

## Technologies Implemented

1.	Creating a network topology using Cisco Packet Tracer.
2.	Hierarchical Network Design.
3.	Connecting Networking devices with Correct cabling.
4.	Configuring Basic device settings.
5.	Creating VLANs and assigning ports VLAN numbers.
6.	Subnetting and IP Addressing.
7.	Configuring Inter-VLAN Routing on the Multilayer switches (Switch Virtual Interface).
8.	Configuring Dedicated DHCP Server device to provide dynamic IP allocation.
9.	Configuring SSH for secure Remote access.
10.	Configuring OSPF as the routing protocol.
11.	Configuring switchport security or Port-Security on the switches.
12.	Configuring WLAN or wireless network (Cisco Access Point).
13.	Host Device Configurations.
14.	Test and Verifying Network Communication.

## Network Model Design:

<img width="1339" alt="image" src="https://github.com/user-attachments/assets/b2a0a1e8-80b6-48cc-a081-41bf46178414" />

## Subnetting the network:

Base Network: 192.168.10.0

No. of subnets required: 3

No. of subnets = 2^n (n = number of bits borrowed)

2^n = 3 (n = number of bits borrowed)

2^2 = 4 

Therefore: n = 2

Class C address:

255.255.255.0 = 11111111.11111111.11111111.00000000

Borrowing 4 bits from host portion:

11111111.11111111.11111111.11000000

New subnet mask: 255.255.255.192 or /26

## IP Addressing

<img width="697" alt="image" src="https://github.com/user-attachments/assets/34c84a17-29dd-4018-9af9-bc4a4e1ce7e0" />

<img width="697" alt="image" src="https://github.com/user-attachments/assets/95f49cb1-b27b-4412-b5ea-f11716908b9d" />

## Between routers and layer 3 switches: 

Base Network Address: 10.10.10.0

<img width="697" alt="image" src="https://github.com/user-attachments/assets/d8cca043-f08c-49b7-8303-3fb9e76b9022" />

## Configuration:

Turning on all necessary router ports:

Floor1-Router

<img width="327" alt="image" src="https://github.com/user-attachments/assets/aacf7231-aa5d-4d98-a6fb-78d5dbbf68ae" />

Floor2-Router

<img width="360" alt="image" src="https://github.com/user-attachments/assets/496f5822-9f21-4262-a126-fd1fc3d1196c" />

Floor3-Router

<img width="459" alt="image" src="https://github.com/user-attachments/assets/cd419e23-db35-4367-a41d-28f40e9e58d6" />

Floor4-Router

<img width="459" alt="image" src="https://github.com/user-attachments/assets/bb1fbdc4-fcfc-47ca-bc32-4d1f149b6d7f" />

Configuring access layer switches:

Floor1-Management-SW

<img width="322" alt="image" src="https://github.com/user-attachments/assets/fa096733-7ce4-44a2-b0ba-65c2dfd9ae6c" />

Floor1-Research-SW

<img width="341" alt="image" src="https://github.com/user-attachments/assets/7617d4b2-df19-4ee2-8c46-00ad1b78fa54" />

Floor1-HR-SW

<img width="323" alt="image" src="https://github.com/user-attachments/assets/fbdde739-d9ed-4c64-b2d3-dd0bed52d7da" />

Floor2-Marketing-SW

<img width="352" alt="image" src="https://github.com/user-attachments/assets/1d07b6db-b57f-46b5-ae35-607aac1ee138" />

Floor2-Accounting-SW

<img width="360" alt="image" src="https://github.com/user-attachments/assets/73d1d525-a505-4fc6-971d-86ce13ea4aea" />

Floor2-Finance-SW

<img width="334" alt="image" src="https://github.com/user-attachments/assets/5f6d4bf9-d57a-4864-86bf-f74d70083536" />

Floor3-Logistics-SW

<img width="348" alt="image" src="https://github.com/user-attachments/assets/6acc0639-6cda-4ae5-b2fb-551b843e1a65" />

Floor3-Customer-SW

<img width="368" alt="image" src="https://github.com/user-attachments/assets/25b17155-f899-4e36-b34b-8522d84129a6" />

Floor3-Guest-SW

<img width="336" alt="image" src="https://github.com/user-attachments/assets/57b43df9-014e-4179-9029-a243c57ac4f4" />

Floor4-Admin-SW

<img width="323" alt="image" src="https://github.com/user-attachments/assets/b7368206-4e67-420e-9220-8d3c2d3bd703" />

Floor4-ICT-SW

<img width="323" alt="image" src="https://github.com/user-attachments/assets/ff3d758d-a758-4ecb-8197-a1d552e861e6" />

Floor4-Server-SW

<img width="323" alt="image" src="https://github.com/user-attachments/assets/53668018-f835-46cc-9a04-2b5775c6b6a5" />

Configuring Distribution layer switches:

Floor1-L3SW

<img width="384" alt="image" src="https://github.com/user-attachments/assets/ed9a7304-3bfe-4e67-8f16-22f3b425e9e9" />

Floor2-L3SW

<img width="383" alt="image" src="https://github.com/user-attachments/assets/134a6b6f-4241-4ebf-92aa-c57ece1e4724" />

Floor3-L3SW

<img width="390" alt="image" src="https://github.com/user-attachments/assets/b5140307-f65d-4349-99ce-813f80d49dca" />

Floor4-L3SW

<img width="382" alt="image" src="https://github.com/user-attachments/assets/4690693f-9d34-455d-8075-abf8707633bc" />

Configuring Core Layer Routers:

Floor1 router

<img width="389" alt="image" src="https://github.com/user-attachments/assets/7f6c43c2-6c93-45d0-8c49-829d8476d4a3" />

Floor2 router

<img width="381" alt="image" src="https://github.com/user-attachments/assets/7632b56c-12e0-424f-95ff-712940b367f0" />

Floor3 router

<img width="383" alt="image" src="https://github.com/user-attachments/assets/ec6e5650-1318-4dd2-867d-7bce9fce04d8" />

Floor4 router

<img width="383" alt="image" src="https://github.com/user-attachments/assets/b47aebeb-2a71-44ed-92ff-4343f543e5e8" />

Configuring trunk and access ports, VLANS and port security:

Floor1-Management-SW

<img width="470" alt="image" src="https://github.com/user-attachments/assets/7f07ce18-e5fe-4d85-b5c2-d4117ec29e73" />


<img width="273" alt="image" src="https://github.com/user-attachments/assets/1d8ccda3-c41c-4e41-8897-8a1c73421f49" />

Floor1-Research-SW

<img width="416" alt="image" src="https://github.com/user-attachments/assets/21e582fd-a6b8-438d-8bd6-fb121c416fe0" />

Floor1-HR-SW

<img width="373" alt="image" src="https://github.com/user-attachments/assets/5abfa06c-9aff-41bc-b3c4-32592bacc2b2" />

Floor2-Marketing-SW

<img width="407" alt="image" src="https://github.com/user-attachments/assets/2dc97fba-95ce-40ba-94e0-c3054ce0da61" />

Floor2-Accounting-SW

<img width="462" alt="image" src="https://github.com/user-attachments/assets/1b668f01-6977-417c-bd41-c902c9bd91f4" />

Floor2-Finance-SW

<img width="460" alt="image" src="https://github.com/user-attachments/assets/e986a67d-1803-4833-81c8-37dec3a6ccc8" />

Floor3-Logistics-SW

<img width="458" alt="image" src="https://github.com/user-attachments/assets/64add720-70c6-43b9-8303-bcb911db4499" />

Floor3-Customer-SW

<img width="457" alt="image" src="https://github.com/user-attachments/assets/15f5a013-1509-46b6-8449-da38f1deaaee" />

Floor 3-Guest-SW

<img width="460" alt="image" src="https://github.com/user-attachments/assets/35dd3257-2f56-4fd6-9a33-f225d02a39e3" />

Floor4-Admin-SW

<img width="463" alt="image" src="https://github.com/user-attachments/assets/2343f489-2bb9-4d6b-9484-82156312b405" />

Floor4-ICT-SW

<img width="464" alt="image" src="https://github.com/user-attachments/assets/9109d591-cbdc-497d-9247-0b32150f579c" />

Floor4-Servers-SW

<img width="464" alt="image" src="https://github.com/user-attachments/assets/6769bd95-3a5c-43ef-b1ad-4c8e3a6d465a" />

Configuring trunk and IP address on layer 3 switches:

Floor1-L3SW

<img width="322" alt="image" src="https://github.com/user-attachments/assets/af6af032-8ea3-43af-9e6f-320343ce9492" />

Floor2-L3SW

<img width="439" alt="image" src="https://github.com/user-attachments/assets/67082cf5-d81c-4b97-8d6d-7a7bef04290e" />

Floor3-L3SW

<img width="437" alt="image" src="https://github.com/user-attachments/assets/3e1b7e84-dd91-45bb-b806-bfc2a6cbaf1d" />

Floor4-L3SW

<img width="445" alt="image" src="https://github.com/user-attachments/assets/e723126e-a1bb-4bcb-9925-642960013115" />

Configuring IP Addresses on Core Layer Routers:

Floor1-Router

<img width="341" alt="image" src="https://github.com/user-attachments/assets/ebf523c0-1793-4dd3-ab3c-803164b0fc3f" />

Floor2-Router

<img width="325" alt="image" src="https://github.com/user-attachments/assets/70903b99-ed28-40d8-bc70-92f3181357a5" />

Floor3-Router

<img width="328" alt="image" src="https://github.com/user-attachments/assets/d7e30fe9-285e-4ffa-99d7-c3fe8068e186" />

Floor4-Router

<img width="322" alt="image" src="https://github.com/user-attachments/assets/0ace37fe-04d8-437c-adc9-e959aef131c1" />

Configuring OSPF on routers and layer 3 switches:

Floor1-Router

<img width="327" alt="image" src="https://github.com/user-attachments/assets/5399e339-7780-4992-9c58-3ca686487da6" />

Floor2-Router

<img width="324" alt="image" src="https://github.com/user-attachments/assets/5bf8a5e0-ec30-4559-87fd-86740f9e3a98" />

Floor3-Router

<img width="318" alt="image" src="https://github.com/user-attachments/assets/663a7f76-324e-407c-bd16-43241134fab9" />

Floor4-Router

<img width="329" alt="image" src="https://github.com/user-attachments/assets/d0bd4fe8-69b7-4c81-8bac-8ef443545c16" />

Floor1-L3SW

<img width="338" alt="image" src="https://github.com/user-attachments/assets/980bd56a-0ade-4377-bca8-05801783e620" />

Floor2-L3SW

<img width="328" alt="image" src="https://github.com/user-attachments/assets/548e55ae-9efa-4829-bbbf-0c22e8f72db9" />

Floor3-L3SW

<img width="326" alt="image" src="https://github.com/user-attachments/assets/b089b6d9-db92-47b4-9e92-549de59be4e2" />

Floor4-L3SW

<img width="327" alt="image" src="https://github.com/user-attachments/assets/50b43d54-3c3f-4f62-983c-4d7d94ee99ce" />

Configuring static Ips on servers:

DHCP Server

<img width="470" alt="image" src="https://github.com/user-attachments/assets/b5ffa121-1d7a-4f00-9b3b-5b25072374d0" />

HTTP Server

<img width="470" alt="image" src="https://github.com/user-attachments/assets/df6655ec-b1fd-4967-90bc-971d233942b0" />

Email Server

<img width="470" alt="image" src="https://github.com/user-attachments/assets/2a4a94a7-06cf-49d3-92b9-975dce3f2e15" />

Configuring DHCP Server pools:

<img width="470" alt="image" src="https://github.com/user-attachments/assets/556e9eec-71a2-4f3e-992a-eb6cb7e5c176" />

Configuring inter VLAN routing:

Floor1-L3SW

<img width="324" alt="image" src="https://github.com/user-attachments/assets/72c5cd6e-5827-4840-ae36-38511a077a5b" />


<img width="328" alt="image" src="https://github.com/user-attachments/assets/3315737b-cc95-456e-8752-5edf961190fd" />

Floor2-L3SW

<img width="330" alt="image" src="https://github.com/user-attachments/assets/a34a8d4f-5658-4027-809e-e216e0b65fbe" />


<img width="326" alt="image" src="https://github.com/user-attachments/assets/bd85918e-e282-42eb-9851-6ed4db8fbffb" />

Floor3-L3SW

<img width="320" alt="image" src="https://github.com/user-attachments/assets/3460a355-7e58-4a24-8ea5-5fca3e318f7b" />

Floor4-L3SW

<img width="333" alt="image" src="https://github.com/user-attachments/assets/e7c3927c-8543-44fa-be7f-64ed4587abad" />

Checking if DHCP is successful:

Management-PC

<img width="470" alt="image" src="https://github.com/user-attachments/assets/c8f109e3-55fd-4095-9714-7d84374fa964" />

Marketing-PC

<img width="470" alt="image" src="https://github.com/user-attachments/assets/7ae50db2-3764-44fa-b3f5-2f518fcb0ede" />

Guest-PC

<img width="470" alt="image" src="https://github.com/user-attachments/assets/57631ac9-36f3-4867-92f6-cc094acf8f28" />

Configuring Access points:

Research-AP

<img width="470" alt="image" src="https://github.com/user-attachments/assets/f06b3079-b55b-4b2d-8c3f-3b9e5c324935" />

Research-Laptop

<img width="470" alt="image" src="https://github.com/user-attachments/assets/a1a90dc7-919e-4c51-a3d3-6890ca3b2704" />

## Final Network in Packet Tracer

<img width="470" alt="image" src="https://github.com/user-attachments/assets/1d5d9c4a-4f1f-453f-99ea-012a79a623ea" />
