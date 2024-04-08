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

![image](https://github.com/Hamza19Mouisset/SOC-Home-Lab/assets/117672234/c49c62a7-3f8e-4a43-910d-675c86ba7642)

