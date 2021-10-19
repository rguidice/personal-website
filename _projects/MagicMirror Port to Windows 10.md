---
name: MagicMirror Port to Windows 10
tools: [Raspberry Pi, Bash]
image: https://ryanguidice.com/assets/project_images/MagicMirror_Port_to_Windows_10/MagicMirror%20Port%20to%20Windows%2010.JPG
blog: 1
github: https://github.com/rguidice/MagicMirror-Win10V2
description: Migrating a Linux tool to a Windows environment.
---
# MagicMirror Port to Windows 10:
### Migrating a Linux tool to a Windows environment
<br>
Ever since I got my first Raspberry Pi, I have been fascinated by the [MagicMirror](https://magicmirror.builders/) project, created by Michael Teeuw. The project was the most futuristic and visually intriguing RPi project I had seen created at the time, and I immediately saw its potential application in my life. At the time, I was running a third monitor in my desk setup that functioned as a testing monitor for whatever PC I was working on at the time. MagicMirror presented me with the opportunity to create a interactive screensaver for that third monitor that could run whenever I wasn’t using the third monitor.

I experimented with many of the modules available via the GitHub page for the MagicMirror project, and found a small collection of them that would be useful in my daily life. I set everything up using the excellent wiki page, and in no time, had the ideal interactive screen saver sitting right on my desk.

When a friend came over to see a couple weeks later, he was definitely impressed with the display’s capabilities. He didn’t have a RPi at the time, and was wondering if it could work on a Windows-based machine. I initially told him no, as it was built for use in Raspbian and would likely be difficult to run on any Windows OS.

That was until I heard about bash shell included in Git for Windows. I started experimenting with just attempting to install the MagicMirror program start away, but had some issues. I then installed Node.js, and after more tinkering, was able to get MagicMirror at least running, but could not get the actual display to appear.

After doing a little more research, I found [this](https://forum.magicmirror.builders/topic/4089/complete-walkthrough-install-magicmirror-on-a-pc-windows-7-10) excellent guide by user Mykle1 on the MagicMirror forums. They were able to create an excellent step-by-step guide that entire walks you through the whole process. After uninstalling everything and starting from scratch with their process, I was able to get MagicMirror running just fine on my Windows 10 PC… with some caveats.

Certain modules will always have issues based on their framework. One module that I loved on the RPi version was the [SystemStats](https://github.com/BenRoe/MMM-SystemStats) module by user BenRoe, which displays the processor temperature, system load, available RAM, uptime and free disk space of the RPi. This module will obviously not work on the Win10 version (although it appears user Mykle1 has made a [different one](https://github.com/mykle1/MMM-PC-Stats) for use on other types of PCs and tested in Ubuntu, which may provide a potential route for Windows ones). Other modules need a bit of editing to work with Windows, although thankfully with open-source software such as these modules, that is easily possible.

Overall, this project was a ton of fun and a real challenge for me. I was not actually successful in making it work entirely on my own, and I am thankful for other developers who have worked on other guides and workarounds. My friend is now running his own display in the background on a Windows machine.

Feel free to check out my [GitHub repository](https://github.com/rguidice/MagicMirror-Win10V2) that discusses this project (and includes the steps I took to reach a working version). Please ignore the cobwebs, that repo needs some serious cleanup that I just haven't gotten around to yet.
