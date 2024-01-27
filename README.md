# ModSecurity

![image](https://raw.githubusercontent.com/owasp-modsecurity/ModSecurity/v3/master/others/modsec.png)

ModSecurity is an open-source web-based firewall application (or WAF) supported by different web servers: Apache, Nginx and IIS. The module is configured to protect web applications from various attacks. ModSecurity supports flexible rule engine to perform both simple and complex operations.

# ModeSecurity Working 

![image](https://github.com/ATUL9372/ModSecurity_with_Nginx/assets/99254634/deac3d76-fc92-483b-9998-ad47e4e22eb4)


## Instructions

1. Install [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/installation_distros.html#installing-ansible-on-ubuntu)

2. Install [vscode (optional)](https://code.visualstudio.com/download)
   
3. Install python3 python3-pip

         sudo apt install python3 python3-pip

4. Install sshpass

         sudo apt install sshpass


5. Modify/Add host IPs to `hosts` and configure the variables. Eg.

         [test]
         192.168.xx.xx
         13.57.xx.xx
         
         [test:vars]
         
         ansible_connection=ssh
         ansible_ssh_user=ENTER-USER-NAME
         ansible_ssh_pass=ENTER-PASSWORD


6. Run ansible playbook on 'Ubuntu Server' used this command.


         ansible-playbook -i hosts modsecurity_with_nginx_ubuntu.yml
   
7. Run ansible playbook on 'CentOS Server' used this command.


         ansible-playbook -i hosts modsecurity_with_nginx_centos_7.yml


8. Run ansible playbook with sudo password use -k and -K Eg.

         
         ansible-playbook -i hosts trivy_automation.yml -k
         
         ansible-playbook -i hosts trivy_automation.yml -K

