#  Ansible playbook for installing and configuring Docker and nginx packages on Ubuntu18.04
This project is for configuring a local server using ansible. Usage is for Ubuntu 18.04
## What do you get as a result of executing the up.yml playbook:
- Installed Nginx web server latest stable version
    - Support for SSL: generated self-signed opensl certificate, as well as private key and dx-key
    - The /etc/nginx/snippets directory contains the self-signed.conf files (contains the paths to the certificate and private key) and ssl-params.conf (contains additional security settings)
    - Config file /etc/nginx/nginx.conf changed to write nginx logs in json format
    - The configuration file of the virtual host /etc/nginx/sites-available/default is configured with the following requirements:
        - The server block contains settings for serving site content from the /var/www/html directory and supporting SSL requests
        - The location block is configured to redirect the request to $ scheme://www.google.com in the absence of the requested content
- Installed docker-ce package latest stable version
    - The daemon startup settings are contained in the /etc/docker/daemon.json configuration file
## Getting Started
To deploy the project, you need to have the ansible and git packages installed on your machine
### Installing Ansible and Git on Ubuntu  
    sudo apt update
    sudo apt install software-properties-common
    sudo apt-add-repository --yes --update ppa:ansible/ansible
    sudo apt install ansible git
### Deploy project
    git clone https://github.com/efgen42/lab1_2gis.git
Go to the project directory and edit the `hosts` file, specifying the value of the variable `ansible_sudo_pass` as the password for your user with sudo rights
### Run
To run the playbook, use `ansible-playbook up.yml`
## Authors  
  
- Evgeny Semenov [efgen42@gmail.com](mailto:efgen42@gmail.com)
