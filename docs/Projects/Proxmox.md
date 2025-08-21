# What is Proxmox?

##### **Introduction**

Virtualization is a technology that allows you to create and run multiple "virtual" computers inside a single physical computer. Instead of needing multiple separate machines, virtualization lets you run multiple operating systems (like Windows, Linux, or macOS) on the same hardware at the same time. At its core, virtualization uses special software called a hypervisor to create and manage virtual machines (VMs). The hypervisor acts as a middleman between the physical hardware and the virtual machines, making sure each VM gets the resources (CPU, RAM, storage, etc.) it needs. ૮₍  ˶•⤙•˶ ₎ა

A Proxmox server is a powerful open-source [Type 1 hypervisor](https://www.techtarget.com/searchitoperations/tip/Whats-the-difference-between-Type-1-vs-Type-2-hypervisor) (also known as "bare-metal" hypervisor) that allows you to run multiple virtual machines (VMs) and containers on a single physical server. It combines two main technologies: KVM (Kernel-based Virtual Machine) for full virtualization and LXC (Linux Containers) for lightweight container-based virtualization. Proxmox is widely used for enterprise-level virtualization, home labs, and small to medium-sized businesses looking for an efficient and cost-effective way to manage virtualized workloads.

One of the awesome things about Proxmox is its ability to cluster (╯✧▽✧)╯. Clustering is the process of grouping multiple independent servers (or nodes) into a single logical unit. This allows you to manage them together as if they were a single entity, making tasks like resource allocation, failover, and load balancing much easier. In Proxmox, clustering involves connecting multiple Proxmox Virtual Environment (PVE) nodes together, enabling them to communicate and share resources. Proxmox uses its PVE Cluster feature to integrate and synchronize nodes into one unified management interface.

##### **Minimum Requirements:**
- **CPU:** 64-bit processor with virtualization support 
- **RAM:** 2 GB (absolute minimum; recommended is at least 8 GB)
- **Storage:** 16 GB+ boot drive (SSD recommended for performance)
- **Network:** 1 Gbps network adapter
- **OS:** Proxmox VE is installed as a bare-metal hypervisor (based on Debian Linux)

##### **Capabilities of Proxmox VE**
- Virtualization Options
- Web-Based Management Interface
- Storage Flexibility
- Networking Features
- High Availability and Clustering
- Backup and Disaster Recovery