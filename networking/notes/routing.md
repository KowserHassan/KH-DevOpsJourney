# Routing

Routing is the process of directing data across networks to ensure it reaches its destination. Routers use **routing tables** to determine the best path for data packets based on destination IP addresses.

Routing ensures that data reaches its destination:
- efficiently
- quickly

therefore it is essential for internet functionality

## Key Concepts

| Term            | Explanation                                                                 |
|-----------------|-----------------------------------------------------------------------------|
| **Router**      | Device that forwards data between networks using routing tables.             |
| **Routing Table**| A set of rules in the router that dictate the next hop for a data packet.    |
| **Hop**         | A step from one router to another in the data's journey.                     |
| **IP Address**  | Unique address assigned to devices on a network, used to route data.         |

## How Routing works?

1. **Data Creation:** A device (like your computer) sends data to a specific destination IP address, such as when you're visiting a website.
2. **Router Decision:** Your device forwards the data packet to your local router (often your home router). The router reads the destination IP address, then checks its routing table to decide where to send the packet next.
3. **Forwarding to Next Hop:** Based on its routing table, the router forwards the packet to the next hop, which is another router closer to the destination.
4. **Routing Across Networks:** As the packet moves from one router to another, it travels across various networks (like your ISP's network, regional networks, etc.).
5. **Destination Network:** Eventually, the packet reaches a router that recognises the destination network (where the target device, such as a web server, is located).
6. **Final Delivery:** The final router forwards the packet to the correct device within the destination network, and the device processes the data.

## Example

If you type www.example.com into your browser:

1. The DNS system converts the domain into an IP address.
2. Your router forwards the packet containing the request to the next available router.
3. The packet moves through several routers (hops), each one checking its routing table to send it to the next closest network.
4. Eventually, the packet reaches the destination web server, and the server sends the response back using the reverse route.

## Why Routing Matters for DevOps?

1. Network performance optimisation - QUICK
2. Ensures reliable application delivery
3. Crucial for managing complex infrastructures 

## Static vs. Dynamic Routing

- **Static Routing**: When routes are manually configured by network administrators, used in simple stable networks.
  - simple but not scalable

>- Since this is a fixed map that has been set up for your data to follow, if the route changes, you have to change this manually.

- **Dynamic Routing**: Routers use algorithms and complex routing protocols to find the best path and automatically update routes. Very flexible and keeps data moving efficiently 
  - scalable and adaptable

## Common Routing Protocols

Routing protocols automate the process of determining the best route for data to travel across the network  
Enhance network efficiency as they find alternative paths quickly if one goes down  

- **Open Shortest Path First (OSPF)**: Uses link state information to make optimal routing decisions. it can quickly recalculate routes when there are changes in the network. known for fast convergence
- **Border Gateway Protocol (BGP)**: Routes data across the different autonomous systems i.e  large networks managed by single orgs. it uses a path vector mechansim that gets updated dynamically as topology changes. bgp allows network admins to define routing policies based on diff attributes giving greater control over how data flows
