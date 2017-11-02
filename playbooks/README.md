# Nutanix Treeptik - Playbooks Ansible

### Config 

Par défaut, les playbooks utilisent un fichier `hosts` qui doit être présent à la racine.
Le fichier `group_vars/all.yml` contient les variables. 

## Roles

### Linux

#### ssh_keys

Déploie un ensemble de clés publiques pour le compte de connexion distant.

Créer au préalable un répertoire à la racine du rôle et y placer un fichier par clé publique. 
Le nom du répertoire doit être placé dans le fichier de config `group_vars/all.yml`
L'ensemble des fichiers sera traité. 

#### packages

Installe un ensemble de paquets à partir des repos officiels.

#### monitoring_copy

Synchronise le projet monitoring sur l'ensemble des noeuds du cluster. 

#### monitoring_build

Build les différentes images sur l'ensemble des noeuds du cluster. En effet, pour le moment nous n'avons pas encore de registry corporate.

#### monitoring_deploy

Déploie la stack sur le cluster UCP à partir du premier noeuds `manager`.

## Playbooks 

#### verify_linux

Mise en conformité des noeuds linux du cluster :
- [ssh_keys](# ssh_keys)
- [packages](# packages)

#### deploy_monitoring

Déploiement de la stack de monitoring :
  - [monitoring_copy](# monitoring_copy)
  - [monitoring_build](# monitoring_build)
  - [monitoring_deploy](# monitoring_deploy)


Déploie la stack de monitoring sur un cluster Swarm/UCP :
  - Synchronisation du projet sur l'ensemble des noeuds
  - Build des images de la stack sur chacun des noeuds
  - Déploiement de la stack à partir

