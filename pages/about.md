---
layout: page
title: About
permalink: /about/
weight: 1
---

# **About Me**

Hi, I am **{{ site.author.name }}**.<br>

<p>Welcome to my website!</p>

<p>I am currently a computer engineering student at Colorado State University.</p>

<p>Outside of my studies, I enjoy soccer, photography/videography, and working on personal projects (such as this site).</p>

<p>The purpose of this website is to serve as a hub for my professional and personal endeavors. You can review an updated blog of whatever I’m working on in the <a href="http://localhost:4000/projects/">Projects</a> section.</p>

<p>I have experience with Java, Python, HTML/CSS, batch and bash scripting, assembly, Git and Matlab. My current workflow mainly uses the Atom text editor, along with Eclipse for Java development and Anaconda for Python development. I have also used Quartus II for logic design, Keil uVision for microprocessor and the Windows deployment kit, WinPE and Hyper-V for Windows image capture and deployment.</p>

<p>I also have experience using Wordpress, Adobe Photoshop, Premiere and Lightroom for creative endeavors.</p>

<h5><strong><center><a href="mailto:ryan@ryanguidice.com">Full resume available upon request.</a></center></strong></h5>
<br>


<div class="row">
{% include about/skills.html title="Programming Skills:" source=site.data.programming-skills %}
{% include about/skills.html title="Other Skills:" source=site.data.other-skills %}
</div>

<div class="row">
{% include about/timeline.html %}
</div>
