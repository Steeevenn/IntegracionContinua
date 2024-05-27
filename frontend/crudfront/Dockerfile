# Utilizamos la imagen oficial de Node.js en su versión 14
FROM node:14

# Establecemos el directorio de trabajo
WORKDIR /app

# Copiamos solo el archivo package.json y package-lock.json (si existe)
COPY package*.json ./

# Instalamos las dependencias con npm para crear Node Modules
RUN npm install

# Copiamos el resto de los archivos de la aplicación
COPY . .

# Exponemos el puerto  (donde se ejecutará el servicio del frontend)
EXPOSE 3001

# Comando para iniciar el servicio del frontend
CMD ["npm", "start"]