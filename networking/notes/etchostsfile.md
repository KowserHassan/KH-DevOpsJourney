# What is a /etc/hosts File?

- It is a local file on your computer
- It maps domain names to IP addresses
- It takes precedence over DNS for specific entries
- Can override DNS settings for certain domains by providing alternative IP addresses


When searching for an IP address, your computer first checks the /etc/hosts file, it uses this IP address instead of querying the DNS server 

# Editing /etc/hosts File

- you need admin priviledges to edit this file

1. open the file with a text editor - `sudo vim /etc/hosts`
2.  Format: IP_address domain_name
