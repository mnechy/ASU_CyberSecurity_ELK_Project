## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

**Note**: The following image link needs to be updated. Replace `diagram_filename.png` with the name of your diagram image file.  

![TODO: Update the path with the name of your diagram] /Users/Matt/Desktop/Project_1/Matthew_Nechy_Project_1.png

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the playbook file may be used to install only certain pieces of it, such as Filebeat.

  - _Enter the playbook file._
    - /etc/ansible/install-elk.yml

This document contains the following details:
- Description of the Topology
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly secure, in addition to restricting traffic to the network.
-What aspect of security do load balancers protect? What is the advantage of a jump box?_
    - The Load Balancer protects against Distibuted Denial-Of-Servvice attacks by shifting the the attack traffic
    - The Jump Box is the host device that can be accessed securely from the internet.  Once connected, the user can "jump" around the network(s) and devices to perform administrative tasks.

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the logs and system traffic.
- What does Filebeat watch for?_
    - Filebeat monitors system log files and/or specified locations for changes made to the system, then forward them to the user specified area for indexing
- What does Metricbeat record?_
    - Metricbeat records system metrics and statistics, and ships them to the user specfied location

The configuration details of each machine may be found below.

| Name     | Function   | IP Address                | Operating System |
|----------|------------|---------------------------|------------------|
| Jump Box | Gateway    | 10.0.0.8 / 104.45.223.215 | Linux            |
| Web-1    | Web Server | 10.0.0.7                  | Linux            |
| Web-2    | Web Server | 10.0.0.6                  | Linux            |
| ELK      | ELK Server | 10.1.0.4 / 157.55.84.167  | Linux            |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the Jump Box machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- Add whitelisted IP addresses_
    -My personal home device Public IP

Machines within the network can only be accessed by the Jump Box via SSH.
- Which machine did you allow to access your ELK VM? What was its IP address?_   
    - The Jump Bov Virtual Machine with a VNet IP of 10.0.0.8

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses      |
|----------|---------------------|---------------------------|
| Jump Box | No                  | Home Public IP            |
| Web-1    | No                  | 10.0.0.8                  |
| Web-2    | No                  | 10.0.0.8                  |
| ELK      | No                  | 10.0.0.8 / Home Public IP |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- What is the main advantage of automating configuration with Ansible?
    - The main advantage of Ansible is that it allows the IT administrators to automate daily tasks, allowing them to focus on other important tasks.

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- ...
- ...

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

**Note**: The following image link needs to be updated. Replace `docker_ps_output.png` with the name of your screenshot image file.  


![TODO: Update the path with the name of your screenshot of docker ps output](Images/docker_ps_output.png)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- _TODO: List the IP addresses of the machines you are monitoring_

We have installed the following Beats on these machines:
- _TODO: Specify which Beats you successfully installed_

These Beats allow us to collect the following information from each machine:
- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., `Winlogbeat` collects Windows logs, which we use to track user logon events, etc._

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the _____ file to _____.
- Update the _____ file to include...
- Run the playbook, and navigate to ____ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on?_
- _Which URL do you navigate to in order to check that the ELK server is running?

_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._
