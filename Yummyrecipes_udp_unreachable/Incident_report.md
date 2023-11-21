## Part 1: Provide a summary of the problem found in the DNS and ICMP traffic log
The UDP protocol was used to request a domain name resolution using the address of the DNS server over port 53.
Port 53, which aligns to the .domain extension in 203.0.113.2.domain, is a well-known port for DNS service.
The message did not go through to the DNS server. The browser was not able to obtain the IP address for 
yummyrecipesforme.com, which it needs to access the website, because no service was listening on the receiving DNS
port as indicated by the ICMP error message “udp port 53 unreachable.”


## Part 2: Explain your analysis of the data and provide one solution to implement
The incident occurred when several customers reported that they were not able to access the company website 
www.yummyrecipesforme.com, and saw the error “destination port unreachable” after waiting for the page to load. 
The team responded by first trying to visit the website and the same error was replicated, tests were run with the 
network protocol analyzer tool tcpdump. The resulting logs revealed that port 53, which is used for DNS service, is 
not reachable. We are continuing to investigate the root cause of the issue to determine how we can restore access to
the website. The analysis team reported to the supervisor and the case has been handed over to the security engineers
team. 

Our next steps include checking the firewall configuration to see if port 53 is blocked and contacting the 
system administrator for the DNS server to have them check the system for signs of an attack such as a DoS. 
