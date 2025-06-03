# Step 1: Sign in to Azure Portal
Open your web browser and navigate to the Azure Portal.
Enter your Microsoft account credentials to sign in. If you don’t have an account, you can create a free one.
# Step 2: Create a Virtual Machine
Once logged in, click on the “Create a resource” button located in the top left corner.
<img width="483" alt="image" src="https://github.com/user-attachments/assets/9952db56-c947-498b-80f5-14c97cf20db8" />

2. Go to Virtual Machine and Click on the “Create” button to start configuring your new Windows 11 VM.
 <img width="521" alt="image" src="https://github.com/user-attachments/assets/b75a553c-3efc-4433-97fe-45bc2c71c113" />


# Step 3: Basic Configuration
Now, you need to fill in the basic settings for your virtual machine.

- **Subscription:** Select your Azure subscription. e.g Azure subscription 1
- **Resource Group:** You can either select an existing resource group or create a new one by clicking on “Create new” .
- **Virtual Machine Name:** Enter a name for your VM (e.g., “my-vm”).
- **Region:** Choose the appropriate region where you want your VM to be hosted.
- **Availability Options:** Leave the default unless you have specific needs for redundancy.
![image](https://github.com/user-attachments/assets/0ce04963-ed59-4cb9-b11c-5ec971518f83)

# Step 4: Choose an Image
Under the Image section, select: See all Images to see the Windows 11 image. You can find it in the “Windows” category or type in the search box.
![image](https://github.com/user-attachments/assets/6f8f81f1-265c-4871-afa0-e6ad210145c6)

2. If applicable, select between the available Windows 11 Image (Standard, Pro, etc.) according to your requirements.
![image](https://github.com/user-attachments/assets/3723cce0-39eb-4ee1-bf3c-5795f1df6862)


# Step 5: Configure Size
For Size. Click on “See all Sizes” to select the appropriate size for your VM based on your expected workload.
![image](https://github.com/user-attachments/assets/a8dd51d7-1c9b-4f82-94ad-f74b0304642d)

Choose a VM size that fits your needs (CPU, RAM). Confirm the choice by clicking on “Select”.

# Step 6: Configure Administrator Account
- Create an administrator account for your VM:
- **Username:** Choose a username. eg azureuser
- **Password:** Set a strong password and confirm it.
![image](https://github.com/user-attachments/assets/ee97aa6d-0754-4a9c-b952-c01db240403e)

# Step 7: Network Configuration
For the Inbound port rules: Select Allow selected port and ensure port RDP 3389 is selected. For a Linux VM, Port 22 is selected instead.
![image](https://github.com/user-attachments/assets/4ad24264-b9d4-4bff-95de-b91a7e1c43b0)

# Step 8: Review and Create
After completing all configurations, click “I confirm” then Click on the “Review + create” button at the bottom.
![image](https://github.com/user-attachments/assets/329b5d57-ef04-4e91-8398-1e285aec50cc)
Azure will validate all your configurations. If everything is correct, you will see a validation passed message.
Click on the “Create” button. Azure will start deploying your virtual machine.
![image](https://github.com/user-attachments/assets/538ce6c1-f94d-4b45-9a45-0830d8afc0b3)

# Step 9: Access Your Windows 11 Virtual Machine
Once the deployment is complete, navigate to the “Virtual machines” section in the Azure portal.
![image](https://github.com/user-attachments/assets/7ca6a085-e6c6-4687-9f89-4703e200474c)

Find your newly created Windows 11 VM and click copy the Public IP Address.
Click on the “Connect” button and select “RDP” to download the RDP file.
Open the RDP file and connect to your VM using the credentials you created.
![image](https://github.com/user-attachments/assets/5d7e029c-ad58-48f7-8faa-a324c8cdb7cb)

4. Input your password... It will bring other prompts…Connect, Ok, Yes…for which you only click in the affirmative and wait till it gets to the windows 11 desktop.
![image](https://github.com/user-attachments/assets/27ee0803-a9d3-45e5-80d5-fbdfd4c07a0e)


# Conclusion
You have successfully set up a Windows 11 Virtual Machine on the Azure portal. You can now use this VM for testing, development, or any other tasks you need. Azure provides a powerful cloud computing setup that can accommodate various workloads. Remember to manage your resources appropriately to avoid unexpected charges.

**Note:** Ensure you delete these resources once you’re through with it as it has a cost implication that comes in once a month if left unused
