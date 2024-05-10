# Usa la imagen de Alpine Linux como base

FROM node:lts-alpine

# Etiqueta de información
LABEL maintainer="Sergio Antonio Trujillo <sergio.trujillo@garabatos.co>"

# Instala dependencias necesarias
RUN apk update && \
    apk upgrade && \
    apk add --no-cache curl 

# Establece el directorio de trabajo en /app
WORKDIR /app
COPY ./app .

# Instala las dependencias del proyecto
RUN npm install

EXPOSE 4567
EXPOSE 8080
EXPOSE 3030
EXPOSE 3031
EXPOSE 3032

VOLUME ["/app"]
# Comando por defecto para ejecutar la aplicación
CMD ["npm", "dev"]
