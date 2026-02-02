- **Cloud computing** - digital services provided on the internet, instead of onsite
- Advantages of cloud computing:
	1. **Better storage & processing** for massive amounts of data
	2. **Accessibility** for any Internet-connected device
- **Cloud service provider** - provides IaaS, PaaS, and SaaS
	- **IaaS** - borrows network, storage, components
	- **PaaS** - borrows cloud-provided environments for app development
		- Ex. containers, databases, runtime, integration, etc.
		- Ex. Vercel, AWS
	- **SaaS** - file management
		- Software and data both reside online. No special software is needed.
	- **XaaS** - "anything as a service"
	- 
![[Pasted image 20260130174620.png]]
- **Virtualization** - allows multiple OSes on a single machine
	- **Physical server** - Hard drive/memory bank devoted to one group of users or one type of data
	- **Virtual server** - A "software-controlled region" of a physical server
		- i.e. a physical server can be divided into multiple virtual servers
	- **VMs** - different network interfaces, memory, storage, etc. on the same machine

### Types of Clouds
- **Public clouds** - for consumer use
	- Easy to scale
	- Under "multi-tenant architecture" (as many users are using one large cloud platform)
- **Private cloud** - for a single organization
	- Can be managed either by the org itself or the cloud service provider
	- Has different scalability requirements (expands only when it needs to)
- **Hybrid cloud** - public & private resources

![[Pasted image 20260130174216.png]]

- **Multicloud** - the use of more than one public cloud, usually either separate IaaS and SaaS, or multiple IaaS

### Other Terminology
- **Cloud** - can also be defined as the *Internet*
- **Cloud computing** - Internet-based computing
- **Clusters** - a collection of standalone computers that work as a single interconnected resource
- **Containers** - a "wrapper" for software in a single OS.
	- **IMPORTANT!** VMs simulate up to the hardware level, containers simulate only above the OS level
	- **Kubernetes** - open-source software for managing containers
- **Premises** - where the cloud data is stored
	- **Off-premises** - different location than the end users
	- **On-premises** - own company's data center
	- **Hybrid** - both, useful if usage comes on bursts. i.e., the company can use an on-premises cloud that scales to vendor's off-premises servers during peak times
	- An organization can have a private cloud either on premises or off premises.
- **Local** - on-premises private cloud
- **Dedicated** - off-premises private cloud
- **Public** - public cloud

### Did You Know?
- 2.5 quintillion bytes are added to the Internet everyday
- Examples of programming languages used for cloud:
	- Python
	- Perl
	- Ruby
	- Puppet
	- Chef
	- Ansible
	- Docker
	- VMware
- Other programming languages:
	- PHP
	- Java
	- .NET
- Major vendors' training
	- AWS
	- Azure
	- Google Cloud
	- IBM Cloud
	- Red Hat

### 