---
title: "Personal Cloud Service"
excerpt: "<p><b>2020</b></p>
I built a personal cloud service at home, covering everything from hardware to software. It offers VPN connectivity, file storage, media services, and an ML computing node, among other functionalities. <br/><img src='/images/home_network.png' width='500'>"
collection: projects
---

<!-- My personal cloud service set at home, where I built from hardware to software, which can provide VPN connection, file storage, media service, ML computing node and etc. -->
I built a personal cloud service at home, covering everything from hardware to software. It offers VPN connectivity, file storage, media services, and an ML computing node, among other functionalities. The network topology is shown in the figure.

![Topology](/images/home_network.png)

## Gateway
<!-- The router hardware is a x86 embedded computer running EXSI hypervisor, under which iKuai and OpenWRT work as the routing OS. 
iKuai mainly works for DHCP, DNS, NAT and traffic control. OpenWRT works as a bypass router providing the VPN and other special service. -->
The gateway is an x86 embedded computer running an ESXi hypervisor, hosting both iKuai and OpenWRT as the routing operating systems. iKuai manages DHCP, DNS, NAT, and traffic control, while OpenWRT serves as a bypass router, handling VPN and additional specialized services.
To connect from outside, DDNS is used to bind a domain name with a dynamic public IP. All requests are forwarded to specific server and port by incoming port number through static NAT rule.
The VPN service enables secure remote control of all computers within my home network and provides my family with access to Google and YouTube from China.


## File & Media Service
A self-built NAS (Network-Attached Storage) server is deployed to handle file and media services, offering file synchronization, backup, sharing, and a video and photo station. For data security, the HDD array is configured in RAID 1.
The NAS server also runs Docker containers for lightweight services.


## Computing Node
<!-- The computing node is an on-demand server, which can be waken through internet to use less power, where I have a shortcut on my iPhone. It configures with a RTX 2080Ti (set up on 2018) and can be accessed through SSH or VNC (Virtual Network Computing). -->
The computing node is an on-demand server that conserves power by remaining in sleep mode until awakened via the internet. I can just start it through a shortcut button on my iPhone. Equipped with an RTX 2080 Ti (installed in 2018), it can be accessed remotely through SSH or VNC (Virtual Network Computing).





