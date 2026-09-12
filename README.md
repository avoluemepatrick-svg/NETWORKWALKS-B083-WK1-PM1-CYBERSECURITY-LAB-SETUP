# NETWORKWALKS-B083-WK1-PM1-CYBERSECURITY-LAB-SETUP
build an isolated cybersecurity lab for pentesting and ethical hacking

skill cybersecurity, VirtualBox v7.2, kali Linux v2026.2, network 10.0.0.0/24, skill penetration testing, skill visualization, skill GitHub, NETWORKWALKS

PROJECT OVERVIEW

This project focuses on setting up a virtual cybersecurity and penetration-testing laboratory using VirtualBox and Kali Linux.

The purpose of the lab is to create a controlled environment where cybersecurity tools, network scanning, reconnaissance, vulnerability assessment, and other security-testing activities can be performed safely and repeatedly.

The lab is configured on a private virtual network so that additional machines can be added later and used as targets for authorized security testing.

OBJECTVES

These iclude

1. Install and configure VirtualBox

2. Install/import Kali Linux as a virtual machine.

3. Create a private NAT Network for the cybersecurity lab.

4. Configure network connectivity for Kali Linux.

5. Assign a consistent IP address to the Kali VM.

6. Verify network connectivity and DNS resolution.

7. Take a clean VM snapshot for recovery.

8. Document the complete setup process.

PURPOSE OF THE LAB

The lab provides an isolated and controlled environment for cybersecurity learning and authorized security testing.

1. Network reconnaissance

2. port scanning
 
3.Vulnerability assessment
 
4.Packet analysis

5.Web security testing

6. Exploitation practice
 
7. Security-tool experimentation


LAB SETUP PROCEDURES

STEP 1 INSTALL 7-ZIP

7-Zip was installed to extract the Kali Linux virtual-machine package, which may be distributed as a .7z archive.

Tool: 7-Zip

STEP 2 IINSTALL VIRTUALBOX

VirtualBox was install as the hypervisor

STEP 3 CREATE THE NAT NETWORK

A dedicated NAT Network was created in VirtualBox.

Configuration: Network Name: NatNetwork IPv4 Prefix: 10.0.0.0/24 DHCP: Enabled IPv6: Disabled

A NAT Network was selected because multiple virtual machines connected to the same NAT Network can communicate with one another while also having outbound network connectivity.

This will allow future attacker and target VMs to communicate within the lab

STEP 4. IMPORT KALI LINUX

The Kali Linux virtual machine was downloaded from the official Kali Linux website and imported into VirtualBox

STEP 5. CONFIGURE THE KALI LINUX NETWORK

The Kali Linux network configuration was checked and configured with a consistent IPv4 address.

A consistent IP address makes it easier to document the lab and reference the Kali machine in future exercises

IP Address: 10.0.0.2
Subnet Mask: 255.255.255.0
Gateway: 10.0.0.1
DNS: 8.8.8.8

STEP 6. CREATE A CLEAN VM SNAPSHOT

After completing the initial configuration, a VirtualBox snapshot was created.

Example snapshot name:

Clean Kali - Network Setup

The snapshot represents the clean baseline of the laboratory.

If a future exercise changes or damages the VM configuration, the machine can be restored to this baseline.

PROBLEMS ENCOUNTERED AND SOLUTIONS

PEOBLEM 1

CONFIGURATION OF THE KALI IP ADDRESS

using this syntax 

sudo ip addr flush dev eth0
sudo ip addr add 10.0.0.2/24 dev eth0
sudo ip link set eth0 up

and verify with

ip addr show eth0

PROBLEM 2.

ENABLE SHARED FOLDER

open VirtualBox - select kali VM - click setting - shared folder - click the + icon - select windows kali screenshot folder - tick AUTO-MOUNT, MAKE PERMANENT - ok 

WHAT I LEARNT

Through this project, I learned how to create and configure a virtual environment for cybersecurity practice.

The most important concepts I learned include:

1. NAT vs NAT Network
   
A standard NAT configuration and a NAT Network serve different purposes.

A NAT Network allows multiple VMs connected to the same virtual network to communicate with one another while providing network address translation for external connectivity.

This makes it useful for building a multi-machine cybersecurity laboratory.

2. Virtual Machine Networking
 
I learned how VirtualBox virtual network adapters connect virtual machines to different types of networks and how network configuration affects communication between machines.

3. Static IP Configuration
 
I learned how to configure and verify IPv4 addressing, subnet masks, gateways, and DNS settings in Kali Linux.

4. VM Snapshots
 
I learned that a clean snapshot should be created before performing risky or experimental activities.

This provides a known-good recovery point for future cybersecurity exercises.

5. Documentation
 
I learned that documenting commands, configuration, screenshots, problems, and solutions is an important part of a professional cybersecurity project.

TOOLS AND RESOURCES

7-Zip: https://7-zip.org/download.html

VirtualBox: https://virtualbox.org/wiki/Downloads

Kali Linux: https://kali.org/get-kali

AUTHOR

Avolueme Patrick

cybersecurity professional  B083

LinkedIn: https://www.linkedin.com/in/patrick-avolueme

PROJECT INFORMATION

Program Name: Cybersecurity at Networkwalks | Week: 01 | Project: Cybersecurity & Pentesting Lab Setup | Repository: GitHub




