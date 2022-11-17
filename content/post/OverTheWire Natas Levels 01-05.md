---
title: "OverTheWire Natas Levels 01-05"
date: 2022-11-17T21:56:39+05:30
tags: ['update','Wargame','CTF']
---

# Natas as a Start 

Over the next few weeks, I will try and post a complete walkthrough guide for the **Natas** war game that you can play over at [OverTheWire](https://overthewire.org/wargames/natas/).  The **Natas** is a war game based around web exploitation and pentesting, to start playing **Natas** we can simply visit the url and enter the password given to us. (Note: As we complete a room in these Wargames we are given the password to access the next room and move forward in a journey) 
![](/Blog2/Natas0-start.png)

Anyway, let's start **_Natas_**

## LEVEL 00
We are given the [URL](http://natas0.natas.labs.overthewire.org/) and the login username and password for the page (_natas0_). The objective of the Room is to find the password for the next room, add the landing page also tells us about it

![](/Blog2/Natas0-home-info.png). 

We can see there is nothing else present on the page, so let's view the page source instead, and there amongst the HTML we can the password for the next![](/Blog2/Natas0-password.png). 

Moving right along...

## LEVEL 01
Moving on to the next room, we enter the username "*_natas1_*" and the password we got from the last room. We are greeted with this bit of information 
![](/Blog2/natas1-home-info.png) 

and trying to right-click lead to JavaScript alert telling us 

![](/Blog2/natas1-rightclick-result.png).

As the page still seem mostly empty, let's try looking at the source by pressing <kbd>Ctrl</kbd>  + <kbd>u</kbd>. This show us the password for the next room.

![](/Blog2/natas1-password.png)

## LEVEL 02
We know the routine now and immediately start looking at the page source. We can see amongst the ``HTML``  an ``img``  tag which is referencing an image named "_pixel.png_".
![](/blog2/natas2-img-html.png) 
If we visit this image, we can see a blank page, but the interesting thing is that we are now in a subdirectory called ``http://natas2.natas.labs.overthewire.org/files/pixel.png``
if we go back a directory, we find our self at an index of all the files used in the page and with it a **Directory listing vulnerability**
![](/Blog2/natas2-index.png) 
we can see a file called users.txt that has the contents:
``# username:password``
``alice:BYNdCesZqW``
``bob:jw2ueICLvT``
``charlie:G5vCxkVV3m``
``natas3:G6ctbMJ5Nb4cbFwhpMPSvxGHhQ7I6W8Q``
``eve:zo4mJWyNj2``
``mallory:9urtcpzBmH``
and we find our next password.
