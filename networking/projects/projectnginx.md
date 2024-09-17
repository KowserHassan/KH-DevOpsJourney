# The Task

1. **Create an EC2 instance with nginx hosted on it.**
2. **Create an A record on Cloudflare:**
   - **Name:** `nginx`
   - **Value:** EC2 IP address
3. **View the home nginx webpage at `nginx.kowserhassan.com`**

> **Background:** Nginx is a high-performance, open-source web server and reverse proxy used by many top websites worldwide. The purpose of this task is to set up a web server that you can access through my domain name. 


# Part 1: Create and configure EC2

### Step 1: Create an EC2 instance on AWS and connect

### Step 2: Install nginx on the EC2

- Install nginx using the package manager

  - `sudo apt install nginx` 

### Step 3: Configure the EC2 for nginx

#### 1. Set Up Access for HTTP

- Navigate to your **EC2 instance** summary on the Amazon AWS console.
- Click on the **Security** tab near the bottom of the page.
- Click on the **Security Group** to modify the instance's security settings.

#### 2. Edit Inbound Rules

- Click **Edit Inbound Rules** to modify access.
- Add an inbound rule for **HTTP** (TCP on port 80). The settings should be:
  
  - **Type**: HTTP
  - **Protocol**: TCP
  - **Port Range**: 80
  - **Source**: 0.0.0.0/0

#### 3. Set Up an Elastic IP Address

An **Elastic IP address** is a public IPv4 address reachable from the internet.

1. **Allocate an Elastic IP address** through the AWS console.
2. **Associate the Elastic IP** with your EC2 instance or network interface.

Refer to Amazon AWS documentation for detailed instructions:
- [Allocate an Elastic IP address](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-ip-addressing.html#vpc-eips)
- [Associate an Elastic IP address](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-ip-addressing.html#vpc-eip-associating)

Once complete, you can find your **public IP address** in the EC2 dashboard.

#### 4. Note the Elastic IP

- Keep a note of this **Elastic IP address**. 

#### 5. Now,  if you type the public IP address in a web browser you see...

---

<img width="568" alt="Screenshot 2024-09-16 at 20 50 09" src="https://github.com/user-attachments/assets/2b326c5a-aac6-4de8-9dfd-7a06e1ad9d0a">

# Part 2: Manage DNS for the domain through AWS Route 53 

> **Information:** Route 53 is a Domain Name System (DNS) service provided by AWS. It helps set up DNS records that map your domain name to the IP address of your EC2 instance, so when users type your domain name into their browser, Route 53 directs them to the IP address of your server where your nginx website is hosted.

1. Go to your AWS Route 53 Console.
2. Under DNS Management, click Hosted Zones.
3. Click Create Hosted Zone, then input your domain name and select Public Hosted Zone.

# Part 3:  Create an A record on Cloudflare

Register a domain with Cloudflare, follow these steps to point your domain to the EC2 instance:

1. Log in to **Cloudflare** and navigate to the **DNS** settings for your domain.
2. Click **Add Record**.
3. Set the following fields:
   - **Type**: A
   - **Name**: nginx
   - **IPv4 Address**: Enter the **Elastic IP address** of your EC2 instance.
   - **TTL**: Auto (default)
   - **Proxy Status**: Proxied
4. Click **Save** to create the A record.
5. Visit nginx.kowserhassan.com in the web browser 🎉

<img width="1379" alt="Screenshot 2024-09-17 at 01 02 16" src="https://github.com/user-attachments/assets/2399f0c0-97ce-423f-b079-bbb16af602c2">


# We've successfully completed the project! 🏆  

We have:  
✅ set up the server  
✅ configured DNS  
✅ verified everything works as expected 



