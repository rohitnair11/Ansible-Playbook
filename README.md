# Ansible-Playbook
This ansible playbook can automate the following operations:  
Install node  
Install Forever  
Pull a git repository  
Install dependencies  
Run the node js app present in the cloned repository  
Check if bash, openssl, openssh-client, and openssh-server are running latest version  
Clear the contents of tmp folder  

To execute this playbook, first, you have to setup ansible.  

## Steps for running Ansible
Clone the below repository that contains the required files:       
```git clone https://github.com/CSC-510/Jenkins-Ansible.git```   
```cd Jenkins-Ansible```  

Run the follwing command to create a virtual machine and install ansible on it using baker:    
```baker bake```  

Run the follwing command to connect to the virtual machine:  
```baker ssh```  
```cd /Jenkins-Ansible```  
Now you are connected to the VM and can start using ansible.  

Reference: https://github.com/CSC-510/Jenkins-Ansible  
## Steps for running the playbook
Store the playbook.yml file in the Jenkins-Ansible directory and just run the following command:  
```sudo ansible-playbook playbook.yml -i inventory```  
Note: The inventory file is already present in the Jenkins-Ansible repository which uses localhost as the ansible connection.
