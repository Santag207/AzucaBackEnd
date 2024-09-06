# AzucaBackEnd

AzucaBackEnd es el backend de un sistema que gestiona una aplicación con funcionalidades de autenticación de usuarios, gestión de roles y otras capacidades relacionadas con la administración de datos. Está construido usando tecnologías robustas para asegurar la escalabilidad, seguridad y fácil mantenimiento del código.

## Características

- **Autenticación de usuarios**: Permite registrar, iniciar sesión y gestionar usuarios.
- **Roles y permisos**: Soporte para la gestión de diferentes niveles de permisos de usuario.
- **Integración con base de datos**: Mapea objetos con una base de datos relacional utilizando Hibernate y JPA.
- **API REST**: Implementación de controladores REST para manejar operaciones CRUD (crear, leer, actualizar y eliminar).
- **Pruebas unitarias e integración**: Incluye pruebas con JUnit y Mockito.
- **Despliegue mediante Docker**: Preparado para ser contenerizado con Docker.
- **Integración continua con Jenkins**: Implementación de pipelines de CI/CD.

## Tecnologías Utilizadas

- **Java 21**: Lenguaje de programación utilizado para el backend.
- **Spring Boot**: Framework principal para la creación de la aplicación.
- **Spring MVC**: Para la implementación de controladores y rutas RESTful.
- **Spring Security**: Para la autenticación y autorización de usuarios.
- **JPA/Hibernate**: Para el mapeo objeto-relacional y la gestión de la base de datos.
- **PostgreSQL**: Sistema de gestión de base de datos utilizado.
- **JUnit y Mockito**: Para pruebas unitarias y de integración.
- **Maven**: Para la gestión de dependencias y la construcción del proyecto.
- **Docker**: Para contenerizar y desplegar la aplicación.
- **Jenkins**: Para la integración continua y la entrega continua del código.

## Requisitos

- **Java 21** o superior.
- **Maven 3.6** o superior.
- **PostgreSQL 12** o superior.
- **Docker 19.03** o superior.
- **Jenkins 2.249.1** o superior.

  ## Ejecución del Proyecto

1. Clona el repositorio:
   ```bash
   git clone https://github.com/tu-usuario/AzucaBackEnd.git

2. Navega al directorio del proyecto:
   ```bash
   cd AzucaBackEnd

3. Compila y ejecuta la aplicación:
   ```bash
   mvn spring-boot:run

4. Para ejecutar dentro de un contenedor Docker:
   ```bash
   docker build -t azucabackend .
   docker run -p 8080:8080 azucabackend

### Pruebas
1. Para ejecutar las pruebas:
   ```bash
   mvn test
   
## Diccionario de Datos

### Tablas del Sistema de Usuarios

#### `user`
- **id_user** (BIGINT): Identificador único del usuario.
- **username** (VARCHAR): Nombre de usuario.
- **password** (VARCHAR): Contraseña cifrada.
- **email** (VARCHAR): Correo electrónico.
- **role** (VARCHAR): Rol del usuario en el sistema (admin, user, etc.).

## Integración Continua

El proyecto usa Jenkins para la integración continua. El archivo `.jenkinsfile` contiene las configuraciones para los pipelines de integración continua.

## Tecnologías Planeadas para el Futuro

En futuras iteraciones del proyecto, se tiene previsto agregar las siguientes tecnologías y características:

- **Gestión de Inventario (Inventory Management)**: Controladores y servicios para manejar el inventario (inventory.controller.ts, inventory.service.ts, inventory.routes.ts).
- **Blog y Comunidad (Blog and Community)**: Funcionalidades para un blog y comunidad, incluidos controladores y rutas (blog.controller.ts, community.controller.ts, blog.routes.ts, community.routes.ts).
- **Proyectos y Calendario (Projects and Calendar)**: Módulo para gestionar proyectos y calendario (projects.controller.ts, calendar.controller.ts, projects.routes.ts, calendar.routes.ts).
- **RESTful API**: Implementación de una API RESTful para la comunicación entre el frontend y el backend.
- **HTTP Methods (GET, POST, PUT, DELETE)**: Definición de los métodos HTTP para gestionar las solicitudes del frontend.
- **JWT (JSON Web Tokens)**: Para la autenticación segura y basada en tokens en el backend.
