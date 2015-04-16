---
title: "Part 3.1: XenServer Installation"
layout: post
date: 2015-02-15
image: 
---
![xenserver installation](/assets/img/Xenserver_Installation.jpg)
<p class="intro"><span class="dropcap">I</span>nstalling XenServer 6.5 was relatively straight-forward, both on bare metal as well as in a virtual machine. Anyone familiar with installing a Linux distro or other hypervisor should be relatively comfortable using the graphical installer. It takes you through typically steps such as setting a root password, networking information, as well as the option to install any supplement packages. After you've completed the installation your machine should reboot into XenServer. On all hardware I tested installation took less than 10 minutes and first boot was under 60 seconds on an SSD which is nice and quick.</p>

![Installation progress](/assets/img/Xenserver_Installation2.jpg)
__An important note regarding booting XenServer from USB:__ On one installation I ran into an issue where I could not boot into the Live USB I had created. After a few hours of googling around I stumbled across a fix which is below. In a virtual machine as well as on a third machine I had no issues so it seems to be a relatively isolated problem.

All the below commands are relative to the root of the USB drive you've created into a Live USB.

{% highlight bash %}
$ mv boot/isolinux/isolinux.cfg boot/isolinux/syslinux.cfg
$ mv boot/isolinux boot/syslinux
$ mv syslinux.cfg syslinux.cfg.bak
{% endhighlight %}

###Management of XenServer
![Xenserver host](/assets/img/Xenserver_HostManagement.jpg)
Once you've booted into XenServer you will be presented with the host management side of things. I was pleasantly surprised with the amount of tools available to you from the host console. In comparison to other hypervisors XenServer gives you far more options to manage things directly on the host. You can do the the expected basics such as looking at and modifying network and authentication settings along with access to the local shell. You can also however view your current virtual machines as well as resource pools which is incredibly useful.

Moving away from managing things directly on the host you will primarily be working with XenServer through the XenCenter Windows Management Console. As the name implies it is unfortunately a Windows only tool. This does require you to have a Windows machine handy. Alternatively if you use Linux or OS X you can always spawn a Windows virtual machine. I will note there is a third party application called [Xen Orchestra](https://xen-orchestra.com) that allows you to manage your host from a web interface. It's not a complete replacement for XenCenter but I will go over it in more detail later on.

A cursory glance over XenCenter shows us that it is relatively simply laid out interface. Your hosts and virtual machines are listed down the left hand pane in a tree structure, as well as any clustering that you have setup. Most of what you'll be doing takes place in the centre of the interface, along with easy to access toolbars. It's not an overly pretty interface but it is clear and doesn't get in the way of managing your hosts and virtual machines.

I'll cover various aspects of XenCenter as we go through the processes of creating and managing virtual machines.

![XenCenter](/assets/img/XenCenter1.png)
###Creation of Virtual Machines 

I strongly believe that the ease with which you can create a new virtual machine is a very important aspect of managing a hypervisor. If creating, editing, and using virtual machines through a management interface is not intuitive I see little reason to use the hypervisor. In this regard XenServer both succeeds and fails in various ways.

My biggest frustration with XenServer is how it handles ISO files for use by the host to create a virtual machine. ISOs are often used as the installation medium for the OS over a typically CD or DVD drive that needs to be passed through to the VM. XenServer uses what is called a an ISO Library. Simply put, this is a folder that the host has access to, via NFS for example, that has your ISOs stored. When starting up a new VM you get to choose an ISO from the Library to be used as the installation medium. You cannot use a ISO saved on your local machine running XenCenter or anywhere else. For some this may be a good thing as they can centrally store and organize their ISOs, as well as providing access to the same group of ISOs for multiple hosts. Personally I spin up VM sporadically and with constantly changing ISOs that having to keep and management a collection of them is tedious. I like to simply download a new Linux release or Virtual Appliance ISO and get it running right away. With XenServer it requires an additional step in between. Ideally it would support both methods: your organized archive of ISOs in the Library, as well as being able to load local ISOs on the fly.

More details will be coming in Part 3.2!