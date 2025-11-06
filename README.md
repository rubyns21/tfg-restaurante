# 🍽️ TFG Restaurante - Stack Docker completo

> Este repositorio contiene la estructura completa para el proyecto de Fin de Grado (DAW) desarrollado por Rubyns. Incluye backend en PHP/Laravel, frontend en Angular, base de datos MySQL, automatizaciones con n8n y una interfaz de phpMyAdmin.

## Servicios incluidos

| Servicio | Descripción |
|---------|-------------|
| 🐘 **PHP/Laravel** | API REST del restaurante |
| ⚙️ **Angular** | Aplicación de cliente y administración |
| 🗄️ **MySQL 8** | Base de datos |
| 🧠 **n8n** | Automatizaciones y flujos |
| 🧩 **phpMyAdmin** | Interfaz para gestionar la base de datos |
| 🐳 **Docker Compose** | Orquestador de los contenedores |

## Cómo levantar el proyecto

1. Clona este repositorio.
2. Copia el archivo `.env.example` a `.env` y ajusta las contraseñas si lo deseas.
3. Ejecuta `docker compose up -d --build` para construir e iniciar todos los servicios.

### Accesos por defecto

- **Angular (Frontend)**: http://localhost:4200  
- **Laravel/PHP (Backend)**: http://localhost:8000  
- **phpMyAdmin**: http://localhost:8081 
- **n8n**: http://localhost:5678 

## Estructura del proyecto

```
tfg-restaurante/
├─ backend/         # Código PHP/Laravel
│  └─ Dockerfile
├─ frontend/        # Proyecto Angular
│  └─ Dockerfile
├─ n8n_flows/       # Flujos de n8n
│  └─ n8n_reservas_restaurante.json
├─ docker-compose.yml
├─ .env.example
├─ .gitignore
└─ README.md
```

## Detalles adicionales

- El contenedor de MySQL utiliza la carpeta `./mysql_data` para persistir datos.
- El contenedor de n8n utiliza `./n8n_data` para almacenar la configuración y la base de datos sqlite.
- Puedes cambiar los puertos mapeados en `docker-compose.yml` si alguno está ocupado en tu máquina.
