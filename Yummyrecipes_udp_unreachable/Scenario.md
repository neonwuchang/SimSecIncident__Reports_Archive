## Background
You are a cybersecurity analyst working at a company that specializes in providing IT consultant services. Several customers contacted your company to report that 
they were not able to access the company website yummyrecipesforme.com, and saw the error “destination port unreachable” after waiting for the page to load. 

## Investigation
You are tasked with analyzing the situation and determining which network protocol was affected during this incident. To start, you visit the website and you also
receive the error “destination port unreachable.” Next, you load your network analyzer tool, tcpdump, and load the webpage again. This time, you receive a lot of
packets in your network analyzer. The analyzer shows that when you send UDP packets and receive an ICMP response returned to your host, the results contain an error
message: “udp port 53 unreachable.” 

## Task
Now that you have captured data packets using a network analyzer tool, it is your job to identify which network protocol and service were impacted by this incident.
Then, you will need to write a follow-up report. 
As an analyst, you can inspect network traffic and network data to determine what is causing network-related issues during cybersecurity incidents. 
This incident, in the meantime, is being handled by security engineers after you and other analysts have reported the issue to your direct supervisor. 
