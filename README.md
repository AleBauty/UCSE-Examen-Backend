
# Examen Final: API CRUD de Trailers con Express y MongoDB 🎬

## Descripción del Proyecto 📋

En este examen final, deberás desarrollar una **API RESTful** usando **Express** y **MongoDB** para gestionar un catálogo de trailers de series y películas. La API permitirá realizar las operaciones **CRUD** (Crear, Leer, Actualizar, Eliminar) sobre una colección de trailers. 

Además del CRUD básico, se requerirán endpoints adicionales para filtrar resultados por género, buscar trailers por actor, y realizar búsquedas avanzadas por palabras clave.

> **Instrucciones**: Al finalizar, deberás completar este README.md con la documentación de cada endpoint implementado. Incluye la siguiente información:
> - Método HTTP (GET, POST, PUT, DELETE).
> - Ruta del endpoint.
> - Descripción de parámetros o query params.
> - Ejemplo del cuerpo de solicitud (si aplica).
> - Posibles respuestas en formato JSON.
> - Códigos de estado HTTP asociados.

## Entrega 📌

Deberás entregar una API backend documentada que maneje información sobre trailers almacenada en una base de datos MongoDB. La documentación debe estar en el archivo `README.md` del repositorio.

## Datos Proporcionados 📂

A continuación se provee un archivo `trailers.json` con datos de ejemplo de trailers, incluyendo:
- **id**: Identificador único del trailer.
- **poster**: URL de la imagen de portada.
- **titulo**: Título del trailer.
- **categoria**: Tipo de contenido (por ejemplo, "Serie" o "Película").
- **gen**: Género principal.
- **genero**: Lista de géneros.
- **busqueda**: Palabras clave para facilitar búsquedas.
- **resumen**: Breve descripción del trailer.
- **temporadas**: Número de temporadas (solo para series).
- **duracion**: Duración en minutos (solo para películas).
- **reparto**: Lista de actores y actrices destacados.
- **trailer**: URL del video del trailer.

## Modelo de Base de Datos 📊

Utiliza el archivo `trailers.json` para definir el modelo en MongoDB con **Mongoose**. Crea un modelo llamado `Trailer` que incluya los siguientes campos:

- **titulo**: Nombre del trailer (Serie o Película).
- **categoria**: Tipo de contenido (Serie o Película).
- **genero**: Lista de géneros relacionados (ej. "Drama", "Ficción").
- **reparto**: Lista de actores.
- **resumen**: Descripción breve de la trama.
- **trailer**: URL del trailer en video.

## Funcionalidades del CRUD 🚀

La API deberá incluir las siguientes operaciones básicas:

1. **Obtener todos los trailers**.
2. **Obtener un trailer por `id`**.
3. **Filtrar trailers** por género.
4. **Buscar trailers** por actor.
5. **Buscar trailers** por palabras clave (búsqueda avanzada).
6. **Agregar un nuevo trailer**.
7. **Actualizar un trailer existente**.
8. **Eliminar un trailer**.
9. **Manejo de Errores**.

### Rutas Adicionales 🔍

Para cumplir con los requisitos de funcionalidad avanzada, agrega los siguientes endpoints:

- Filtra trailers según uno o varios géneros.
- Filtra trailers por nombre de actor.
- Busca trailers según palabras clave, como el título o categoría.
- Devolver una lista de series que tienen más de X temporadas.

## Estructura del Repositorio 🗂️

```plaintext
/controllers
  - trailerController.js
/data
  - trailers.json
/README.md
/app.js
/config/
  - database.js
/models/
  - trailer.js
/routes/
  - trailerRoutes.js
```

### Descripción de Archivos 📝

- **/data**: Contiene el archivo `trailers.json` con los datos iniciales.
- **/README.md**: Archivo que documenta el proyecto y explica cómo ejecutarlo.
- **/app.js**: Archivo principal de la aplicación Express.
- **/config/database.js**: Configuración para conectar con MongoDB.
- **/models/**: Contiene el modelo `Trailer` de MongoDB.
- **/routes/**: Define las rutas de los endpoints CRUD.

## Instrucciones de Entrega 🚀

1. **Clona** el repositorio desde [aquí](https://github.com/FabioDrizZt/UCSE-Examen-Backend).
   ```bash
   git clone https://github.com/FabioDrizZt/UCSE-Examen-Backend.git
   ```
2. Desarrolla las funcionalidades requeridas en el repositorio clonado.
3. **Documenta** todos los endpoints en el archivo `README.md`.
4. **Sube** tus cambios y compártelos en el repositorio.
   ```bash
   git add .
   git commit -m "Implementación de funcionalidades y documentación"
   git push origin main
   ```
