# 1. Base : image Node officielle
FROM node:slim

# 2. Définir le dossier de travail
WORKDIR /app

# 3. Copier les fichiers importants
COPY package*.json ./
RUN npm install
COPY . .

# 4. Ouvrir le port que ton app utilise
EXPOSE 5000

# 5. Lancer ton application
CMD ["node", "server.js"]