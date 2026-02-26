# 🎓 Sistema de Matrículas Universitarias

Sistema web para la gestión integral de matrículas universitarias desarrollado con Spring Boot, MySQL, React y arquitectura de Microservicios.

## 📌 Descripción

El Sistema de Matrículas Universitarias permite administrar el proceso académico de inscripción de estudiantes en cursos, controlando cupos, validaciones y registros históricos.

El sistema está diseñado bajo una arquitectura de microservicios, lo que permite:

Escalabilidad independiente

Alta disponibilidad

Fácil mantenimiento

Despliegue autónomo de servicios

## 🏗️ Arquitectura del Sistema

La aplicación está dividida en microservicios independientes que se comunican mediante APIs REST.

### 🔹 Componentes principales

Frontend: React

Backend: Spring Boot

Base de datos: MySQL

Arquitectura: Microservicios

Comunicación: REST APIs

Autenticación: JWT

Gestión centralizada: API Gateway

Configuración distribuida: Config Server

## 🧠 Fundamento Teórico
### 🔹 Spring Boot

Framework basado en Spring que permite crear aplicaciones Java rápidamente con mínima configuración.

Ventajas:

Configuración automática

Integración con bases de datos

Seguridad integrada

Creación rápida de APIs REST

### 🔹 React

Biblioteca de JavaScript desarrollada por Meta Platforms para construir interfaces de usuario dinámicas basadas en componentes reutilizables.

Ventajas:

Virtual DOM

Arquitectura basada en componentes

Alta eficiencia

Gran ecosistema

### 🔹 MySQL

Sistema de gestión de bases de datos relacional ampliamente utilizado en aplicaciones web.

Características:

Integridad referencial

Soporte para transacciones

Alto rendimiento

Open Source

### 🔹 Arquitectura de Microservicios

Es un estilo arquitectónico donde una aplicación se divide en servicios pequeños e independientes que:

Se despliegan de manera autónoma

Tienen su propia base de datos

Se comunican mediante HTTP/REST

Escalan de forma individual

Ventajas:

Mayor resiliencia

Desarrollo independiente por equipos

Mejor mantenimiento

Escalabilidad granular

## ⚙️ Funcionalidades
👨‍🎓 Gestión de Estudiantes

Registro de estudiantes

Actualización de datos

Eliminación lógica

Consulta por código

### 📚 Gestión de Cursos

Creación de cursos

Asignación de créditos

Gestión de docentes

Control de cupos

### 📝 Gestión de Matrículas

Inscripción en cursos

Validación de prerrequisitos

Control de duplicidad

Historial académico

### 🔐 Seguridad

Autenticación con JWT

Autorización por roles:

ADMINISTRADOR

ADMINISTRATIVO

ESTUDIANTE

DOCENTE

Protección de endpoints

## 🔄 Flujo de Funcionamiento

El usuario interactúa con la interfaz en React.

React consume la API Gateway.

El Gateway redirige al microservicio correspondiente.

El microservicio procesa la solicitud y accede a su base de datos MySQL.

La respuesta retorna al cliente.

## 🚀 Instalación y Ejecución
### 1️⃣ Clonar el repositorio
git clone https://github.com/tuusuario/matriculas-universitarias.git
cd matriculas-universitarias
### 2️⃣ Configurar la base de datos

Crear la base de datos en MySQL:

CREATE DATABASE `ms-administrador`;

CREATE DATABASE `ms-administrativo`;
CREATE DATABASE `ms-calendarioacademico`;
CREATE DATABASE `ms-carrera`;
CREATE DATABASE `ms-curso`;
CREATE DATABASE `ms-docente`;
CREATE DATABASE `ms-estudiante`;
CREATE DATABASE `ms-evaluacionacademica`;
CREATE DATABASE `ms-materialeseducativos`;
CREATE DATABASE `ms-planificacionacademica`;
CREATE DATABASE `ms-auth`;
CREATE DATABASE `ms-persona`;
CREATE DATABASE `ms-roles`;
CREATE DATABASE `ms-usuarios`;
CREATE DATABASE `ms-inscripciones`;
CREATE DATABASE `ms-postulante`;
CREATE DATABASE `ms-realTimeChat`;
CREATE DATABASE `ms-matriculas`;
CREATE DATABASE `ms-pagos`;
CREATE DATABASE `ms-requisitosAcademicos`;
CREATE DATABASE `ms-nivelesDeEnsenanza`;
CREATE DATABASE `ms-cuentaFinancieraU`;

SHOW VARIABLES LIKE 'max_connections';
SET GLOBAL max_connections = 200; -- Aumenta según sea necesario

Configurar el archivo application.yml de cada microservicio:

spring:
  datasource:
    url: jdbc:mysql://localhost:3306/ms-administrador (etc.)
    username: root
    password: tu_password

### 3️⃣ Ejecutar los microservicios
mvn spring-boot:run
### 4️⃣ Ejecutar el frontend
cd frontend
npm install
npm start

## 🧪 Pruebas

Pruebas unitarias con JUnit

Pruebas de integración

Testing del frontend con Jest

## 📈 Mejoras Futuras

Contenerización con Docker

Orquestación con Kubernetes

Comunicación asíncrona con RabbitMQ

Implementación de CI/CD

Monitoreo con Prometheus y Grafana

## 📜 Licencia

Este proyecto está bajo la licencia MIT.

---

## 👨‍💻 Autor

**Josue Ochoa**  
Estudiante de Ingeniería de Sistemas

Proyecto académico desarrollado para demostrar la implementación de una arquitectura de microservicios aplicada a un sistema universitario.

---

✨ *Gracias por visitar el proyecto* ✨