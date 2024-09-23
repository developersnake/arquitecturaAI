# arquitecturaAI
# Diagrama de Secuencia

Este diagrama ilustra el flujo de interacción entre los distintos componentes del sistema.

```mermaid
sequenceDiagram
    actor Usuario
    participant Front
    participant Backend
    participant AI
    participant BaseDeConocimiento
    participant bdv as Base de Datos Vectorial

    Usuario->>Front: Solicitud de procesamiento
    Front->>Backend: Envía solicitud al backend
    Backend->>AI: Solicitud a AI para procesar los datos
    AI->>BaseDeConocimiento: Consulta a la base de conocimiento
    BaseDeConocimiento->>bdv: Búsqueda vectorial en Pinecone
    bdv-->>BaseDeConocimiento: Resultados de la búsqueda
    BaseDeConocimiento-->>AI: Respuesta con información relevante
    AI-->>Backend: Respuesta con los resultados procesados
    Backend-->>Front: Devuelve la respuesta al Front
    Front-->>Usuario: Devuelve la respuesta al usuario

    
### Cómo Guardar

1. **Crea un archivo**: Abre tu editor de texto y crea un archivo nuevo llamado `diagrama_secuencia.md`.
2. **Escribe el contenido**: Copia el código de arriba y pégalo en el archivo.
3. **Guarda** el archivo.

### Visualización

- **En VSCode**: Puedes usar la extensión de Markdown para visualizar el diagrama.
- **En GitHub**: Al subir el archivo a un repositorio, GitHub renderizará automáticamente el diagrama.
- **En otras herramientas**: Asegúrate de que la herramienta que uses soporte diagramas Mermaid.

Con esto, deberías poder ver tu diagrama de secuencia correctamente en Markdown. Si necesitas más ayuda o ajustes, ¡dímelo!
