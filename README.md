
CRUD

Aplicación CRUD usando React y Spring Boot

Este proyecto es una aplicación CRUD (Crear, Leer, Actualizar, Eliminar) simple creada con React para el frontend y Spring Boot para el backend. Le permite gestionar una colección de elementos.

=> Tabla de contenidos

 Requisitos previos
 Instalación
 Ejecutando la aplicación
 Uso
 Estructura del proyecto
 Tecnologías utilizadas

=>Comenzando

 Node.js y npm instalados.
 Java y Maven para Spring Boot.
 Una base de datos compatible (por ejemplo, MySQL, PostgreSQL) con el esquema creado.

=> Instalación


-> Instalar dependencias frontend:

instalación de npm del cliente de CD

-> Configurar el backend:

 Cree un archivo application.properties en el directorio src/main/resources del proyecto Spring Boot.
 Configure la conexión de su base de datos en application.properties. Por ejemplo:

-> propiedades

spring.datasource.url=jdbc:mysql://localhost:3306/su_base de datos spring.datasource.username=su_nombre de usuario spring.datasource.password=su_contraseña

Especifique otras configuraciones como el puerto del servidor y el registro según sea necesario.

-> Construya el proyecto Spring Boot:

cd server mvn clean install Ejecutando la aplicación

-> Inicie el servidor Spring Boot:

servidor de cd mvn spring-boot: ejecutar

El servidor backend ahora debería estar ejecutándose en http://localhost:8080.

-> Inicie la interfaz de React:

inicio de npm del cliente de CD

El servidor de desarrollo de React debería iniciar y abrir la aplicación en su navegador web predeterminado en http://localhost:3000.

=> Uso

Acceda a la aplicación CRUD a través del navegador web. Realice operaciones CRUD en los artículos. Cree, lea, actualice y elimine elementos en la base de datos.

=> Estructura del proyecto

-> El proyecto se estructura de la siguiente manera:

cliente/: Contiene el código de interfaz de React. server/: Contiene el código backend de Spring Boot. base de datos/: Contiene el esquema de la base de datos y los scripts de migración.

=> Tecnologías utilizadas
 React
 Spring Boot
 Java
 MySQL (o su base de datos preferida)
 npm
 Maven



