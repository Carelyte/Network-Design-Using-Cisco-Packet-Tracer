# Network-Design-Using-Cisco-Packet-Tracer
Building a secure office network
# Overview of Project
A small company with three departments (Admin, Sales and IT) needs a network with access to the internet. All departments are entitled to different VLANs to avoid inter-VLAN routing (restriction from accessing each others file) where only Admin will have access to the File Server and everyone will have access to the internet.
# Tools Used
Cisco Packet Tracer
1. 4 PCs (one for each department and one serving as internet host)
2. 3 switches (one for each department, where the File Server is connect to that of the Admin)
3. 4 routers (one for each department and one for internet access)
4. 1 File Server
# Setup and Security
Each PC (for each departemt) were connect to their own switches and then to their routers, then the routers are connected to the internet router. 
Each department has its own VLAN where only the file Server shares the same VLAN with the Admin department (the should be the only department to have access to the File Server).
Each router and Switches were assigned UAV and console passwords to avoid unathorised access to the departments. 
Necessary inter-VLAN routing was enable and the Sales and ID departments were restricted from accessing the File Server using ACLs.
# Challenges Faced
1. Cable and Port Issues 
We had trouble getting devices to connect properly because of wrong cable choices and 
unclear port functions. Figuring out which cable matched each connection fixed most of 
the problems. 
2. VLAN Communication 
Setting up separate VLANs was easy, but allowing just Admin to access the file server 
required inter-VLAN routing with router-on-a-stick and careful trunk configuration. 
3. Internet Simulation 
The cloud device didn’t let us simulate internet access properly, so we replaced it with a 
router and a PC using 8.8.8.8 to act as the internet, which gave us more control. 
4. IP Assignment Errors 
Some router ports wouldn’t accept IP addresses because they were switchports. 
Switching to real routed interfaces solved the problem. 
5. Ping Failures 
We struggled with devices not responding to pings. These issues were usually caused by 
incorrect subnets, missing gateways, or misconfigured access rules. 
6. Limited Router Ports 
We ran out of available ports on the routers and had to switch to models like ISR4331, 
which support more routed interfaces.
7. File Server Restrictions 
All departments could access the file server at first. We fixed this by applying ACLs to 
allow only the Admin network through. 
# VLAN Configurations 
Each department was placed in its own VLAN. Inter VLAN routing was set up with only 
Admin allowed to access the file server. 
# Security Features 
Console and enable passwords were set. Port security was used to limit one device per 
port based on MAC address. 
# File Server Access 
The server was placed in the Admin VLAN. An access list blocked other VLANs, 
allowing only Admin to reach it. 
# Lesson Learned from this Project
1. Planning First Saves Time: Mapping out the network before diving into configurations helped avoid errors later.
2. Team Collaboration is Key: Clear communication made troubleshooting easier and faster. 
3. Practice Makes Perfect: Repeating configurations like port security and access lists made us more confident.
4. VLANs Are Powerful: VLANs effectively improve security and control traffic within a network.
5. Attention to Detail: One wrong IP address or untagged port can break the whole network
# Advice and Tips for others
From our experience with this challenge, here are some tips that we wish we had earlier - and we hope they help you too.
1. Start simple, then build up: Don't try to do everything at once. Begin with device placement and basic connectivity before diving into VLANs or advanced security. It makes troubleshooting way easier.
2. Label everything clearly: Use meaningful names for PCs, switches, and routers. This helped us stay organized and made the network easier to understand, especially during testing.
3. Document as you go: It's tempting to configure everything first and explain later - but it's better to document each step while it's fresh. This made our final slides clearer and saved us time.
4. Test access early and often: After VLAN configuration, run ping tests frequently. It's better to catch access issues early than to debug everything at the end.
5. Security is not just a checkbox: Port security, passwords, and restricting access are not just tasks - they're what make your network realistic. 
6. Use Packet Tracer shortcuts wisely: The simulation can lag with many devices. Use logical spacing and hide layers if needed to keep things tidy.
7. Communicate with your team: Collaboration made a huge difference for us. Assign tasks, share findings, and keep each other updated to avoid overlap or confusion. 
8. Have fun with it: This was more than just a technical task - it was a creative challenge too




