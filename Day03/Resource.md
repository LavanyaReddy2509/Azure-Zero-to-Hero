# Azure Resources

A **resource** in Azure is a single instance of a service—such as a virtual machine, database, web app, storage account, or network.

Azure resources are the building blocks of your cloud infrastructure in Microsoft Azure. These resources can be virtual machines, databases, storage accounts, or any other service offered by Azure. Each resource is a manageable item in Azure, and they are provisioned and managed individually.

# 🔹 Examples of Azure Resources:

| Resource Type |	Azure Service Example |
| :-------------| :---------------------|
| Compute |	Azure Virtual Machine (VM) |
| Database	| Azure SQL Database |
| Storage |	Azure Blob Storage |
| Networking	| Azure Virtual Network (VNet) |
| Web	| Azure App Service |
| AI/ML	| Azure Cognitive Services |
| Security |	Azure Key Vault |

# Resource Groups in Azure

A Resource Group is a logical grouping of related Azure resources like virtual machines, databases, web apps, storage accounts, etc., that share the same lifecycle.

# 🎯 Benefits of Resource Groups
- Easier organization of resources
- Simplifies deployment and deletion
- Centralized monitoring, security, and billing
- Supports tagging for cost and resource tracking

# ⚠️ Important Notes
- Resources in a group can be in different regions
- A resource can only belong to one resource group at a time
- You can move resources between groups (with some restrictions)

#  🛠️ Creating a Resource Group (Portal & CLI)
# 🌀 Azure Portal:
- Go to "Resource groups"
- Click "Create"
- Choose:
  - Subscription
  - Resource Group name
  - Region

- Click "Review + create"

  # 💻 Azure CLI:

- az group create --name WebApp-RG --location eastus

# Key Points about Resource Groups:
- **Lifecycle Management:** Resources within a group can be managed collectively, making it easy to handle deployments, updates, and deletions.
- **Resource Organization:** Grouping resources based on projects, environments, or applications helps keep your Azure environment well-organized.
- **Role-Based Access Control (RBAC):** Permissions and access control are applied at the resource group level, allowing you to manage who can access and modify resources within a group.
# Azure Resource Manager (ARM) Overview
- **Azure Resource Manager (ARM)** is the deployment and management service for Azure. It acts as the control plane that lets you create, update, delete, and manage Azure resources in a consistent and organized way.It provides a consistent management layer that enables you to deploy resources with declarative templates. ARM templates describe the resources you need and their configurations, allowing you to deploy and update resources in a predictable manner.

# Key Features of Azure Resource Manager:
- **Template-Based Deployment:** ARM uses JSON templates to define the infrastructure and configuration of your Azure resources. This enables repeatable and consistent deployments.
- **Dependency Management:** ARM automatically handles dependencies between resources, ensuring they are deployed in the correct order.
- **Rollback and Roll-forward:** In case of deployment failures, ARM can automatically roll back changes to maintain the desired state, or roll forward to the last known good state.
- **Tagging and Categorization:** You can use tags to label and categorize resources, making it easier to manage and organize your Azure environment.

- **Note:** Understanding Azure resources, resource groups, and Azure Resource Manager is fundamental to effectively utilize and manage your resources in the Azure cloud.
  
