## Domain Name System

- a hierarchical system that translates human-readable domain names (like www.example.com) into machine-readable IP addresses (like 192.0.2.1).

- DNS simplifies navigation on the internet by allowing users to access websites using easy-to-remember names instead of numeric IP addresses which is essential for navigating websites and services.

## DNS components

1. Nameservers

loads DNS settings and configurations and respond to queries about domain names 

Two types:

    - authoritative: holds the actual DNS records for a specific domain so can provide answers to queries about domains it is authoritative for, such as A records, MX records, and CNAME records.
    - recursive (DNS resolver): this server takes on the responsibility of querying other DNS servers to resolve a domain name

>- DNS resolver: When a user queries a domain, the recursive nameserver will first check its cache. If it doesn’t have the answer, it will recursively query other nameservers, including root and TLD nameservers, until it finds the authoritative nameserver for the domain.
Once it receives the answer, it caches the result for future queries.


2. Zone files
     - stored inside nameservers
     - store infromation about how to get to the domain
     - stores DNS information in an organised and readable format

<img width="655" alt="Screenshot 2024-09-30 at 15 11 17" src="https://github.com/user-attachments/assets/87f23b91-1d0b-41f3-9e13-7811ab92deb6">

## DNS records

- a zone file is comprised of multiple resource records and each record contains specific information about hosts, nameservers and other resources
