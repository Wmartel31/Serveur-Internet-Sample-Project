# Étape 1 : image de base
FROM mariadb:latest
 
# Étape 2 : copier les scripts SQL d'initialisation dans le dossier que MariaDB lit au démarrage
# /docker-entrypoint-initdb.d/ est exécuté automatiquement par l'image officielle
COPY init.sql /docker-entrypoint-initdb.d/
 
# Étape 3 : (optionnel) copier un fichier de configuration personnalisé
# COPY my.cnf /etc/mysql/my.cnf
 
# Étape 4 : définir les variables d'environnement par défaut
# Celles-ci seront utilisées pour créer la DB et l'utilisateur
ENV MARIADB_ROOT_PASSWORD=123
ENV MARIADB_DATABASE=tasksdb
 
 
# Le port par défaut de MariaDB
EXPOSE 3306