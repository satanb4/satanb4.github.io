+++
title = 'Containerization'
date = 2024-11-25T17:52:33+01:00
author = 'Sayan Bandyopadhyay'
draft = false
description = 'A short blog on the history and use of containers'
tags = ['containerisation', 'blog', 'cloud']
categories = ['computing']
+++

# Virtualization and Containers (When, Where and Why?)

Containerize! This word is thrown around irreverently everywhere nowadays. "Is this application containerized? Is this a micro-services architecture? Can this be deployed in container form?" - Generic questions asked by everyone vaguely even familiar with the term in the industry. But the question has got to be asked, why bother going for a micro-services architecture, and why do we even need to containerize the "robust" application that we have just built?

![containers](https://cdn-images-1.medium.com/max/800/0*ca1XZPTXMrJ3OEY5)

Before containers, there was the Virtual (gear up for some history)-
The concept of creating a virtual space that is independent of your environment is decades old. Very much akin to virtual-reality that has been around since the 1980s. Basically, creating a space that does not affect reality and is a microcosm unto itself. This concept while widely popular, did not really implement application into the computing space immediately. While the world was climbing out of the primordial ooze of IBM mainframes and into desktop computing, server virtualization remained in the hands of the of the technological pioneers, mostly big tech companies in the 1960s (Bell Labs, IBM and GE).

System Virtualization for consumers came with the UNIX kernel, which allowed a single computer's resources to be split among multiple users (yes, that is virtualization too, something we take for granted nowadays). Fun fact:- UNIX brought the revolution of a kernel written in the C language, unlike its predecessors which were written in Assembly (oh, the pain) and made it into the computing equivalent of Ditto, being able to mould and compile itself onto any platform.
Application Virtualization was now the need of the hour, as we barrel into the 1990s of computing. Some engineers from Sun Microsystems (pepperidge farms remembers), being the finicky beings that all engineers are, decided that Sun's C/C++ APIs were cumbersome and a pain to deal with. And honestly, who are we to argue? This division of Sun being called "Stealth", "Oak" etc… Came to be known as - Any guesses?

**"JAVA"**

![JAVA](https://cdn-images-1.medium.com/max/800/0*Gia5SshbWMkFUA5S.jpg)

In 1995. Yes, Java was technically the first application virtualization platform. Since web-technology was now the baby-boomer, the Java compiled programs only needed the Java Runtime Environment (JRE) which runs on the Java Virtual Environment (JVM) to be present on any system to run the software. And there you have it, the first glory of virtualization that still hounds us to this day. In 1998, this tiny little company called VMWare came into existence and alongwith it brought in the twins, the ESX and the GSX servers. And yada, yada, as they say, the rest is history, with every major platform ie- Windows, Citrus, IBM coming up with their own virtualization software.

___

Now that we understand the history and geography of Virtualization, let's see where containers fit in.
Virtualization - Running multiple OSes on a single system
Containerization - Running multiple applications in a container engine within ONE host OS machine

Right off the bat, we can see how virtualization can mean hogging those precious computing resources spent on running multiple different OSes with their own schedulers, and CPU, Disk allocations.
Containers on the other hand are meant to run an application in its lonesome environment, independent of the host (sounds lonely, but engineers are terrifying people). Now imagine, having multiple of these application containers running and they being able to communicate their information with each other. Boom, you now have a microservices cluster and your application is buzzword approved "microservices-application".

**Where would you like to use this?** Honestly. Just use your imagination. 

If your application consists of multiple modules that require information being processed independently and need to be scaled up or down based on usage, that is perfect for a microservices architecture. Maintaining each module becomes a breeze in smaller teams since only the communications protocol needs to be standardized and every container can have a module of the application running in its own environment.
