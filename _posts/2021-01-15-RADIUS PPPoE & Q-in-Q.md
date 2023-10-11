---
layout: post
title: RADIUS PPPoE & Q-in-Q
lead: 
---

<a><img src="https://i.ibb.co/3NDyTB4/msedge-8ri-Jf-XFe-Ct.png" alt="msedge-8ri-Jf-XFe-Ct" border="0"></a>

<h1 style="color: grey;"> Outcomes </h1>

I successfully implemented particular ISP elements within a GNS3 virtual environment using Cisco IOSvL2 switches, and Cisco IOSv routers. The implemented ISP elements within this assignment are as follows:
- RADIUS Authentication through PPPoE
- Q-in-Q Tunneling.
Implementation of both ISP elements has been successful. The outcome of this implementation is as 
follows:
- PPPoE successfully authenticates Customer routers through the use of a FreeRadius server 
running within the ISP.
- When successfully authenticated, the interface Dialer1 of the Customer Router is granted an IP 
address. The Dialer1 interface is linked to the outgoing G0/1 interface of the Customer router. 
The result of being allocated this IP address is that hosts behind the Customer Router can now 
interact with the ISP network, simulating a real-life instance of a router connecting to an ISP.
- If a customer router becomes unauthenticated, the IP address is stripped, and the 
unauthenticated customer region can not interact with the ISP region.
- The result of being successfully authenticated against PPPoE, and with the Customer router now 
being allocated an IP address, the hosts of one Customer region can now ping the other hosts 
within another authenticated Customer region. All Customer regions are on VLAN 12, while the 
service-provider Q-in-Q tunneling region is allocated VLAN 150. This setup shows correct 
implementation of Q-in-Q tunneling as packets are double-tagged.
- Static routes have been set within each Customer region, allowing for successful pings across 
regions to provide proof-of-concept for the Q-in-Q tunneling implementation, taking note that 
static routes have been used instead of dynamic routing methods due to the size of the network
(External/Internal BGP).
- DHCP has also been implemented on the Customer Router interface G0/0 of both regions. This is 
to provide IP addresses to clients automatically. 


<h2 style="color: grey;"> Devices </h2>

- All Routers: Cisco IOSv Version 15.6(2)T 2016
- ISP Switches: Cisco vIOSl2 15.2 2017
- RADIUS ISP Servers: Ubuntu 16.04 LTS – FreeRadius Server running
- Customer Switches: Standard GNS3 Switches
- End Clients: GNS3 Virtual PCs.

<h2 style="color: grey;"> Design considerations </h2>

During the design planning for this network, I had to take into consideration the needed elements that 
each device had to be capable of for completing this assignment. Due to Cisco virtual IOS images not 
including everything that the physical Cisco IOS counterpart contains, I had to ensure that elements such 
as Q-in-Q Tunneling, and PPPoE were possible on the images. 

The choice of switches determined if the image was capable of configuring Q-in-Q tunneling. Luckily, as 
of recently, Cisco had updated their images to include the capability of configuring Q-in-Q tunneling on 
their vIOSl2 images. 

The use of the standard GNS3 Switches and GNS3 Virtual PC’s were made final as no configuration on 
the end-user switches was needed, along with only needing end-users as test clients for connectivity.

I sat (and subsequently) passed the CISSP earlier this year, thus earning the associate of ISC2 status!

Such pass of the CISSP was no small feat - I carried out 140 days of study across numerious study materials to gain the confidence to go ahead and attempt the 4 hour exam.

I passed the CISSP at 145Q with around 50 minute remaining! This was my first attempt.

![placeholder](https://i.ibb.co/xgbfWPx/WINWORD-ymbp-PKp-Top.png "Just a couple word docs from my studies!")

<h2 style="color: green;"> Studies </h2>

I started the journey November 2022 via the Destination Certification Masterclass.

The Masterclass presents the information in a way that is not even comparable to any of the other study material I had a look at.

![placeholder](https://i.ibb.co/wN78PRw/WINWORD-BKX2-Q53c1z.png "Masterclass present")

It is a very concise course that explains exactly what you need to know in a very clear way. The course is built and presented in a way to automatically make you think like a CEO without even knowing it. Videos presented within the course range from 5-20 minutes, and each video comes with it's own written summary including easily digestible diagrams. There are multiple end-of-domain knowledge assessments which cover the most critical areas, and an end-of-class practice test.

All throughout my study towards achieving the CISSP, my tutor Lou was available for guidance via my purchase of the Destination Certification Masterclass. He was essential to my passing of the exam, and is extremely knowledgeable surrounding all things CISSP. He took great care in ensuring I was on the correct path during my studies.

<h2 style="color: green;"> Exam </h2>

I was taught to read the question 3 times, and not even look at the answers until you point out the key words to figure the answer out on your own. This stops potential answers from messing with your thinking.

Some questions required me to sit back for a moment after re-reading the question 11 times, and some questions I knew straight away the answer. I was able to easily remove 2 wrong answers.

Comprehending questions is half of the job, most of the time it wasn't even the language, or wording of the questions that made it confusing, you could understand what it's asking, but then the answers would be worded in a way that really tests your abilities to link all your knowledge together.

<h2 style="color: green;"> Verdict </h2>

It was a difficult exam. I can see how someone could know all the topics but still not pass if they don't have the perspective that ISC2 is looking for.

The exam is really a mile wide, inch deep, and will challenge you quite rigorously across all domains while using language that makes you think.

Achieving the CISSP is a very big milestone for me, and I owe it to the masterclass, and everyone in the community who sticks around to help out.


