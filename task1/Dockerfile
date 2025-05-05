# Utilise l'image officielle Ubuntu la plus récente comme base
FROM ubuntu:latest

# Définit le répertoire de travail dans le conteneur
WORKDIR /app

# Met à jour les paquets et effectue une mise à niveau
RUN apt-get update && apt-get upgrade -y

# Installe Python 3 et pip
RUN apt-get install -y python3 python3-pip

# Supprime la gestion externe de Python (pour permettre l'installation de paquets)
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED || true

# Installe Flask via pip
RUN pip3 install flask

# Copie le fichier api.py dans le conteneur
COPY ./api.py /app/

# Ouvre le port 5252
EXPOSE 5252

# Commande de démarrage du conteneur
CMD ["python3", "api.py"]