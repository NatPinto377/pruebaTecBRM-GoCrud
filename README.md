# 🚀 API REST con Go, PostgreSQL y Docker

## 🧠 Lo que aprendí

Este proyecto me ayudó a reforzar varios temas importantes en el desarrollo backend:

- 🔗 **Conexión entre Go y PostgreSQL** usando el driver `lib/pq`.
- 🐳 **Docker y Docker Compose** para levantar todo el entorno fácilmente.
- 🔁 **Rutas REST completas** (`GET`, `POST`, `PUT`, `DELETE`) con `gorilla/mux`.
- 🛠️ Cómo **crear la tabla automáticamente** si no existe.
- 🧱 Uso de variables de entorno para separar la config.
- 🕒 Manejo de errores al conectar con la base de datos, con reintentos incluidos.

> 💡 Fue clave entender cómo se comunican los contenedores entre sí y lo importante que es esperar a que la base de datos esté lista.

---

## 🔧 Lo que mejoraría

Hay varias cosas que me gustaría seguir puliendo en la API:

- ✅ **Validación de datos** antes de insertarlos (por ejemplo, emails válidos).
- ✅ Manejo de errores más detallado, devolviendo mensajes JSON bien estructurados.
- ✅ **Organizar mejor el código** separando rutas, controladores y DB.
- ✅ Implementar autenticación (JWT o tokens simples).
- ✅ Agregar **tests automáticos** para endpoints.
- ✅ Usar `.env` para separar totalmente configuración y secretos.

---

## 🌱 Próximos pasos

- [ ] Agregar autenticación.
- [ ] Refactorizar en capas (handlers, models, db).
- [ ] Documentar la API con Swagger o Postman.
- [ ] Subir a un repositorio en GitHub.

---

✨ En resumen: este proyecto fue muy útil para practicar cómo levantar una API desde cero con Go, conectarla con una base de datos, y dejarla corriendo en Docker como un servicio real.

