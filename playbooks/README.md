# Nutanix Treeptik

### Config 

Par défaut, les playbooks utilisent un fichier *hosts* présent à la racine.

## Roles

### Linux

* ssh_keys 

Déploie un ensemble de clés publiques pour le compte de connexion distant.

Créer au préalable un répertoire *public_keys/* à la racine du rôle et y placer un fichier par clé publique. 
Chaque fichier devra être appelé explicitement.

* packages

Installe un ensemble de paquets à partir des repos officiels.
