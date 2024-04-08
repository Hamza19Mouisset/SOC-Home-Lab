# SOC-Home-Lab

In this Repo, I will show the steps I followed to build a SOC Home Lab on my computer.

### Abstract

The project describes setting up a cybersecurity home lab with an emphasis on monitoring and detection. It gives me a realistic setting in which to configure, secure, and monitor an IT infrastructure, allowing me to put newly newly acquired knowledge to work in actual situations. The components consist of a Kali Linux machine for attacking, pfSense firewall, Snort IDS, Windows Server as a domain controller, and Splunk for log management. The project places a strong emphasis on practical instruction and risk-free cybersecurity exploration.

### My Computer

I built the lab on a DELL Latitude 5520 laptop. It had the following configuration.
* Intel Core I5-1135G7 processor
* 16 GB of memory
* 512 GB NNMe
* Windows 10 Professional

### Downloading the Hypervisor

For this I used VMware Workstation.

[Link to Download](https://www.vmware.com/content/vmware/vmware-published-sites/us/products/workstation-pro/workstation-pro-evaluation.html.html)

You can alternatively use [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

Or Enable the built-in Windows Hypervisor which is [Hyper-V](https://techcommunity.microsoft.com/t5/itops-talk-blog/step-by-step-enabling-hyper-v-for-use-on-windows-10/ba-p/267945#:~:text=1%20Ensure%20that%20hardware%20virtualization%20support%20is%20turned,taskbar%2C%20type%20Hyper-V%20Manager%20and...%20.%20See%20More.)

### Downloading and configuring the firewall 

You can download pfsense [here](https://www.pfsense.org/download/)

Here is my pfsense configuration

![image](https://github.com/Hamza19Mouisset/SOC-Home-Lab/assets/117672234/c49c62a7-3f8e-4a43-910d-675c86ba7642)

I added 4 Network Adapters:

* NAT interface for Internet connection
* VMnet3 for kali linux machine
* VMnet4 for the Victim Network
* VMnet5 for Splunk

We will then need to assign IP addresses to the interfaces:

![image](https://github.com/Hamza19Mouisset/SOC-Home-Lab/assets/117672234/eac687dc-a239-4a98-942a-e5590468d749)

Finally, we will head to teh Pfsense admin interface to configure the firewall rules.

![image](https://github.com/Hamza19Mouisset/SOC-Home-Lab/assets/117672234/12c1e2bd-df64-4de0-94b0-d31a273ae3dc)

### Victim Network

For this part, I used Windows Server 2022 and WIndows 10 Enterprise machines.

I followed the configuration steps provided by the Cyber Mentor. [Here you can find the instructions](https://www.youtube.com/watch?v=VXxH4n684HE&t=6517s&pp=ygUbYWN0aXZlIGRpcmVjdG9yeSBwZW50ZXN0aW5n)

![image](https://github.com/Hamza19Mouisset/SOC-Home-Lab/assets/117672234/d8bc78ae-1d29-436a-a3d9-b3c2ae9b9ffd)



