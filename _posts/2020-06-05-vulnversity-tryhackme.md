---
layout: post
title: My journey into Cybersecurity - tryhackme vulnversity
---

<img src="/images/journey_unsplash.jpg" alt="the journey is on - letters made of glass">

During my life I have always been fascinated by tech, which brought me from web dev to data science and data engineering. On thing the services I have had the pleasure to work on at was their need to be pen-tested and security-audited in accordance with our best-practice approach. 
For the longest time I felt the urge to learn more about what the pen-testers/auditors actually did - not anymore. 

I started watching Nahamsec, superhero1 and Ashf0x on twitch to familiarize myself with current trends and found [tryhackme.com ](https://www.tryhackme.com) as a good ressource for starting the journey. 


## summary
The setup for pen-testing the tryhackme-boxes (capture the flags) includes kali-linux in a vm, learning about burpsuite and packet interception, exploits of upload forms, getting a reverse shell, privilege escalation to get a root shell and finally obtaining all the flags for the first time. 


## So how does all of this work? 

After installing kali in a vm we connect via vpn to tryhackme with their provided openvpn config.
Then we can start the box, copy the IP and start reconnaissance. 

1. check if it is a web server by entering the IP into a browser
1. to find open ports we can utilize a tool called network mapper (nmap):

```bash
nmap -sV <box ip>
```

1. We will see that 6 ports are open and one of them `3333` is exposing what seems to be a webserver
1. upon opening the <box ip>:3333 we can see a landing page which confirms that this is a webserver
1. next we can use a enumeration to identify which urls can be reached by employing a common-wordlist together with GoBuster
  
  TO BE CONTINUED
