# Ansible-EasyTraining

TP 5 
Installation sur un serveur d'un container docker apache avec Ansible.

Creer un dossier webapps, copier le contenu du git dedans et creer un fichier hosts.yaml

[admin@node1 webapps]$ cat hosts.yaml 
all:
  vars:
    ansible_ssh_common_args: '-o StrictHostKeyChecking=no'
prod:
  hosts:
    client:
      ansible_host: 10.0.0.4


ansible-playbook -i hosts.yaml deploy.yaml
