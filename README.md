# Challenge Foro Hub - API REST

Este proyecto es una implementación de un foro desarrollado con Java y Spring Boot, donde los usuarios pueden crear tópicos para plantear dudas o sugerencias, y responder a los mismos dentro de una comunidad.

# Características principales
   - Uso de PostgreSQL como base de datos.
   - Migraciones gestionadas con Flyway.
   - Crear, listar, buscar tópico por id, actualizar y eliminar tópicos.
   - Buscar tópicos por palabras clave en el título o contenido.
   - Asociar respuestas a un tópico específico.
   - Seleccionar respuestas como soluciones al tópico.
   - Actualizar el estado del tópico a "Cerrado" cuando tiene al menos una respuesta marcada como solución.
   - Uso de JWT (JSON Web Tokens) para asegurar el acceso a los endpoints.
   - Endpoint para la API con Swagger: `/swagger-ui.html`.
   
# Tecnologías utilizadas

- Java 17.
- Spring Boot 3, Spring Data JPA, Spring Security, Spring Validation.
- PostgreSQL.
- 
# Endpoints

# Tópicos
- Listar tópicos: `GET /topicos`
- Buscar tópico por id `GET / topicos/{id}`
- Buscar tópicos por palabras clave: `POST /topicos/busqueda`
- Crear un tópico: `POST /topicos`
- Actualizar un tópico: `PUT /topicos/{id}`
- Eliminar un tópico: `DELETE /topicos/{id}`

# Respuestas
- Listar respuestas de un tópico: `GET /topicos/{topicoId}/respuestas`
- Crear una respuesta: `POST /topicos/{topicoId}/respuestas`
- Marcar una respuesta como solución: `PUT /topicos/{topicoId}/respuestas/{respuestaId}/solucion`
- Eliminar una respuesta: `DELETE /topicos/{topicoId}/respuestas/{respuestaId}`


