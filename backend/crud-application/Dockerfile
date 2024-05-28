

#etapa 1 Creación del Jar
#Usar la imagen de Maven y Openjdk 17 y definirlo como constructor
FROM maven:3.8.5-openjdk-17 as builder
#Establecer el directorio de trabajo
WORKDIR /app
#Copiar archivo pom con las dependencias necesarias para el trabajo
COPY pom.xml .
#resolvemos todas las dependencias del proyecto Lo que significa que ahora tenemos todo esto instalado en nuestro contenedor para facilitar la agrupación del archivo .jar 
RUN mvn dependency:go-offline
#Copiamos todos los archivos y paquetes/directorios que están dentro de nuestro proyecto local
COPY src/ ./src/
#ejecutamos el comando anterior para agrupar nuestra aplicación y crear un archivo jar. El indicador -DskipTests=true se utiliza para omitir la ejecución de la prueba.
RUN mvn clean package -DskipTests=true


#etapa 2 Creación del Jar
#Traemos imagen de jdk
FROM openjdk:17-jdk-alpine as prod
#creamos el directorio de aplicación

# copie el archivo jar de la etapa del generador en la primera etapa, que se encuentra en /app/target/. lo copiamos en /app/app.jar
COPY --from=builder /app/target /app/app.jar/
#definimos el puerto del servicio
ENV SERVER_PORT=6060
# Establece el directorio de trabajo
WORKDIR /app
#Le indicamos a docker que exponga el puerto donde trabajará el servicio
EXPOSE 6060
#Correr aplicación cuando inicie el contenedor
CMD [ "executable" ] ["java","-jar", "app.jar"]

#Archivo inicial
# Usa una imagen base de Java
#FROM openjdk:17-jdk-alpine

# Copia el archivo JAR de la aplicación al contenedor
#COPY target/crud-application-0.0.1-SNAPSHOT.jar /app/crud-application.jar

# Establece el directorio de trabajo
#WORKDIR /app

# Comando para ejecutar la aplicación cuando se inicie el contenedor
#CMD ["java", "-jar", "crud-application.jar"]