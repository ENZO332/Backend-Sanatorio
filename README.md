# Backend - Sistema de Guardia Hospitalaria

API REST desarrollada para la gestión de pacientes en una guardia hospitalaria, permitiendo registrar ingresos, administrar la cola de atención y gestionar el flujo de pacientes según su nivel de emergencia.
Este proyecto fue desarrollado como parte de un TFI para la materia "Ingenireria de Software" del 4to nivel.

---

## Tecnologías utilizadas

- Java
- Spring Boot
- Spring Data JPA
- Spring Security
- PostgreSQL
- Maven
- Cucumber Java

---

## Funcionalidades principales

- Autenticación de usuarios
- Registro y gestión de pacientes
- Registro de ingresos a guardia
- Clasificación por nivel de emergencia
- Cola de atención en tiempo real
- Atencion de pacientes en cola de espera
- Consulta de pacientes en atención
- Detalle completo de cada ingreso

---

## Arquitectura

El sistema está diseñado siguiendo una arquitectura en capas:

- Controller → Manejo de endpoints REST
- Service → Servicios de aplicacion
- Domain → Lógica de negocio
- Repository → Acceso a datos (JPA)
- DTOs → Transferencia de datos entre capas

---

## Endpoints principales

| Método | Endpoint                         | Descripción |
|--------|----------------------------------|------------|
| POST   | `/auth/login`                   | Autenticación de usuario |
| GET    | `/api/ingresos/cola`            | Obtener cola de atención |
| GET    | `/api/ingresos/en-atencion`     | Paciente en atención |
| GET    | `/api/ingresos/{id}/detalle`    | Detalle de ingreso |
| POST   | `/api/ingresos`                 | Registrar ingreso |
| POST   | `/api/pacientes`                | Registrar paciente |
| POST   | `/api/medico/{ingresoId}/iniciar` | Iniciar atención al paciente |
---

## Configuración y ejecución

1. Clonar el repositorio

git clone https://github.com/ENZO332/Backend-Sanatorio.git  
cd Backend-Sanatorio

---

2. Configurar base de datos

Editar application.properties o application.yml:

spring.datasource.url=jdbc:postgresql://localhost:5432/tu_db  
spring.datasource.username=tu_usuario  
spring.datasource.password=tu_password  

---

3. Ejecutar la aplicación

./mvnw spring-boot:run  

o  

mvn spring-boot:run  

---

## Testing

El proyecto incluye pruebas automatizadas para validar flujos de negocio clave como:

- Registro de admisiones
- Priorización por nivel de emergencia
- Busqueda de pacientes
- Registro de pacientes
- Autenticacion de usuarios

---

## Estado del proyecto

✔ Versión estable funcional  
En constante mejora  

---

## Autor

Enzo Juarez  
Estudiante de Ingeniería en Sistemas – UTN  

---

## 📎 Notas

Este proyecto fue desarrollado como parte de una práctica académica orientada a simular un sistema real de gestión hospitalaria.
