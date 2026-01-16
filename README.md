# Flowable BPM + PostgreSQL (Dockerized Infrastructure)

Este proyecto despliega una instancia completa del motor de procesos de negocio **Flowable (UI All-in-one)** conectado a una base de datos **PostgreSQL** persistente, utilizando **Docker Compose**.

El objetivo es proporcionar un entorno de desarrollo local rápido, aislado y reproducible para modelar y ejecutar procesos BPMN.

## 🚀 Stack Tecnológico

* **Aplicación:** Flowable UI (Latest) - Incluye Modeler, IDM, Task y Admin.
* **Base de Datos:** PostgreSQL 13 (Alpine).
* **Orquestación:** Docker Compose.
* **Persistencia:** Volumen de Docker local (`postgres_data`).

## 📋 Prerrequisitos

* **Docker Engine** (Linux) o **Docker Desktop** (Windows/Mac).
* **Git** instalado.
* Puertos libres: `8080` (Flowable) y `5432` (Postgres).

## 🛠️ Instalación y Despliegue

1. Levantar el Servicio
```PowerShell
# Si tu usuario tiene permisos de docker
docker compose up -d

# Si no estás en el grupo docker
sudo docker compose up -d
```

2. Verificar el arranque (Espera hasta ver el mensaje: Started Application in ... seconds.)
```PowerShell
docker compose logs -f flowable-ui
```

3. Detener y Limpiar
```PowerShell
docker compose down
```

### 🖥️ Acceso a la Plataforma
Una vez iniciado el servicio, abre tu navegador:

URL: http://localhost:8080/flowable-ui
Usuario por defecto: admin
Contraseña: test

### Reset de Fábrica (Borrar todo)
```PowerShell
docker compose down -v
```

### 1. Clonar el repositorio
```bash
git clone <URL_DE_TU_REPO_GITHUB>
cd flowable-docker-BPMN