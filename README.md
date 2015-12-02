# Deployment for testserv

### Note that this will only work on OS X or a Linux Distro with Python 2.x installed

This guide assumes that the servers to be deployed to have sshd set up and that you also
have ssh keys set up for testuser.
testuser will need sudo permissions on the server.
This also assumes installation on Ubuntu server 14.04 LTS or later

The easiest way to install Ansible is using pip
```
sudo pip install ansible
```


Modify the "hosts" file so that [webserver] contains the domain names (or ip addresses) of the
servers we're going to deploy on.
Copy the "hosts" file to /etc/ansible/hosts on your local machine if you don't have it already
```
sudo mv hosts /etc/ansible/hosts
```


To use the deployment script run:
```
ansible-playbook deploy.yml --ask-sudo-pass
```
You'll need to enter the user password for the testuser
