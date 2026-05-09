# APV - Administrador de Pacientes de Veterinaria

APV es una aplicacion web full stack para la gestion de una clinica veterinaria. El proyecto permite registrar veterinarios, confirmar su cuenta por correo, iniciar sesion, administrar su perfil y gestionar pacientes asociados a cada usuario.

Este repositorio se usa como practica de aprendizaje de desarrollo web moderno, combinando un backend REST con un frontend en React y una base de datos MongoDB.

## Que hace el proyecto

- Registro de veterinarios con confirmacion de cuenta por email.
- Inicio de sesion con autenticacion basada en JWT.
- Recuperacion de password mediante enlace enviado por correo.
- Panel privado para crear, listar, editar y eliminar pacientes.
- Edicion de perfil y cambio de password del veterinario autenticado.
- Proteccion de rutas publicas y privadas segun el estado de autenticacion.

## Tecnologias utilizadas

### Backend

- Node.js
- Express
- MongoDB
- Mongoose
- JWT para autenticacion
- bcrypt para hash de passwords
- Nodemailer para envio de correos
- CORS para control de origenes permitidos

### Frontend

- React 18
- Vite
- React Router DOM
- Axios para consumo de API
- Tailwind CSS para estilos

### Infraestructura

- Docker
- Docker Compose

## Aprendizajes web que demuestra

Este proyecto muestra conceptos clave de desarrollo web moderno:

- Arquitectura cliente-servidor con consumo de una API REST.
- CRUD completo con persistencia en base de datos.
- Relacion entre entidades: cada paciente pertenece a un veterinario.
- Autenticacion y autorizacion con JWT en frontend y backend.
- Proteccion de rutas con middleware en Express y rutas protegidas en React Router.
- Manejo de estado global con Context API.
- Formularios, validacion y flujo de captura de datos en la interfaz.
- Envio de correos transaccionales para confirmacion y recuperacion de acceso.
- Configuracion por variables de entorno para separar desarrollo y ejecucion.
- Contenerizacion con Docker para facilitar despliegue y entornos reproducibles.

## Estructura general

- `backend/`: API, modelos, controladores, rutas y middleware.
- `frontend/`: aplicacion React, paginas, componentes, contexto y configuracion HTTP.
- `docker-compose.dev.yml`: entorno de desarrollo con backend, frontend y MongoDB.
- `docker-compose.prod.yml`: entorno de produccion con frontend servido por nginx.


## Funcionalidades principales por area

### Publico

- Registro de cuenta.
- Confirmacion por correo.
- Inicio de sesion.
- Solicitud de recuperacion de password.

### Privado

- Ver perfil del veterinario.
- Editar datos del perfil.
- Cambiar password.
- Crear, editar, listar y eliminar pacientes.

---

Proyecto desarrollado como practica de aprendizaje en desarrollo full stack con JavaScript.
