#  Ansible playbook for installing and configuring Docker and nginx packages on Ubuntu18.04
This project is for configuring a local server using ansible. Usage is for Ubuntu 18.04.
## Getting Started
To deploy the project, you need to have the ansible and git packages installed on your machine.
### Installing Ansible and Git on Ubuntu  
    sudo apt update
    sudo apt install software-properties-common
    sudo apt-add-repository --yes --update ppa:ansible/ansible
    sudo apt install ansible git
### Deploy project
    git clone https://github.com/efgen42/lab1_2gis.git
Go to the project directory and edit the `hosts` file, specifying the value of the variable `ansible_sudo_pass` as the password for your user with sudo rights.
### Run
To run the playbook, use `ansible-playbook up.yml`.
