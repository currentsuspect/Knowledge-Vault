---
tags:
  - networking
  - IP_addresses
  - security
  - internet_basics
  - networking_fundamentals
aliases:
  - IP Address
  - Internet Protocol
  - Networking Basics
cssclasses:
  - pen-blue
---
### 1. **Understanding IP Addresses**

An **IP (Internet Protocol) address** is a unique identifier assigned to each device connected to a network. Think of it as a "home address" for devices that helps them find and communicate with each other.

- **[[Is There a Unique Identifier for Everyone Online?]]**
#### **IPv4 vs. IPv6**

- **IPv4 (Internet Protocol version 4):**
  - **Format:** 32-bit numeric address written as four decimal numbers separated by dots (e.g., `192.168.1.1`).
  - **Range:** Each decimal number can range from 0 to 255.
  - **Total Addresses:** Around 4.3 billion (2^32).
  - **Example:** `192.168.1.1`, `172.16.0.1`.
  - **Use:** IPv4 is the most widely used protocol. It has been around since the early days of the internet.

- **IPv6 (Internet Protocol version 6):**
  - **Format:** 128-bit alphanumeric address, written in hexadecimal and separated by colons (e.g., `2001:0db8:85a3:0000:0000:8a2e:0370:7334`).
  - **Range:** Uses 16-bit blocks separated by colons (`:`), allowing for far more addresses.
  - **Total Addresses:** Approximately 340 undecillion (2^128), which is a massive increase over IPv4.
  - **Example:** `2001:0db8:85a3:0000:0000:8a2e:0370:7334`.
  - **Use:** IPv6 was developed to address the shortage of IPv4 addresses and is slowly being adopted worldwide.

#### **Key Differences:**
- **Address Space:** IPv6 provides a vastly larger address space than IPv4.
- **Security:** IPv6 has built-in IPsec (Internet Protocol Security) support for encrypted communication.
- **Configuration:** IPv6 supports auto-configuration (plug and play), while IPv4 may require manual or DHCP-based configuration.
- **Performance:** IPv6 eliminates the need for Network Address Translation (NAT), potentially improving performance by allowing direct end-to-end communication.

### 2. **Public vs. Private IP Addresses**

#### **Public IP Addresses:**
- **Definition:** Public IPs are globally unique and can be accessed over the internet. They are assigned by Internet Service Providers (ISPs) to network devices like routers.
- **Purpose:** Used for direct communication between different networks (e.g., a website server or any internet-facing service).
- **Example Range (IPv4):** 
  - `1.0.0.0` to `126.255.255.255` (Class A)
  - `128.0.0.0` to `191.255.255.255` (Class B)
  - `192.0.0.0` to `223.255.255.255` (Class C)

#### **Private IP Addresses:**
- **Definition:** Private IPs are used within a local network (LAN) and are not routable on the internet. Devices within a private network can communicate with each other but require a router with NAT to communicate outside the local network.
- **Purpose:** Provides IP addresses for internal use without using up the limited public IP address space.
- **Example Range (IPv4):**
  - **Class A:** `10.0.0.0` to `10.255.255.255`
  - **Class B:** `172.16.0.0` to `172.31.255.255`
  - **Class C:** `192.168.0.0` to `192.168.255.255`

#### **NAT (Network Address Translation):**
- **Role:** Translates private IP addresses to a public IP address, allowing devices on a local network to access the internet.
- **Why It’s Needed:** Since private IP addresses aren’t routable on the internet, NAT is necessary for any device on a private network to communicate with devices on the internet.

### 3. **Subnetting Basics**

#### **What is Subnetting?**
**Subnetting** is dividing a larger network into smaller, more manageable subnetworks (subnets). This allows for better control, efficiency, and security within the network.

#### **Why is Subnetting Important?**
- **Improves Network Performance:** By breaking down a large network into smaller subnets, network traffic is reduced on each subnet, minimizing congestion and improving performance.
- **Enhances Security:** Subnets can be isolated from each other, limiting the impact of security breaches.
- **Optimizes IP Address Use:** Efficiently allocates IP addresses to different parts of a network, avoiding wastage.

#### **How Subnetting Works:**
Subnetting involves modifying the subnet mask of an IP address to divide it into multiple smaller networks.

- **Subnet Mask:** A 32-bit number used in IPv4 to differentiate the network and host portions of an IP address. 
  - Example: `255.255.255.0` is a common subnet mask.
- **CIDR Notation:** Represents an IP address with its associated routing prefix. For example, `192.168.1.0/24`.
  - The `/24` tells us that the first 24 bits are the network part, leaving the last 8 bits for host addresses within that network.

#### **Example:**
- **IP Address:** `192.168.1.0/24` 
  - **Subnet Mask:** `255.255.255.0` 
  - **Network Portion:** The first 24 bits (`192.168.1`) define the network, and the remaining 8 bits define the host portion. 
  - **Hosts:** This subnet can have 256 IP addresses (`2^8`), but only 254 usable addresses because two addresses are reserved: one for the network (`192.168.1.0`) and one for the broadcast (`192.168.1.255`).

### 4. **How IP Addresses Are Used in Networking**

IP addresses are essential for routing data between devices. Here’s how they’re commonly used:

- **Host Identification:** Each device in a network must have a unique IP address to be identified and communicate.
- **Routing:** Routers use IP addresses to determine where to send packets of data. This process involves examining the destination IP address, comparing it with routing tables, and deciding the best path.
- **Security Policies:** Firewalls and other security devices use IP addresses to enforce policies like allowing or blocking traffic to certain destinations.

### **Hands-On Practice Tasks:**

1. **Research and Write:** What is the difference between public and private IP addresses? Why do we use NAT? Write a summary in your own words.
2. **Install `ipcalc` (IP Calculator):** Use it to calculate subnets and understand CIDR notation. For example, try `ipcalc 192.168.1.0/24` and analyze the output.
3. **Practice Subnetting:** Take a few IP addresses and practice converting them to binary to understand the difference between the network and host portions of the address.
4. **Experiment with `ping` and `ifconfig`:** Use `ping` to test connectivity and `ifconfig` (or `ip addr` on Linux) to view and understand your network configuration.

### Questions to Test Understanding:

1. **How do IPv4 and IPv6 differ in terms of address format and purpose?**
2. **What does the subnet mask `255.255.255.0` represent in CIDR notation?**
3. **Why might an organization need to use both public and private IP addresses?**

Let me know once you've gone through these tasks or if you need clarification on any point! We’ll take it from there to more complex networking scenarios and tools.