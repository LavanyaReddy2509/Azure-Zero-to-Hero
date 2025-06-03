# Step 1: Sign in to Azure Portal
Open your web browser and navigate to the Azure Portal.
Enter your Microsoft account credentials to sign in. If you don’t have an account, you can create a free one.
# Step 2: Create a Virtual Machine
Once logged in, click on the “Create a resource” button located in the top left corner.

2. Go to Virtual Machine and Click on the “Create” button to start configuring your new Windows 11 VM.


# Step 3: Basic Configuration
Now, you need to fill in the basic settings for your virtual machine.

Subscription: Select your Azure subscription. e.g Azure subscription 1
Resource Group: You can either select an existing resource group or create a new one by clicking on “Create new” .
Virtual Machine Name: Enter a name for your VM (e.g., “my-vm”).
Region: Choose the appropriate region where you want your VM to be hosted.
Availability Options: Leave the default unless you have specific needs for redundancy.

# Step 4: Choose an Image
Under the Image section, select: See all Images to see the Windows 11 image. You can find it in the “Windows” category or type in the search box.

2. If applicable, select between the available Windows 11 Image (Standard, Pro, etc.) according to your requirements.


# Step 5: Configure Size
For Size. Click on “See all Sizes” to select the appropriate size for your VM based on your expected workload.

Choose a VM size that fits your needs (CPU, RAM). Confirm the choice by clicking on “Select”.

# Step 6: Configure Administrator Account
Create an administrator account for your VM:
Username: Choose a username. eg azureuser
Password: Set a strong password and confirm it.

# Step 7: Network Configuration
For the Inbound port rules: Select Allow selected port and ensure port RDP 3389 is selected. For a Linux VM, Port 22 is selected instead.

# Step 8: Review and Create
After completing all configurations, click “I confirm” then Click on the “Review + create” button at the bottom.

Azure will validate all your configurations. If everything is correct, you will see a validation passed message.
Click on the “Create” button. Azure will start deploying your virtual machine.

# Step 9: Access Your Windows 11 Virtual Machine
Once the deployment is complete, navigate to the “Virtual machines” section in the Azure portal.

Find your newly created Windows 11 VM and click copy the Public IP Address.
Click on the “Connect” button and select “RDP” to download the RDP file.
Open the RDP file and connect to your VM using the credentials you created.

4. Input your password... It will bring other prompts…Connect, Ok, Yes…for which you only click in the affirmative and wait till it gets to the windows 11 desktop.


# Conclusion
You have successfully set up a Windows 11 Virtual Machine on the Azure portal. You can now use this VM for testing, development, or any other tasks you need. Azure provides a powerful cloud computing setup that can accommodate various workloads. Remember to manage your resources appropriately to avoid unexpected charges.

**Note:** Ensure you delete these resources once you’re through with it as it has a cost implication that comes in once a month if left unused
