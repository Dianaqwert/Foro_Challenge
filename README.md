# Foro [CHALLENGE] :

Este proyecto implementa una API REST para gestionar tópicos, desarrollada con Spring Boot y enfocada en brindar funcionalidades CRUD (Crear, Leer, Actualizar y Eliminar).

Características principales:

Modelo REST: Rutas organizadas siguiendo las mejores prácticas.
Validaciones: Implementación de reglas de negocio para datos consistentes.
Persistencia de datos: Uso de MySQL con integración de Spring Data JPA y migraciones gestionadas con Flyway.
Seguridad: Autenticación y autorización con Spring Security para proteger los datos.
Desarrollo ágil: Uso de herramientas como Lombok y Spring Boot DevTools para optimizar la productividad.
El proyecto está diseñado para ser escalable y seguir los estándares modernos de desarrollo web backend.

## Configuración
Este documento detalla la configuración inicial y los pasos necesarios para desarrollar un proyecto Spring Boot centrado en la implementación de una API REST con funcionalidades CRUD.

## Índice
1. [Requisitos Iniciales](#requisitos-iniciales)
   - [Herramientas y Versiones Necesarias](#herramientas-y-versiones-necesarias)
   - [Guía de Instalación de MySQL](#guía-de-instalación-de-mysql)
2. [Configuración del Proyecto](#configuración-del-proyecto)
   - [Opciones del Proyecto](#opciones-del-proyecto)
   - [Dependencias a Agregar](#dependencias-a-agregar)
3. [Configuración en el Proyecto](#configuración-en-el-proyecto)
   - [Dependencias en `pom.xml`](#dependencias-en-pomxml)
   - [Configuración en `application.properties`](#configuración-en-applicationproperties)
4. [Objetivos del Proyecto](#objetivos-del-proyecto)
5. [Funcionalidades de la API](#funcionalidades-de-la-api)
6. [Desarrollo](#desarrollo)

---

## Requisitos Iniciales

### Herramientas y Versiones Necesarias:
- **Java**: Versión 17 o superior. Descarga la última versión LTS de Java gratuita.
- **Maven**: Versión 4 o superior (Spring Initializr utiliza Maven por defecto).
- **Spring Boot**: Versión 3 o superior. Disponible en [Spring Initializr](https://start.spring.io/).
- **MySQL**: Versión 8 o superior. Descarga el instalador desde [MySQL Installer](https://dev.mysql.com/downloads/installer/).
- **IDE IntelliJ IDEA** (opcional): Descarga desde [IntelliJ IDEA](https://www.jetbrains.com/idea/).

### Guía de Instalación de MySQL
Puedes consultar el artículo de Alura Latam para una guía paso a paso sobre la instalación de MySQL en Windows: [MySQL: desde la descarga e instalación hasta su primera tabla](https://www.alura.com.br/).

---

## Configuración del Proyecto

### Opciones del Proyecto
1. Lenguaje: Java
2. Formato de empaquetado: JAR
3. Versión de Java: 17 o superior

### Dependencias a Agregar
- Lombok
- Spring Web
- Spring Boot DevTools
- Spring Data JPA
- Flyway Migration
- MySQL Driver
- Validation
- Spring Security

---

## Configuración en el Proyecto

### Dependencias en `pom.xml`
Asegúrate de incluir las siguientes dependencias si no las agregaste durante la configuración inicial:

```xml
<dependencies>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-web</artifactId>
    </dependency>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-data-jpa</artifactId>
    </dependency>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-security</artifactId>
    </dependency>
    <dependency>
        <groupId>org.flywaydb</groupId>
        <artifactId>flyway-core</artifactId>
    </dependency>
    <dependency>
        <groupId>mysql</groupId>
        <artifactId>mysql-connector-java</artifactId>
    </dependency>
    <dependency>
        <groupId>org.projectlombok</groupId>
        <artifactId>lombok</artifactId>
        <scope>provided</scope>
    </dependency>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-validation</artifactId>
    </dependency>
</dependencies>
```

### Configuración en `application.properties`
Configura la conexión a la base de datos MySQL:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/tu_base_de_datos
spring.datasource.username=tu_usuario
spring.datasource.password=tu_contraseña
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver

spring.jpa.hibernate.ddl-auto=validate
spring.jpa.show-sql=true

flyway.enabled=true
flyway.baseline-on-migrate=true
```

> **Nota**: Crea tu base de datos antes de continuar con las migraciones.

---

## Objetivos del Proyecto
El proyecto es una API REST centrada en la gestión de tópicos, implementando las siguientes funcionalidades CRUD:

1. **Crear un nuevo tópico**
2. **Mostrar todos los tópicos creados**
3. **Mostrar un tópico específico**
4. **Actualizar un tópico**
5. **Eliminar un tópico**

---

## Funcionalidades de la API

1. **Modelo REST**:
   - Las rutas se implementan siguiendo las mejores prácticas del modelo REST.

2. **Validaciones**:
   - Se realizan validaciones según las reglas de negocio.

3. **Persistencia de Datos**:
   - La información se almacena en una base de datos MySQL utilizando JPA y Flyway.

4. **Autenticación y Autorización**:
   - Se implementa Spring Security para restringir el acceso a la información según roles o permisos.

---




