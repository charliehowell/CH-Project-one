# CH-Project-one

## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![TODO: Update the path with the name of your diagram](Images/diagram_filename.png)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the playbook (.yml) file may be used to install only certain pieces of it, such as Filebeat.
  
ELK PLAYBOOK
  
  root@8f4a0e3c149d:/etc/ansible/roles/elk.yml
  <img width="443" alt="elk install playbook" src="https://user-images.githubusercontent.com/73140949/110365649-4547cf00-8013-11eb-81e1-f2bf29f14ee7.png">

FILEBEAT PLAYBOOK

  root@8f4a0e3c149d:/etc/ansible/roles/filebeat-playbook.yml
  <img width="709" alt="filebeat playbook" src="https://user-images.githubusercontent.com/73140949/110365675-4bd64680-8013-11eb-8761-01b66d1b07fc.png">

METRICBEAT PLAYBOOK

  root@8f4a0e3c149d:/etc/ansible/roles/metricbeat-playbook.yml
<img width="706" alt="metricbeat playbook" src="https://user-images.githubusercontent.com/73140949/110365690-509afa80-8013-11eb-91bc-5d94122ad43f.png">


This document contains the following details:
- Description of the Topologu
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly responsive, in addition to restricting traffic to the network. They also protect against DDoS attacks by shifting attack traffic from the corporate server to a public cloud provider. 

A jump box is a secure computer that all admins first connect to before launching any administrative task or use as an origination point to connect to other servers or untrusted environments.

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the data and system logs. Filebeat monitors specified log files or locations while metricbeat collects and ships metrics and statistics to specified outputs.

The configuration details of each machine may be found below.


| Name     | Function | IP Address | Operating System |
|----------|----------|------------|------------------|
| Jump Box | Gateway  | 10.0.0.4   | Linux            |
| web-1    | server   | 10.0.0.5   | Linux            |
| web-2    | server   | 10.0.0.6   | Linux            |
| web-3    | server   | 10.0.0.7   | Linux            |
| Elk-vm   | server   | 10.1.0.4   | Linux            |
### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the jump box machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses: 73.79.65.86
- _TODO: Add whitelisted IP addresses_

73.79.65.86

Machines within the network can only be accessed by SSH.
I allowed my jump-box machine and its IP was 40.117.239.186


A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses         |
|----------|---------------------|------------------------------|
| Jump Box | no                  |  73.79.65.86                 |
| web-1    | no                  |   73.79.65.86                |
| web-2    | no                  |  73.79.65.86                 |
| web-3    | no                  | 73.79.65.86                  |
| elk-vm   | no                  | 73.79.65.86 & 40.117.239.186 |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- _TODO: What is the main advantage of automating configuration with Ansible?_

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- ...
- ...

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

<img width="902" alt="docker_ps_output" src="https://user-images.githubusercontent.com/73140949/110365483-192c4e00-8013-11eb-9f01-d4c996c6e237.png">


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
