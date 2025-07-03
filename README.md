# 📋 Documentación Técnica – API REST en Go (Prueba Técnica)

Hola equipo 👋, A continuación les comparto la documentación funcional de la API REST desarrollada como parte de la prueba técnica solicitada. El objetivo es ofrecer un backend simple pero robusto para gestión de usuarios, construido con **Go**, **PostgreSQL** y empaquetado con **Docker Compose**, permitiendo portabilidad y despliegue inmediato.

---

##  Tecnologías empleadas

- **Lenguaje:** Go (Golang)
- **Framework:** Gorilla Mux (router HTTP)
- **Base de datos:** PostgreSQL
- **Contenedores:** Docker + Docker Compose
- **Cliente sugerido para pruebas:** Postman o `curl`

---

## 🚀 ¿Cómo ejecutar el proyecto?

### ✅ Requisitos

- Docker y Docker Compose instalados
- Sistema operativo: Windows, macOS o Linux

### 🧱 Pasos

1. Clonar o descomprimir el repositorio en el equipo local.
2. Abrir terminal en la raíz del proyecto.
3. Ejecutar:

```bash
docker compose up --build
```

4. Una vez desplegado, la API estará disponible en:

```
http://localhost:8080
```

---

## 📁 Estructura de la solución

```
go-crud-live/
├── Dockerfile
├── docker-compose.yml
├── go.mod / go.sum
├── main.go
```

---

## 🔐 Credenciales por defecto (en entorno local)

| Parámetro     | Valor          |
| ------------- | -------------- |
| Host          | `go_db`        |
| Usuario       | `postgres`     |
| Contraseña    | `postgres`     |
| Base de datos | `go_crud_live` |

Estas credenciales están definidas en `docker-compose.yml`.

---

## 🧪 Endpoints del API

---

### 📄 `GET /users`

- Retorna todos los usuarios registrados.
- **Respuesta esperada:**

```json
[
  {
    "id": 1,
    "username": "carlos",
    "email": "carlos@example.com"
  }
]
```

---

### 🔍 `GET /users/{id}`

- Retorna un usuario por su ID.
- **Ejemplo de éxito:**

```json
{
  "id": 1,
  "username": "carlos",
  "email": "carlos@example.com"
}
```

---

### 📝 `POST /users`

- Crea un nuevo usuario.
- **Body esperado:**

```json
{
  "username": "ana",
  "email": "ana@example.com"
}
```

- **Respuesta:**

```json
{
  "id": 2,
  "username": "ana",
  "email": "ana@example.com"
}
```

---

### ✏️ `PUT /users/{id}`

- Actualiza un usuario existente.
- **Body:**

```json
{
  "username": "Ana Actualizada",
  "email": "ana.nueva@example.com"
}
```

---

### ❌ `DELETE /users/{id}`

- Elimina un usuario por ID.
- **Respuesta:** `204 No Content` o `404 Not Found` si no existe.

---

## 💻 Ejemplo de prueba con `curl`

```bash
curl -X POST http://localhost:8080/users \
  -H "Content-Type: application/json" \
  -d '{"username":"juan", "email":"juan@example.com"}'
```

---

## 🖼️ Capturas sugeridas para documentar

1. Docker levantando servicios (`go-app`, `go_db`)
2. GET a `/users` vacío
3. POST creando usuario
4. GET a `/users/{id}` exitoso
5. PUT actualizando datos
6. DELETE y validación posterior
7. Código abierto en VS Code (resaltado `main.go`)
8. Error controlado (por ejemplo, email duplicado)

---

## 🧹 Comentarios adicionales

- El código está modularizado y preparado para escalar (por ejemplo, agregar autenticación, logs avanzados o middleware de validación).
- El middleware `jsonContentTypeMiddleware` asegura que todas las respuestas del API sean entregadas como `application/json`.
- La base de datos se inicializa automáticamente con la tabla `users` si no existe.

---

## 📢 Contacto

Si desean desplegar esta misma solución en la nube (Render, Railway, Fly.io), integrar autenticación JWT o conectar a un frontend, estoy disponible para continuar el desarrollo sin problema.

Saludos,\
**William Bermúdez**\
📧 [william.bermudez@ejemplo.com](mailto\:william.bermudez@ejemplo.com)\
📍 Bogotá, Colombia

