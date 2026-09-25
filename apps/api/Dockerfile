# Utilise l'image de node
FROM node:24-alpine
# Crée le dossier app
WORKDIR /app
# copie toutes les dépendances (permet d'accélérer les builds en ne rebuildant pas les dépendances)
COPY package*.json ./
# installe les dépendances
RUN npm ci
# copie le dossier /api dans /app
COPY . .
# expose le port 3000 du docker 
EXPOSE 3000
# lance les commandes
CMD ["npm", "run", "start:dev"]