---
layout: page
title: Arquitectura
permalink: /arquitectura/
---

# Diagrama de Arquitectura
![Diagrama de arquitectura](../assets/architecture.png)

# Decisiones de Arquitectura
### Microservicios
- **Python + FastAPI**:
Elegimos FastAPI para los principales microservicios backend por su rapidez, facilidad de desarrollo y excelente soporte para APIs modernas (OpenAPI, validación automática, tipado). Esto nos permitió construir endpoints robustos y fácilmente testeables para usuarios, canciones y notificaciones.

- **JS + Express**:
Para el microservicio de notificaciones, elegimos el stack de JS + Express debido a que teníamos más experiencia con el lenguaje y su implementación no era muy distinto a lo que veníamos haciendo con Python + FastAPI.

- **Separación en microservicios**:
Dividimos el backend en tres servicios principales (users-api, songs-api, notifications-api) para facilitar el mantenimiento, la escalabilidad y el trabajo en equipo. Cada servicio tiene su propio ciclo de vida y puede escalarse de forma independiente.

### Bases de Datos
- **PostgreSQL**:
Usamos PostgreSQL como base de datos principal por su robustez, soporte para relaciones complejas y compatibilidad con los ORMs modernos de Python.
Cada microservicio tiene su propia base de datos, lo que mejora la seguridad y el aislamiento de datos.

- **SQLite en memoria**:
Para testing y desarrollo rápido, usamos SQLite en memoria en algunos entornos, permitiendo pruebas sin necesidad de levantar un servidor de base de datos.

### Almacenamiento de archivos: Cloudflare R2
- **R2**:
Para almacenamiento de archivos (imágenes de portadas, audios, etc.), usamos Cloudflare R2.
R2 es compatible con S3, económico y fácil de integrar con FastAPI y otros servicios.
Esto nos permitió desacoplar el almacenamiento de archivos del backend y escalarlo según la demanda.

### Autenticación: Google Auth y JWT
- **Google Auth**:
Integramos autenticación con Google para facilitar el registro y login de usuarios, mejorar la seguridad y ofrecer una experiencia moderna.
Usamos la librería oficial de Google y validamos los tokens en el backend.

- **JWT**:
Para la autenticación interna, usamos JWT (JSON Web Tokens).
Esto permite que los microservicios validen la identidad del usuario de forma rápida y segura, y facilita la integración con el frontend móvil.

### Frontend Mobile: Expo + React Native
- **Expo Router**:
Usamos Expo Router para la navegación en la app móvil, lo que simplifica el manejo de rutas, deep linking y el stack de navegación.

- **React Native**:
Permite desarrollo multiplataforma (iOS/Android) y fácil integración con librerías de notificaciones, autenticación y diseño.

### Notificaciones Push: Firebase Cloud Messaging
- **FCM**:
Elegimos Firebase Cloud Messaging para enviar notificaciones push por su confiabilidad, integración nativa y soporte multiplataforma.

### Infraestructura y DevOps
- **Railway**:
Usamos Railway para el deploy de los microservicios por su facilidad de uso, integración con bases de datos y despliegue automático desde GitHub.

- **Github Actions**:
Implementamos Github Actions para automatizar los flujos de integración y despliegue continuo (CI/CD). Esto nos permitió ejecutar tests, validar el código y desplegar los servicios automáticamente ante cada cambio en el repositorio, mejorando la calidad y velocidad de desarrollo.

- **Github Pages**:
Para la documentación y bitácora, usamos Github Pages, permitiendo acceso público y fácil edición colaborativa.