# HW4-510
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
Store the hwplaybook.yml file in the Jenkins-Ansible directory and just run the following command:  
```sudo ansible-playbook hwplaybook.yml -i inventory```  
Note: The inventory file is already present in the Jenkins-Ansible repository which uses localhost as the ansible connection.

## Screencast
Here's the [link](https://drive.google.com/open?id=1WWMDQj7E831E5KixyTOwEm2f5rXsXtBE) to the screencast.

## Concepts
+ ### Explain continuous integration. How is it used on a project?  
  Continuous Integration:  
Continuous integration is a software development practice wherein there is a central repository to which the developers commit their code frequently and these changes would then be merged. After merging, the code is automatically built and tested to check if there are any errors. This process is done several times a day depending on the commit frequency of the developers. This is used to automate the process of integrating the changes in code made by the developers working on a project. This practice encourages the developers to commit small changes more frequently and not committing a large change at once causing more errors and also it is difficult to identify the cause of the error.

  Use of continuous integration in a project:  
Continuous integration contributes a lot to the success of a project. The use of continuous integration is as follows:  
Consider a scenario where a project is worked on by a team of developers. One of the developers makes some changes to the code and these changes are committed and pushed to the shared repository.   
The newly pushed changes are detected by the continuous integration server and the project along with these changes is built. This is tested using automated tests to check if the newly added changes cause any problems.  
If any of the tests fail, then the developers are informed about it so that they can work on fixing the problem right away.  
This process is repeated until the project is successfully completed.  

+ ### Why should developers use configuration management tools to manage their software programs? What can go wrong if they don't?  
  Configuration management tools are used by developers to maintain the development environment consistent throughout all the endpoints and document any changes made to it. Configuration management makes sure that a system performs the way it is planned.  
Some of the benefits of using Configuration management tools in a project are:  
It is easier to implement any new system requirements as the management of changes is taken care of by these tools.  
CM tools make it easier to work on a project in a large team as these tools update all of the changes throughout the infrastructure. This increases collaboration and significantly increases productivity and efficiency.  
Configuration Management tools support most of the tools used for version control.  
CM tools run regular checks to ensure that the system is in the desired state and prevents configuration drifts.  
If a service outage happens, it is easier and quicker to recover and bring the service back up as all the requirements and changes are documented using the CM tools.  

  Some of the issues that occur when configuration management tools are not used are:  
When a requirement changes, it might take a lot of time to implement that change in all the systems manually. Moreover, the difficult task is to determine which component of the system should be updated.  
Without CM tools, if the system requirements are not communicated with all the developers, then while merging and building the software, it might fail due to requirement inconsistencies.  
There might be frequent system outages due to modifying certain components of the system without updating it throughout the infrastructure.  
The productivity of the team might be reduced significantly due to manually updating the changes and solving failed builds.
