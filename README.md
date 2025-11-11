# Overview 

The goal of this assignment is to further practice computing network performance metrics based on given scenarios.

# Instructions

Answer the following questions by showing your work. You should write your responses directly in this Markdown file.

# Q1

Suppose Host A wants to send a 7 MB file to Host B. The path between Host A and Host B includes three links with the following capacities and current usage levels:

* Link 1: 1 Mbps (30% utilized)
* Link 2: 800 Kbps (10% utilized)
* Link 3: 3 Mbps (70% utilized)

Questions:

* What is the effective throughput available for the file transfer?
* Approximately how long will it take for the file to reach Host B?

```
# Link 1: 1 Mbps x (1-0.3) = 0.7 Mbps
  Link 2: 800 Kbps x (1-0.1) = 720 Kbps
  Link 3: 3 Mbps x (1-0.7) = 0.9 Mbps
  The Slowest link determines the maximum throughput, so from (0.7, 0.72, & 0.9 Mbps). 
  Throughput = 0.7 Mbps

# File size = 7 x 8 = 56 Mb 
  Transfer Time = File size/Throughput
  Transfer Time = 56 Mb/0.7 Mbps
  Transfer Time = 80 seconds
```

# Q2

How many bits are expected to arrive with errors during the transmission of a 500 MB file, assuming a bit error rate (BER) of 10^-6?

```
# File size = 500 MB x 8 = 4000 MB = 4,000,000,000 (4x10^9) bits
  BER = 10^-6

  Errors = Total bits x BER
  Errors = (4x10^9) x (10^-6)
  Errors = 4000 bits
```

# Q3

![pic1.png](pics/pic1.png)

What is the overhead percentage of an Ethernet frame that carries 500 bytes of payload?

Refer to the Ethernet frame structure shown above. Show your work and explain your reasoning.

```
# Header = Dst MAC + SRC MAC + Type/Length
  Header = 6 bytes + 6 bytes + 2 bytes = 14 bytes
  DATA (Payload)= 500 bytes
  FCS (Trailer) = 4 bytes
# Total Frame size = 14 + 500 + 4 = 518 bytes
# Overhead bytes = 14 + 4 = 18 bytes

# Overhead Percentage = (Overhead bytes/Total frame size) x 100%
  Overhead Percentage = (18/518) x 100%
  Overhead Percentage = 3.475 %
The overhead percentage of an Ethernet fram that carries 500 bytes of payload is 3.48%.

```

# Q4

A packet sent to a target host must travel through three hops, with each intermediate device introducing the following delays:

* Hop 1: 3 ms
* Hop 2: 5 ms
* Hop 3: 2 ms

What is the total end-to-end delay for the transmission?

```
# Total Delay = Hop1 + Hop2 + Hop3
  Total Delay = 3ms + 5ms + 2ms
  Total Delay = 10ms
Total end-to-end delay for the transmission is 10ms.
```

# Q5

A router has an input queue that can hold up to 10 packets. Each packet takes 0.5 ms to be processed. If the router already has 7 packets in its input queue, what is the expected queuing delay for a newly arriving packet?

```
# Queuing Delay = 7 packets x 0.5 ms
  Queuing Delay = 3.5 ms
The Expected queuing delay for a newly arriving packet is 3.5 ms.
```

# Submission

Update your remote repository by pushing this README file. 