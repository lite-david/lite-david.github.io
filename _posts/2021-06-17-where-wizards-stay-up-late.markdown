---
layout: post
title:  "Where wizards stay up late"
date:   2021-06-17 11:50:21 -0800
categories: Systems
---

_In 2018 I took a really interesting course called [Internetworking Technologies](http://prasad.talasila.in/courses/inet-201718/) taught by TSRK Prasad at BITS. As part of the reading assignment we had to review Where wizards stay up late: The origins of the Internet by Katie Hafner and Matthew Lyon. This is one of those pieces of written work at the intersection of technology and history that has inspired me and I've thoroughly enjoyed reading. The internet as you know it, where you're reading this, has a rich history and this book does a fine job of telling it._ 

_The book touches upon several issues which stands true in matters of research even today, like the bureaucratic issues in getting funding for a research project and opposition to any idea which questions the status quo. It also gives an insight into how back in the day researchers took crucial hardware software design decisions and thought about reliability since the beginning of the implementation. It silently instills a sense of appreciation for the efforts put in by various agencies in developing this infrastructure which is often just taken for granted today. Lastly it ensures that you don't look at the @ sign in your email id in the same way ever again._

_This blog post is an effort to provide a crisp summary of the events_


## ARPA is founded

The fear of being left out, surrounding the launch of the Sputnik satellites by the Soviet Union ultimately lead to the founding of the Advance Research Projects Agency (ARPA). After the launch of the Sputnik 2, the then Secretary of defense, Mr.McElroy, several scientists and prominent advisers, met many times discussing the need to set up a R&D division. 

McElroy proposed to President Eisenhower to form a centralized agency for advance research projects to reduce the rivalry between the forces for getting the biggest share from the R&D budget. 

On January 7, 1958, Eisenhower requested the Congress for funds to establish the Advanced Research Projects Agency (ARPA) with Roy Johnson as ARPA's first director. Five days after the appointment, funding was approved by Congress and ARPA went into business.

## The birth of the computer network idea

Initially ARPA focused it's research on several space projects. However with the formation of NASA, all the projects were shifted from ARPA, and the organization shifted gears. From trying to beat the Soviet Union at Space technology it moved to being a high-risk, high-gain research sponsor. 

- In 1961, Jack Ruina, the first scientist to direct ARPA, brought about a decentralized structure in the agency. 
- ARPA ventured into computer science, with arrival of the Q-32 computer, passed down from the Air Force.
- J.C.R. Licklider, expressed his thoughts on starting a communication between the computers, and for the first time the idea of a computer network emerged. 
- He established research contracts with the best computer scientists at Stanford, MIT, UCLA, Berkely and few other companies.
- Bob Taylor, continued on Licklider's idea. He realized that scientists spent considerable time and resources duplicating software and programs rather than sharing them. He thought of computer networking as a better way of resource sharing, a level above time sharing on a single computer.
- Bob Taylor employed Larry Roberts as program manager to design and oversee the construction of the network.

## Packet Switching is invented

Independent researchers, Paul Baran and Donald Davies, arrived at the idea of packet-switching. Paul Baran was studying ways to build reliable communication systems and in doing so, he made several valuable contributions:

1. Set up networks with several redundant connections, like the neural networks in the human brain.
2. Have a decentralized network, with no central communications switch.
3. Divide the message to be delivered into several parts, and reassemble them at the receiver.
4. Dynamic routing or adaptive routing: Each node contains a routing table, which indicated how many hops were required to each other node in the network

However Baran faced severe opposition for his ideas, from the AT&T officials of the telecom industry. They didn't want to disrupt their well established circuit switched system. 

In the meanwhile, Donald Davies, also came up with the similar idea, with one major difference: Davies focused on the details of configuring the data blocks, instead of the reliability and redundancy tests that Baran focused on. Davies also foresaw the need to overcome differences in computer languages, machine procedures and hardware-software that would exist in a large network. He coined the name 'packet', for each fragment of the fractured message.

## The ARPA Net paper
At the end of 1967, at a conference in Gatlinburg, Tennessee, Roberts presented his paper titled the ARPA net. 

He described the intermediate computers or interface message processors (imps) that would control the network, forward packets and do error checking. He proposed to use ordinary dial-up phone lines to connect four nodes, but these lines were slow. 

Another paper was presented by Roger Scantlebury from Donald Davies' team which descrbed communication lines that operated much faster than the 2000 bits per second proposed by Roberts.

Roberts incorporated this papers techniques, as well as Baran's dynamic routing scheme and drafted a document with details of how the network should look like and what an IMP would be expected to do. 

The contract to build the IMP was given to a small firm called Bolt Beranek and Newman(BBN).

## Engineering the ARPA Net

The **Honeywell DDP-516** minicomputer was chosen to be modified into the IMP, because of its sophisticated I/O capability. It had non-volatile memory, as well as a watchdog timer enabling it to recover from crashes easily. Teams worked on the hardware as well as software of the IMP, keeping the code as small yet robust at the same time. 

Features which needed to be fast were implemented in hardware. The forwarding and routing algorithms were written in minimal lines of assembly instructions. BBN also gave specifications features which each of the four centers would have to independently develop for their host computers to support IMP software development. They also implemented a 24-bit checksum to check for errors in the packets.

After multiple iterations of debugging bugs in the honeywell system as well as resolving a synchronizer bug, the first IMP was finally set up at UCLA. A second IMP was set up at Stanford.

## "Lo" and behold, the rest is history
The first message over the internet or ARPA net was sent from UCLA to Stanford.

_Fun Fact: I recently got a chance to visit this building at UCLA with my friends Shashwat and Nitish. Suparno was kind enough to host us and give us the tour!_ 

Graduate students from UCLA, Stanford, UCSB and University of Utah formed a committee called Network Working Group, to discuss and design host to host communication protocols. The idea of a layered structure originated there.

Once all four nodes were set up, Bob Kahn performed tests to check congestion in the network and congestion control was implemented in the IMPs. Slowly and gradually, different host to host applications came up, beginning with Telnet, then FTP and e-mail.
