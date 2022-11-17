---
title: "OverTheWire Natas Levels 01-05"
date: 2022-11-17T21:56:39+05:30
tags: ['update','Wargame','CTF']
---

# Natas as a Start 

Over the next few weeks, I will try and post a complete walkthrough guide for the **Natas** war game that you can play over at [OverTheWire](https://overthewire.org/wargames/natas/).  The **Natas** is a war game based around web exploitation and pentesting, to start playing **Natas** we can simply visit the url and enter the password given to us. (Note: As we complete a room in these Wargames we are given the password to access the next room and move forward in a journey) 
![](/static/Blog2/Natas0-start.png)

Anyway, let's start **_Natas_**

## LEVEL 00
We are given the [URL](http://natas0.natas.labs.overthewire.org/) and the login username and password for the page (_natas0_). The objective of the Room is to find the password for the next room, add the landing page also tells us about it

![](/static/Blog2/Natas0-home-info.png). 

We can see there is nothing else present on the page, so let's view the page source instead, and there amongst the HTML we can the password for the next![](/static/Blog2/Natas0-password.png). 

Moving right along...

## LEVEL 01
Moving on to the next room, we enter the username "*_natas1_*" and the password we got from the last room. We are greeted with this bit of information 
![](/static/Blog2/natas1-home-info.png) 

and trying to right-click lead to JavaScript alert telling us 

![](/static/Blog2/natas1-rightclick-result.png).

As the page still seem mostly empty, let's try looking at the source by pressing <kbd>Ctrl</kbd>  + <kbd>u</kbd>. This show us the password for the next room.

![](/static/Blog2/natas1-password.png)

## LEVEL 02
