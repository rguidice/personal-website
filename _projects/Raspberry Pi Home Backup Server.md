---
name: Raspberry Pi Home Backup Server
tools: [Raspberry Pi, SyncBack]
image: /assets/project_images/Raspberry_Pi_Home_Backup_Server/raspberry_pi_home_backup_server.PNG
blog: 1
description: An experiment in cheap network storage.
---
# Raspberry Pi Home Backup Server:
### An Experiment in Cheap Network Storage
<br>
After dealing with multiple hardware swaps on my personal PC and some situations that could’ve led to data loss, I decided that it would be worth it to invest in a backup solution for my family. At the same time, I was experimenting with the (at the time) brand-new Raspberry Pi Model 3. I figured that there was likely a decent way to create a home backup server using the raspberry pi as a network and data controller, and possibly attach an external hard drive as data storage.

[This](https://www.howtogeek.com/139433/how-to-turn-a-raspberry-pi-into-a-low-power-network-storage-device/) excellent article from How-To Geek helped me get started and oriented with all of the potential ways to pursue this idea. I ended up going down a similar path as them, with some changes to reflect my use-case.

First, I set up a fresh install of Raspbian on the pi and started configuring the hard drive. For a more budget-oriented solution, I went with a 2tb external HDD from WD ([this one I believe](https://www.2brightsparks.com/freeware/freeware-hub.html)). Since I had two computers who would be making routine backups to this drive, I initially went to partition the drive into two sections. After some thought though, I decided to partition it into three sections:

* 1tb for my parent’s machine
* 750gb for my machine
* 250gb for network storage

By doing it this way, I would allow myself 250gb of space to keep on the network to mess around with. This has come in handy when transferring files between machines (no more need for a USB drive back and forth, just toss it on the network drive) and media hosting as well.

From here, I installed Samba to enable the drive to be used over the network. After configuring the setup to match my standard for credentials and security, I was ready to test everything. I immediately hit a rough spot, where I was having trouble discerning where specific password changes were reflected within the network setup.

After some research into how Samba actually works, I was able to figure out that I was totally wrong about how my assumptions into what passwords were used where, and I had to redo quite a bit of the installation to ensure nothing was improperly configured.

Finally I had everything ready to use, and data could be transferred back and forth over the network. But now, how should I backup many different folders over time and control these backups? This could easily get very convoluted and messy. Luckily I found a program called [SyncBack](https://www.2brightsparks.com/freeware/freeware-hub.html) that supported exactly what I needed. On top of options for selecting individual files and folders, it also supports scheduling backups.

After configuration, my parent’s PC now backs up to the drive every night, over the network. Since I don’t leave my PC on all the time, I just backup whenever I remember, which has worked very well so far. We now have a second copy of any data that is important in hand at any time, and due to the nature of the setup, the backups are entirely readable without any other help. The drive, if needed, could be unplugged and used as a normal USB external hard drive to pull off any data needed very easily.

This project was great because I was able to continue experimenting with raspberry pi’s, all while learning how Samba and network drive configuration works. Now, my family doesn’t have to worry about any potential data loss issues, and it is accomplished with a low-power, cheap and easy to configure option.
