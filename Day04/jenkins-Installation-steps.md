# How to install jenkins in azure VM:
 - in Azure Go to VM then copy the IP address, then go for **gitbash** or **git**

# Install Jenkins.
- Pre-Requisites:
    - Java (JDK)
# Run the below commands to install Java and Jenkins
**Install Java**
### Run the below commands to install Java and Jenkins

Install Java

```
sudo apt update
sudo apt install openjdk-17-jre
```

Verify Java is Installed

```
java -version
```

Now, you can proceed with installing Jenkins

```
curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins
```

# **Note: ** By default, Jenkins will not be accessible to the external world due to the inbound traffic restriction by AZure. Open port 8080 in the inbound traffic rules as show below.
#** Add/Modify a Network Security Group (NSG)
In the Azure Portal, go to Virtual Machines.
- Select your VM.
- In the left pane, click Networking.
- Under Network Interface, click the NIC name.
- Under Settings, click Network security group.

# ✅ Configure Inbound Security Rules
- Click on your NSG (Network Security Group).
- Under Settings, click Inbound security rules.
- Click + Add to add a rule.
<img width="578" alt="image" src="https://github.com/user-attachments/assets/9eec5348-0a0d-4cef-b896-683f17167954" />

# Source	Any or IP Addresses (safer)
- Source port ->	*
- Destination ->	Any
- Destination port ->	present 8080 (for jenkins) 
- Protocol	-> TCP
- Action	-> Allow
- Priority ->	100 (lower = higher priority)
- Name	-> Allow-SSH or Allow-RDP
### Login to Jenkins using URL:
http://:8080 [You can get the ec2-instance-public-ip-address from your azure VM console page]

Note: If you are not interested in allowing All Traffic to your vm 1. Delete the inbound traffic rule for your VM 2. Edit the inbound traffic rule to only allow custom TCP port 8080
After you login to Jenkins, 
      - Run the command to copy the Jenkins Admin Password - `sudo cat /var/lib/jenkins/secrets/initialAdminPassword`
      - Enter the Administrator password
      
<img width="1291" alt="Screenshot 2023-02-01 at 10 56 25 AM" src="https://user-images.githubusercontent.com/43399466/215959008-3ebca431-1f14-4d81-9f12-6bb232bfbee3.png">

### Click on Install suggested plugins

<img width="1291" alt="Screenshot 2023-02-01 at 10 58 40 AM" src="https://user-images.githubusercontent.com/43399466/215959294-047eadef-7e64-4795-bd3b-b1efb0375988.png">

Wait for the Jenkins to Install suggested plugins

<img width="1291" alt="Screenshot 2023-02-01 at 10 59 31 AM" src="https://user-images.githubusercontent.com/43399466/215959398-344b5721-28ec-47a5-8908-b698e435608d.png">

Create First Admin User or Skip the step [If you want to use this Jenkins instance for future use-cases as well, better to create admin user]

<img width="990" alt="Screenshot 2023-02-01 at 11 02 09 AM" src="https://user-images.githubusercontent.com/43399466/215959757-403246c8-e739-4103-9265-6bdab418013e.png">

Jenkins Installation is Successful. You can now starting using the Jenkins 

<img width="990" alt="Screenshot 2023-02-01 at 11 14 13 AM" src="https://user-images.githubusercontent.com/43399466/215961440-3f13f82b-61a2-4117-88bc-0da265a67fa7.png">

## Install the Docker Pipeline plugin in Jenkins:

   - Log in to Jenkins.
   - Go to Manage Jenkins > Manage Plugins.
   - In the Available tab, search for "Docker Pipeline".
   - Select the plugin and click the Install button.
   - Restart Jenkins after the plugin is installed.
   
<img width="1392" alt="Screenshot 2023-02-01 at 12 17 02 PM" src="https://user-images.githubusercontent.com/43399466/215973898-7c366525-15db-4876-bd71-49522ecb267d.png">

Wait for the Jenkins to be restarted.


## Docker Slave Configuration

Run the below command to Install Docker

```
sudo apt update
sudo apt install docker.io
```
 
### Grant Jenkins user and Ubuntu user permission to docker deamon.

```
sudo su - 
usermod -aG docker jenkins
usermod -aG docker ubuntu
systemctl restart docker
```

Once you are done with the above steps, it is better to restart Jenkins.
```
http://<VM-public-ip>:8080/restart
```
The docker agent configuration is now successful.


