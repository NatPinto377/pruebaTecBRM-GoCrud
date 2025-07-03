# Aprendizajes y Mejoras: API REST con Go, PostgreSQL y Docker

## 🧠 ¿Qué aprendí?

Durante el desarrollo de esta API RESTful en Go, aprendí a:

- **Conectar Go con PostgreSQL** utilizando el driver `lib/pq` y cadenas de conexión seguras.
- **Usar Docker y Docker Compose** para orquestar múltiples servicios (API + base de datos) de forma consistente.
- **Definir rutas RESTful** con el paquete `gorilla/mux`, manejando métodos `GET`, `POST`, `PUT` y `DELETE`.
- **Crear tablas automáticamente** desde la app si no existen, facilitando el despliegue inicial.
- **Manejar errores comunes** de conexión a base de datos, incluyendo el uso de `Ping()` y reintentos automáticos para esperar la disponibilidad del servicio.

## 🔧 ¿Qué mejoraría?

Aunque la API funciona correctamente, hay aspectos que podría mejorar:

- ✅ **Variables de entorno**: Centralizar configuraciones como credenciales y puertos en un archivo `.env` para mayor seguridad y flexibilidad.
- ✅ **Manejo de errores más detallado**: Actualmente los errores se devuelven con mensajes genéricos. Podría mejorarse con respuestas estructuradas (JSON) y códigos más descriptivos.
- ✅ **Validación de datos**: Agregar validaciones a los campos `username` y `email` antes de insertarlos en la base de datos.
- ✅ **Tests automáticos**: Incluir pruebas unitarias y de integración para asegurar que los endpoints se comporten como se espera.
- ✅ **Separación en capas**: Refactorizar el código para separar la lógica de base de datos, controladores y rutas, siguiendo una arquitectura más limpia.
- ✅ **Autenticación**: Agregar un sistema básico de autenticación (por ejemplo, JWT) para proteger los endpoints de escritura.

---

Este proyecto me permitió fortalecer habilidades en backend con Go, trabajar con contenedores y resolver errores reales en entornos distribuidos.
