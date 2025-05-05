# Utilisation de l'image officielle Nginx comme base pour notre serveur proxy
FROM nginx:latest

# Copie du fichier de configuration personnalisé dans le conteneur
# Ce fichier remplace la configuration par défaut de Nginx dans le conteneur
COPY ./proxy.conf /etc/nginx/conf.d/default.conf

# Indique que le conteneur expose le port 80 (HTTP standard)
# Cette instruction est documentaire et n'ouvre pas réellement le port
EXPOSE 80