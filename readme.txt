Pre-Requisites for the successful deployment:

1- Create 2 s3 buckets and add in the code: 
   prodwebserver/webserver
   prod-network/network
   

2- create ssh-keys needed for the instances:
   Command: ssh-keygen -t rsa -f project3


Ansible configuration:
Install ansible  sudo yum install ansible
Install boto3    sudo pip install boto3
Run the comand: sudo vim /etc/ansible/ansible.cfg
modify the cofige file
inventory      = /home/ec2-user/environment/Ansible/hosts.txt
ansible_user   = ec2-user
ansible_ssh_private_key = /home/ec2-user/environment/Ansible/FinalProject




Change the directory to the network from the root: cd environment/project/project/modules/aws_network 
1)Start with the network folder, we will deploy the network of the dev environment using:
tf init
tf plan
tf apply
2)Change the directory to the prod from the root: cd environment/project/project/project/prod/network. 
tf init
tf plan
tf apply
3)Change the directory in the prod from the root: cd environment/project/project/project/prod/webserver. 
tf init
tf plan
tf apply
4) After deploying everything, we will go to the EC2 in the console and look for bastion-azone-linux and enter it.
5) Copy the public ip
7) Open a web page and type hppt://ip-address
   you can do the same for the other webserves


Destroy webservers

Destroy network  

