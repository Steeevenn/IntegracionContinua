# Usa una imagen base de Java
FROM openjdk:17-jdk-alpine

# Copia el archivo JAR de la aplicación al contenedor
COPY target/crud-application-0.0.1-SNAPSHOT.jar /app/crud-application.jar

# Establece el directorio de trabajo
WORKDIR /app

# Comando para ejecutar la aplicación cuando se inicie el contenedor
CMD ["java", "-jar", "crud-application.jar"]

