# Dockerfile para el frontend Angular
FROM node:20

# Establecer el directorio de trabajo
WORKDIR /usr/src/app

# Copiar paquetes de Node
COPY package*.json ./

# Instalar dependencias
RUN npm install

# Copiar el resto del código de la aplicación
COPY . .

# Exponer el puerto en el que Angular servirá la aplicación
EXPOSE 4200

# Comando por defecto
CMD ["npm", "start"]
