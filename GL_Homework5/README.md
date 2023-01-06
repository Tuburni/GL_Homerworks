<p align="center">
      <img src="https://github.com/Tuburni/GL_Homerworks/blob/main/GL_Homework5/jpg/EC2%20servers.jpg">
</p>

<p align="">
   <img src="https://github.com/Tuburni/GL_Homerworks/blob/main/GL_Homework5/jpg/ansible-inventory%20--graph.jpg">
</p>

<p align="">
   <img src="https://github.com/Tuburni/GL_Homerworks/blob/main/GL_Homework5/jpg/ansible%20-i%20hosts%20all%20-m%20ping.jpg">
</p>

<p align="center">
   <img src="https://github.com/Tuburni/GL_Homerworks/blob/main/GL_Homework5/jpg/ansible-playbook%20playbook.yml.jpg">
</p>

## Distribute

- [roles](https://github.com/Tuburni/GL_Homerworks/tree/main/GL_Homework5/roles)
- [ansible.cfg](https://github.com/Tuburni/GL_Homerworks/blob/main/GL_Homework5/ansible.cfg)
- [hosts](https://github.com/Tuburni/GL_Homerworks/blob/main/GL_Homework5/hosts)
- [playbook.yml](https://github.com/Tuburni/GL_Homerworks/blob/main/GL_Homework5/playbook.yml)

## Instruction

Here is a detailed guide on how to complete the task described above: 
 
1. Create a inventory file with four groups: 

- First, create a new file called inventory in your controller machine. 
- In this file, define four groups: group1, group2, group3, and iaas. The iaas group should include children from group1 and group2. For example 


2. Create reusable roles for creating a file and fetching a Linux distro name: 

- In your controller machine, create a new directory called roles. 
- Within the roles directory, create a new directory called create_file. This will be the directory for the role that creates a file. 
- Within the create_file directory, create the following files and directories: 
 > tasks directory 
 > main.yml file within the tasks directory 
- In the main.yml file, add the following task to create a file called /etc/iaac with permissions 0500
- In the roles directory, create a new directory called fetch_distro. This will be the directory for the role that fetches the Linux distro name. 
- Within the fetch_distro directory, create the following files and directories: 
 1) tasks directory 
 2) main.yml file within the tasks directory 
 3) vars directory 
 4) main.yml file within the vars directory 

- In the main.yml file within the tasks directory, add the following task to define a variable called distro with the value of the Linux distro name

- In the main.yml file within the vars directory, add the following variable to define the distro_version variable with the value of the Linux distro version

3. Create a playbook for invoking the roles and printing the registered variables: 

- In your controller machine, create a new file called playbook.yml. 
- In this file, add the following content to specify 
 
- The roles to be invoked and the hosts on which they will be applied


## Developers

- [Borys Kondrashov](https://github.com/Tuburni)

## License