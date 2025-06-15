# raspberry-pi-hole
Documentation for setting up a Raspberry Pi-Hole.

I found a Raspberry Pi 2B, somewhat forgotten and bashed about, under my bed. I've been itching to get started learning some networking and Linux skills, so here goes!

Hardware:

- Raspberry Pi 2B
- Power Supply
- Ethernet Cable
- Micro SD Card (32GB)*

Software:

- Raspberry Pi OS Lite

*Smaller memory would be sufficient, but that's what I had.

# Getting Started
Flash the OS
Download Raspberry Pi OS Lite and flash it to your SD card using Raspberry Pi Imager. 
I like using Raspberry Pi's software because you can already enable SSH. Press *Ctrl + Shift + X*. Then you can set the username and password and enable SSH through a simple click.

# Boot your Pi
Insert the SD card, connect power and ethernet, and boot it up. You can access it via SSH or connect a keyboard and monitor.
I wanted to learn how to use SSH, and found my Pi using 

```
ping raspberrypi.local
```
Then after finding the IP address you can type 

```
ssh 'username'@'ip address'
```

# Update everything
Run these commands to make sure your system is up to date:

```
sudo apt update && sudo apt upgrade -y
```

# Set a static IP
Pi-Hole works best with a static IP so your devices know where to find it. Apparently, you can set this up during the install or manually.

I had some trouble with this part and will share more details.

To intall enter the following code

```
curl -sSL https://install.pi-hole.net | bash
```
Follow the prompts to set it up. I chose the defaults mostly, but you can customize the DNS providers and interface.

# Configuration & Usage
Access the Pi-Hole dashboard at "http://your-pi-ip-address/admin"

Use the dashboard to see stats, block domains, and tweak settings.

You can point your router’s DNS to the Pi-Hole IP so all your network traffic goes through it, I've yet to try this.

# What I Learned So Far
- Basic Linux commands and navigation

- How DHCP and DNS work in a home network

- Setting up services on Raspberry Pi



Now to learn what I can really do with this thing.
