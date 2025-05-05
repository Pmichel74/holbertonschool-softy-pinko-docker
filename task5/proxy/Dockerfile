# Dockerfile pour le serveur proxy de l'application Softy Pinko
# Utilisation de l'image Nginx officielle comme base
FROM nginx:latest

# Copie du fichier de configuration du proxy dans le conteneur
# Cette configuration remplace la configuration par défaut de Nginx
COPY ./proxy.conf /etc/nginx/conf.d/default.conf

# Indique que le conteneur écoute sur le port 80
EXPOSE 80