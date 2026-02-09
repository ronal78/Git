
# Mi pagina web

## Ronaldo Nuñez Castro
### Descripcion del proyecto
### # Mi pagina web – Ronaldo Nuñez Castro

Este proyecto consiste en un **pagina web dinámico**, desarrollado con **HTML, CSS y JavaScript**, cuyo contenido se carga de manera automática desde un archivo **JSON**. El objetivo es mostrar información personal, académica y profesional de forma estructurada, moderna y fácil de mantener.

---

## 📌 Estructura general del proyecto

El sitio está compuesto por:
- Un archivo HTML principal
- Hojas de estilo CSS externas
- Un archivo `data.json` que contiene toda la información del CV
- JavaScript integrado para cargar y mostrar los datos dinámicamente

---

## 🧱 Estructura del HTML

### 1. Declaración y configuración inicial
El documento utiliza el estándar **HTML5** e incluye:
- Codificación UTF-8 para soportar acentos y caracteres especiales
- Meta viewport para diseño responsive
- Idioma configurado en español (`lang="es"`)

```html
<!DOCTYPE html>
<html lang="es">
```

## Encabezado (Header)
El encabezado contiene:
- Un logo con el nombre del sitio
- Un menu de navegacion responsive
- Enlaces a las diferentes secciones del sitio:
    - Inicio
    - presentacion
    - Curriculum Vitae

## Secciones principales del CV
El contenido de curriculum está divido en secciones bien definidas:
- Experencias laborales
- Educacion
- Proyectos personales
- Habilidades tecnicas
- Certificaciones
Cada seccion tiene un contenedor propio y un div con un id especifico donde se insertan los datos dinamicamente.
## Funcionamiento del JavaScript
- Carga dinamica de datos con Fetch 
El archivo utiliza la funcion fetch()para obtener la informacion desde el archivo data.json

Esto permite separar los datos del diseño y facilita futuras actualizaciones del CV sin modificar el HTML.

- Procesamiento del archivo JSON 
        
    Una vez cargado el JSON:
    - Se recorren los arreglos usando forEach
    - Se generan tarjetas(div.card) dinamicamente
    - Se insertan los datos en el HTML usando innerHTML

Cada seccion del CV se construye a partir de su perspectiva informacion en el JSON.

- Manejo de lista y arreglos

para las experiencias laborales:

- Se utiliza map() y join() para crear listas (ul) de actividades de forma dinamica.
Tambien se valida si ciertos campos son arreglos usando:
        
        -Array.isArray()    

- Manejo de Errores
Si ocurre un problema al cargar el archivo data.json, el error se muestra en la consola del navegador para facilitar la depuracion.

        .catch(err => console.error("Error cargando el JSON:", err));

## Archivo data.json
El archivo data.json contiene toda la informacion del curriculum, organizada en:

-  Experiencias laborales
- Educacion 
- Proyectos personales
- Habilidades tecnicas 
- Certificaciones

Esto permite que el contenido sea facilmente editable, reutilizable y escalable.