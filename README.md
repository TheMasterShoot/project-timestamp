# Timestamp Microservice

This is the boilerplate code for the Timestamp Microservice project. Instructions for building your project can be found at https://www.freecodecamp.org/learn/apis-and-microservices/apis-and-microservices-projects/timestamp-microservice

Este proyecto es una implementación en Node.js con Express de un microservicio de marcas de tiempo (timestamp), parte del curriculum de APIs y microservicios de FreeCodeCamp.

La API acepta fechas como parámetros de URL y devuelve una representación en formato Unix timestamp y UTC. Si no se proporciona una fecha, retorna la fecha y hora actual.

---

## Tecnologías utilizadas

- Node.js  
- Express  
- CORS  

---

## Instalación

1. Clona el repositorio:

```bash
git clone https://github.com/tu-usuario/nombre-del-repo.git
cd nombre-del-repo
```

2. Instala las dependencias:

```bash
npm install
```

3. Crea un archivo `.env` si deseas especificar un puerto personalizado:

```
PORT=3000
```

4. Inicia el servidor:

```bash
npm start
```

El servidor estará disponible en `http://localhost:3000`.

---

### Pruebas

1. Se proporciona un proyecto propio, no la URL de ejemplo.  
2. Una solicitud a `/api/:date?` con una fecha válida devuelve un objeto JSON con una clave `unix` que es un timestamp Unix en milisegundos.  
3. Una solicitud a `/api/:date?` con una fecha válida devuelve un objeto JSON con una clave `utc` que es una cadena con el formato: `Thu, 01 Jan 1970 00:00:00 GMT`.  
4. Una solicitud a `/api/1451001600000` devuelve `{ unix: 1451001600000, utc: "Fri, 25 Dec 2015 00:00:00 GMT" }`.  
5. El proyecto maneja fechas que puedan ser analizadas exitosamente por `new Date(date_string)`.  
6. Si el string de fecha es inválido, la API retorna `{ error : "Invalid Date" }`.  
7. Si no se pasa parámetro de fecha, retorna la hora actual con `unix` y `utc`.  
8. Asume que las fechas se analizan con `new Date()` como fechas en GMT (sin conversión de zona horaria).  