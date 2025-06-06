# 📚 Mis Recursos App

- Aplicación web para llevar un registro personalizado del progreso del usuario al ver series, películas y leer libros. Esta app permite organizar, clasificar y valorar cada uno de estos recursos a través de una interfaz que interactúa con una base de datos MongoDB.

## 🧩 Generalidades del Proyecto

- El objetivo de este proyecto es crear una plataforma donde los usuarios puedan registrar y gestionar los recursos de entretenimiento que consumen. Se proporciona soporte completo de operaciones CRUD, así como filtros y búsqueda para facilitar la navegación por el contenido registrado.

## ✨ Funcionalidades Implementadas

Tienes completamente la posibilidad de Crear un espacio con la informacion referente a una pelicula para poder llevar el registro de que has visto cuales estas viendo y cuales tienes pendientes y que tal te parecieron... tambien puedes eliminar actualizar y mostrar los datos de la forma en la que tu quieras

## 📦 Estructura de la Base de Datos (MongoDB)

```json
{
  "nombre": "Breaking Bad",
  "genero": "Drama",
  "plataforma": "Netflix",
  "estado": "Terminado",
  "formato": "Serie",
  "fecha_terminacion": "2024-08-15",
  "valoracion": 5,
  "resena": "Una de las mejores series que he visto, con un desarrollo de personajes impresionante."
}
```
## 📁 Archivos JSON de Datos

- contiene un archivo recursos.json que tiene almenos 50 datos los cuales cuenta con todos los parametros

# COMO USAR?

## 🧪 Comandos de Creación y Carga de datos

```json
use MisRecursosApp
db.Recursos.insertOne({
        "nombre": "Demon Slayer",
        "genero": "Accion",
        "plataforma": "crunchyroll",
        "estado": "En progreso",
        "formato": "serie",
        "fecha_terminacion": "2024-04-01",
        "valoracion_final": 3,
        "reseña_personal": "Simplemente El mejor anime de los timepo"
})
```
## 🧪 Comando para mostrar por estado

```json
use MisRecursos
db.Recursos.find({estado: "Pendiente"})

use MisRecursos
db.Recursos.find({estado: "En progreso"})

use MisRecursos
db.Recursos.find({estado: "Terminado"})
```

## 🧪 Comando para mostrar por Formato

```json
use MisRecursos
db.Recursos.find({formato: "serie"})

use MisRecursos
db.Recursos.find({formato: "pelicula"})

use MisRecursos
db.Recursos.find({formato: "libro"})
```

## 🧪 Comando para mostrar por plataforma

```json
use MisRecursos
db.Recursos.find({plataforma: "Netflix"})

use MisRecursos
db.Recursos.find({plataforma: "Disney+"})

use MisRecursos
db.Recursos.find({plataforma: "Star+"})
```

## 🧪 Comando para editar datos

```json
use MisRecursos
db.Recursos.updateOne({nombre: "Demon Slayer"},
{
    $set: {
        nombre: "Kimetsu No Yaiba"
    }
})
```

## 🧪 Comando para eliminar datos

```json
use MisRecursos
db.Recursos.deleteOne({nombre: "Demon Slayer"})
```

## tabla de peliculas disponibles

| Nombre                     | Género          | Plataforma   | Formato  |
|----------------------------|-----------------|--------------|----------|
| BoJack Horseman            | Animación       | Netflix      | serie    |
| Narcos                     | Crimen          | Netflix      | serie    |
| Matrix                     | Ciencia Ficción | HBO Max      | pelicula |
| Black Mirror               | Distopía        | Netflix      | serie    |
| Fight Club                 | Psicológico     | Star+        | pelicula |
| Merlí                      | Drama           | Netflix      | serie    |
| La Divina Comedia          | Religioso       |              | libro    |
| The Batman                 | Acción          | HBO Max      | pelicula |
| Los Juegos del Hambre      | Aventura        |              | libro    |
| House of the Dragon        | Fantasía        | HBO Max      | serie    |
| Better Call Saul           | Crimen          | Netflix      | serie    |
| Coraline                   | Fantasía        | Netflix      | pelicula |
| Yo Robot                   | Ciencia Ficción | Star+        | pelicula |
| Arcane                     | Acción          | Netflix      | serie    |
| Sherlock                   | Misterio        | Netflix      | serie    |
| Big Fish                   | Fantasía        | Amazon Prime | pelicula |
| Mindhunter                 | Psicológico     | Netflix      | serie    |
| Titanic                    | Romance         | Star+        | pelicula |
| El Perfume                 | Misterio        |              | libro    |
| The Boys                   | Superhéroes     | Amazon Prime | serie    |
| Berserk                    | Fantasía oscura |              | libro    |
| Shrek 2                    | Animación       | Netflix      | película |
| Peaky Blinders             | Drama           | Netflix      | serie    |
| El Club de la Pelea        | Psicológico     |              | libro    |
| Monster                    | Thriller        | crunchyroll  | pelicula |
| Los Simpson                | Comedia         | Star+        | serie    |
| El Código Da Vinci         | Thriller        |              | libro    |
| Spider-Man                 | Animación       | Netflix      | película |
| Parásitos                  | Thriller        | Amazon Prime | película |
| Breaking Bad               | Drama           | Netflix      | serie    |
| El Padrino                 | Crimen          | Amazon Prime | película |
| Stranger Things            | Suspenso        | Netflix      | serie    |
| Dune                       | Ciencia Ficción | HBO Max      | película |
| 1984                       | Distopía        |              | libro    |
| The Office                 | Comedia         | Peacock      | serie    |
| Interestelar               | Ciencia Ficción | HBO Max      | película |
| El Principito              | Filosofía       |              | libro    |
| La Casa de Papel           | Acción          | Netflix      | serie    |
| The Mandalorian            | Aventura        | Disney+      | serie    |
| Harry Potter               | Fantasía        |              | libro    |
| Avatar: El Camino del Agua | Ciencia Ficción | Disney+      | película |
| Rick and Morty | Animación | HBO Max         | Netflix      | serie    |
| La Odisea                  | Épico           |              | libro    |
| Dark                       | Misterio        | Netflix      | serie    |
| Pulp Fiction               | Crimen          | Amazon Prime | película |
| Chernobyl                  | Historia        | HBO Max      | serie    |
| El Señor de los Anillos    | Fantasía        | Libro        | libro    |
| The Social Network         | Biografía       | Netflix      | película |
| El Juego del Calamar       | Thriller        | Netflix      | serie    |
| Demon Slayer               | Accion          | crunchyroll  | serie    |

## tecnologia usada

MongoDB Base de datos NoSQL

## Trabajito echo por

Manuel Meneses






