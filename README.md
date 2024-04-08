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

### Snort IDS

In order to optimize my hardware ressources usage, I used Snort as a package on Pfsense.

[Here is how to cnnfigure it](https://www.youtube.com/watch?v=12u_chrgIKI)

![image](https://github.com/Hamza19Mouisset/SOC-Home-Lab/assets/117672234/f5e65b64-1518-4674-a2d6-b674f1eecfd8)

![image](https://github.com/Hamza19Mouisset/SOC-Home-Lab/assets/117672234/9310a42c-2f7c-47b7-91a0-4c60037c28fc)



### Victim Network

For this part, I used Windows Server 2022 and WIndows 10 Enterprise machines.

I followed the configuration steps provided by the Cyber Mentor. [Here you can find the instructions](https://www.youtube.com/watch?v=VXxH4n684HE&t=6517s&pp=ygUbYWN0aXZlIGRpcmVjdG9yeSBwZW50ZXN0aW5n)

![image](https://github.com/Hamza19Mouisset/SOC-Home-Lab/assets/117672234/d8bc78ae-1d29-436a-a3d9-b3c2ae9b9ffd)

I added 2 users.

Mary Yan

![Marie](https://github.com/Hamza19Mouisset/SOC-Home-Lab/assets/117672234/9d832642-f476-4e9d-b504-73ffae46d3c0)

John David

![jdavid](https://github.com/Hamza19Mouisset/SOC-Home-Lab/assets/117672234/710486cb-daf2-4c76-aa47-943561b770c6)

Then I added a service account and configure it for kerberoasting.

![kerb](https://github.com/Hamza19Mouisset/SOC-Home-Lab/assets/117672234/b3184cde-e721-4421-aa94-a9d1c5d7b7a1)

![kerb2](https://github.com/Hamza19Mouisset/SOC-Home-Lab/assets/117672234/c8e09c9c-b3d3-492a-8df7-58b979ab0bae)

### Splunk

I deployed Splunk on an Ubuntu Server Machine.

![image](https://github.com/Hamza19Mouisset/SOC-Home-Lab/assets/117672234/954c7b97-0ff8-48c9-ab4e-e8152919389c)

Upon successful installation. You will be able to access the Splunk web interface for configuration.

![image](https://github.com/Hamza19Mouisset/SOC-Home-Lab/assets/117672234/881ab150-0d02-4e3f-96bf-b2ff86927a59)

[Here are the steps I followed for that](https://www.youtube.com/watch?v=yP_PFRy-pdA&t=882s&pp=ugMICgJmchABGAHKBSJzcGx1bmsgdW5pdmVyc2FsIGZvcndhcmRlciB3aW5kb3dz)

Finally, if everything was well configured, you will see the logs in Splunk.

![logs](https://github.com/Hamza19Mouisset/SOC-Home-Lab/assets/117672234/d8a948fc-7ff3-4f2f-bd78-1717d485dfbb)










