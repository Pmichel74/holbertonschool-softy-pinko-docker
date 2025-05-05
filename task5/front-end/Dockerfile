# Dockerfile pour le front-end de l'application Softy Pinko

# Utilise l'image officielle nginx comme base
FROM nginx:latest

# Copie les fichiers de l'application web dans le répertoire de publication nginx
COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Copie le fichier de configuration nginx personnalisé
COPY ./softy-pinko-front-end.config /etc/nginx/conf.d/default.conf

# Indique que le conteneur écoute sur le port 9000
EXPOSE 9000