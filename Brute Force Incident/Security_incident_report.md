## Section 1: Identify the network protocol involved in the incident

The protocol impacted in this incident is HTTP (Hypertext Transfer Protocol). An analysis
of the DNS & HTTP traffic logs shows the potential download request of the malicious
file through the HTTP:GET method, as following this, the user gets rerouted to a
different website. 


## Section 2: Document the incident

The website owner reported several customer reports about the website prompting them to 
download a file to update their browsers. The customers claimed that, after running the file,
the address of the website changed and their personal computers began running more slowly. 
In response to this incident, the website owner tried to log in to the admin panel but found themselves
locked out of the account. 

The incident was then reported to this team. To address the incident, we 
created a sandbox environment to observe the suspicious website behavior. We ran the network protocol
analyzer tcpdump and typed in the URL for the website, yummyrecipesforme.com. As soon as the website
loaded, we were prompted to download an executable file to update the browser. On accepting the
download and allowing the file to run, the browser redirected to a different URL, greatrecipesforme.com
made to mimic the legitimate website. The tcpdump logs revealed that a GET request was made through HTTP
when the download was accepted and executed, and the browser started a new connection request with the
mimic website, greatrecipesforme.com. 

A senior analyst then analyzed the source code of the downloaded file and the website and noticed that
javascript code had been added to prompt website visitors to download an executable file that contains
a script to redirect the visitors’ browsers from yummyrecipesforme.com to greatrecipesforme.com. 

The web server may have been impacted by a brute force attack possibly because the admin password was
still set to the default password, leaving it vulnerable. The malicious executable file compromised
the users' computers.


## Section 3: Recommend one remediation for brute force attacks

- For the admin account, the default password must be changed as it easy to brute force the default.
- For the user accounts, two-factor authentication (2FA) may be employed to reduce chances of a brute force as
additional authentication via phone or email is required.
- Additionally, password checks may be impelemted to enforce the requirement of created strong passwords and the
number of unsuccessful login attempts from the same IP can be limited.
