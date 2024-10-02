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

- components of resource records: TTL, Class, Type, Data

<img width="655" alt="Screenshot 2024-09-30 at 15 36 23" src="https://github.com/user-attachments/assets/7c7b745f-5d44-4b75-b9ea-78460ae3b81b">

## DNS records

<img width="660" alt="Screenshot 2024-09-30 at 15 37 28" src="https://github.com/user-attachments/assets/75b7490b-fa4f-47a2-93e9-fa506f53dce4">

A records are the most common type of DNS record and is essential for direccting traffic to the correct IP address

<img width="512" alt="Screenshot 2024-09-30 at 15 39 19" src="https://github.com/user-attachments/assets/8b5aa5f1-860e-4482-9268-f6dc86153d24">
<img width="512" alt="Screenshot 2024-09-30 at 15 40 09" src="https://github.com/user-attachments/assets/10bb60de-5960-4235-ab22-1cdc9ca8361f">
<img width="512" alt="Screenshot 2024-09-30 at 15 40 26" src="https://github.com/user-attachments/assets/856bdb16-1066-4db4-a12f-743a04ee077f">
<img width="512" alt="Screenshot 2024-09-30 at 15 41 04" src="https://github.com/user-attachments/assets/707ea050-4f65-4936-bbee-92742fa20161">


# How DNS Works

DNS translates human-readable domain names (e.g. `www.example.com`) into machine-readable IP addresses (like `192.0.2.1`). This process allows users to access websites easily without memorizing numerical addresses. 

## 1. DNS Hierarchy
DNS operates in a hierarchical structure:
- **Root Domain**: The top of the DNS hierarchy, represented by a dot (`.`).
- **Top-Level Domains (TLD)**: Includes domains like `.com`, `.org`, and `.net`.
- **Second-Level Domains**: Specific domain names, such as `example` in `example.com`.
- **Subdomains**: Additional divisions under a domain, like `www` in `www.example.com`.
  
<img width="590" alt="Screenshot 2024-09-30 at 15 53 34" src="https://github.com/user-attachments/assets/cd269ca4-5c91-4569-b129-93afe190d12d">

## 2. DNS Resolution Process

When you enter a domain name in your browser, the DNS resolution process involves several steps:

1. **DNS Query Initiation**:
   - You enter a URL (e.g., `www.example.com`) in your web browser.

2. **Querying the DNS Resolver**:
   - The request first goes to a **DNS resolver** (often provided by your ISP).
   - If the resolver has the IP address cached locally, it returns it immediately.

3. **Root Nameserver Query**:
   - If not cached, the resolver sends a query to a **root nameserver**.
   - The root nameserver responds with the address of the appropriate **TLD nameserver**.

4. **TLD Nameserver Query**:
   - The resolver queries the TLD nameserver, which knows the authoritative nameservers for the specific domain.
   - It responds with the address of the **authoritative nameserver** for `example.com`.

5. **Authoritative Nameserver Query**:
   - The resolver then queries the authoritative nameserver for `example.com`.
   - This nameserver contains the DNS records for the domain.

6. **Returning the IP Address**:
   - The authoritative nameserver responds with the IP address (e.g., `192.0.2.1`).
   - The resolver caches this response for future queries.

7. **Connecting to the Server**:
   - The resolver sends the IP address back to your device.
   - Your browser can now connect to the web server to retrieve the requested webpage.

## 3. Caching
DNS responses are cached at various levels:
- **Device Cache**: Your device caches responses for a specified duration (TTL - Time to Live).
- **Resolver Cache**: The DNS resolver caches responses to serve future requests quickly.
- **Nameserver Cache**: Intermediate nameservers cache responses to reduce lookup times.


## Debugging DNS issues

Two main troubleshooting tools

### 1. nslookup

- gives you the IP address associated with that domain

<img width="655" alt="Screenshot 2024-10-02 at 14 55 01" src="https://github.com/user-attachments/assets/239c559c-d632-4ba5-9de8-83b299b98a38">

#### The Output

<img width="655" alt="Screenshot 2024-10-02 at 16 49 40" src="https://github.com/user-attachments/assets/3b8997e7-34b7-4a97-a189-e5eeff1de07a">

### 2. dig

- more advanced and detailed than nslookup
- when you want to do DNS queiries
  
<img width="531" alt="Screenshot 2024-10-02 at 14 55 21" src="https://github.com/user-attachments/assets/0404433d-1fe4-464f-81f8-31c5c6139353">

#### The Output

<img width="655" alt="Screenshot 2024-10-02 at 16 51 17" src="https://github.com/user-attachments/assets/237c1c7d-1e2a-4dbc-a504-733b4ec20e07">
<img width="655" alt="Screenshot 2024-10-02 at 16 51 58" src="https://github.com/user-attachments/assets/ed11d80f-7f7f-40e9-958a-92ec0626e35a">

- you can also run `dig +short google.com` or `dig +short ns`
