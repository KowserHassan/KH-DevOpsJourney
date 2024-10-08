### Subnetting

Subnetting is dividing one large network into smaller networks 
- this improves network management and efficiency

<img width="455" alt="Screenshot 2024-10-02 at 18 19 02" src="https://github.com/user-attachments/assets/2ff60fc1-c46e-4214-b013-dc97bad8cd12">

The address 192.168.1.0/24 represents a network in CIDR notation.

- 192.168.1.0 is the network address
- /24 indicates the subnet mask, which tells us how many bits are used for the network portion of the address
- /24: the first 24 bits (the first three octets: 192.168.1) are reserved for the network, while the remaining 8 bits (the last octet) are available for host addresses.

### NAT (Network Address Translation)

- Translates private IP addresses to a public IP
- Everything in you home network has thier own private IP addresses but when they go online, they all share 1 private IP address - this is facilitated by NAT
- W/O NAT, all your devices would need their own public IP address which is not practical because there are a limited number of public IPs

- facilitates communication between your internal  network and the internet
- <img width="493" alt="Screenshot 2024-10-08 at 16 14 19" src="https://github.com/user-attachments/assets/2ee71036-2e11-4f3b-ae1e-38f1e3f26db0">


#### How NAT works?



