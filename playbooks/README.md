# Nutanix Treeptik - Playbooks

### Config 

Par défaut, les playbooks utilisent un fichier *hosts* qui doit être présent à la racine.
Le fichier *group_vars/all.yml* contient les variables. 

## Roles

### Linux

* ssh_keys 

Déploie un ensemble de clés publiques pour le compte de connexion distant.

Créer au préalable un répertoire à la racine du rôle et y placer un fichier par clé publique. 
Le nom du répertoire doit être placé dans le fichier de config *group_vars/all.yml*
L'ensemble des fichiers sera traité. 

* packages

Installe un ensemble de paquets à partir des repos officiels.
