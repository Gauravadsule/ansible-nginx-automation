# ansible-nginx-automation
**Project Title :**
Automating Nginx installation and website Dployment with Ansible.

**Project Description :**
This project demonstrates how to use Ansible for automating the installation of Nginx on multiple servers and deploying a custom webpage. The setup consists of an Ansible control node managing multiple EC2 instances (managed nodes).

**Features :**
	•	Automates the installation of Nginx on target servers.
	•	Starts and enables the Nginx service.
	•	Deploys a custom index.html file to serve as the homepage.
	•	Reduces manual effort with a single playbook execution.

**Prerequisites :**
To run this project, ensure you have:
	•	AWS account with at least 2 EC2 instances (1 control node, 1 managed nodes).
	•	Ansible installed on the control node.
	•	SSH access configured between the control node and the managed nodes.

 **Project Setup**

**Step 1: Configure Inventory**

Add the IP addresses of the managed nodes to the Ansible hosts file:
[servers]
<IP_ADDRESS_1>

**Step 2: Secure SSH Access**
Transfer your private key from your local machine to the control node using: SCP command.

**Step 3: Run the Playbook**
Execute the Ansible playbook to install Nginx and deploy the website:

**Files in the Repository**
	•	playbook.yml: The Ansible playbook that installs Nginx, starts the service, and deploys the index.html file.
	•	index.html: A sample HTML file for the deployed website.

**How It Works**
	1.	The apt module in the playbook installs the latest version of Nginx.
	2.	The service module ensures Nginx is started and enabled to run on system boot.
	3.	The copy module deploys the index.html file to /var/www/html.

**Example Output**
Once the playbook is executed, you can access the deployed website using the public IP of any managed node:
http://<managed_node_ip>

