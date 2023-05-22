# Selecciona la imagen base
FROM node:14-alpine

# Define el directorio de trabajo dentro del contenedor
WORKDIR /app

# Copia los archivos necesarios para instalar las dependencias
COPY package*.json ./

# Instala las dependencias
RUN npm install

# Copia el código fuente de la aplicación
COPY . .

# Compila la aplicación
RUN npm run build

# Define el puerto que se va a exponer
EXPOSE 3000

# Ejecuta el comando para iniciar la aplicación
CMD ["npm", "run", "dev"]