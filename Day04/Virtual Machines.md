## 💻 What Are Virtual Machines (VMs) in Azure?
- A **Virtual Machine (VM)** is a **software-based computer** that runs on a physical machine but behaves like a separate physical device. It has its own ***CPU, memory, storage, and operating system,*** just like a real computer.
- **Azure Virtual Machines** (VMs) are **on-demand, scalable computing resources** offered by Microsoft Azure. They provide **Infrastructure as a Service (IaaS)**, enabling you to run **Windows or Linux operating** systems in the cloud—just like on a physical server, but virtualized.

# ✅ Key Features of Azure Virtual Machines
| Feature| Description |
| :------------| :--------------- |
| Operating Systems |	Supports both Windows and Linux |
| Scalability	Easily | scale up/down based on demand using VM Scale Sets |
| Availability Options	| Use Availability Sets or Zones for high availability and fault tolerance |
| Custom Images |	Create and deploy your own custom OS images |
| Automation |	Automate VM creation with ARM Templates, Bicep, or Terraform |
| Integration |	Connects with Azure services like Load Balancer, Backup, Monitor |

# 🛠️ Common Use Cases
- Hosting web servers and application backends
- Running databases (SQL, MySQL, PostgreSQL, etc.)
- Development and testing environments
- Legacy application support
- Disaster recovery and failover infrastructure

# 🧱 VM Components
| Component	| Description |
| :--------------- | :---------------- |
| VM Size	| Determines CPU, RAM, and disk capacity (e.g., Standard_B2s, D4s_v3) |
| OS Disk |	Managed disk that holds the OS and boot files |
| Data Disk |	Optional disks attached to store additional data |
| NIC	| Network interface card connects the VM to a virtual network |
| Public IP	| Optional IP for external access |
| NSG (Firewall)	| Network Security Group rules to allow/deny traffic |

# 🔐 Security Features
- Azure Defender for VMs (threat protection)
- Disk Encryption using Azure-managed keys or customer keys
- Just-in-Time VM Access to reduce attack surface
- RBAC and Privileged Identity Management (PIM) for access control

# ⚙️ Creating an Azure VM (Portal Steps)
- Go to **Azure Portal**
- Click **"Create a resource" > "Virtual Machine"** 
- Choose:
   - Subscription
   - Resource Group
   - Region
   - Image (OS)
   - Size (compute power)
   - Authentication type (password or SSH)
   - Configure disk, networking, monitoring
-Click "Review + Create" and then "Create"
