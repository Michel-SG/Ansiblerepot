# Ansiblerepot
# Commandes ad-Hoc sur le groupe all et prod
ansible -i hosts.ini all -m ping
ansible -i hosts.ini prod -m ping

# Création de fichier .txt et ajout d'une variable env issue d'un groupe du fichier .ini
ansible -i hosts.ini all -m copy -a "dest=/home/admin/toto.txt content='salut les amis {{env}}'"