## Section 1: Identify the network protocol involved in the incident
http





## Section 2: Document the incident
Website owner reported several customer reports about the website prompting them to download a file to update their browsers. The customers claimed that, after running the file, the address of the website changed and their personal computers began running more slowly. In response to this incident, the website owner tried to log in to the admin panel but was unable to. The incident was then reported to this team. To address the incident, we created a sandbox environment to observe the suspicious website behavior. We ran the network protocol analyzer tcpdump and typed in the URL for the website, yummyrecipesforme.com. As soon as the website loaded, we were prompted to download an executable file to update the browser. On accepting the download and allowing the file to run, the browser redirects to a different URL, greatrecipesforme.com made to mimic the legitimate website. A senior analyst then analyzed the source code and noticed that javascript code had been added to prompt website visitors to download an executable file that contains a script to redirects the visitors’ browsers from yummyrecipesforme.com to greatrecipesforme.com. 
The web server may have been impacted by a brute force attack possibly because the admin password was still set to the default password, leaving it vulnerable.




## Section 3: Recommend one remediation for brute force attacks

Some of the common security methods used to prevent brute force attacks include:
Requiring strong passwords
Enforcing two-factor authentication (2FA)
Monitoring login attempts
Limiting the number of login attempts
One measure applicable here is 1) esp resetting default pswrd bcoz that is easier to guess







