# [ - ] API WHATSAPP MULTIDEVICE [2024]
 RESTful API service with multi device support just `download`, `install`, and `start` using, `simple` as that.

## Comenzando 🚀

---

Estas instrucciones te permitirán obtener una copia del proyecto en funcionamiento en tu máquina local para propósitos
de desarrollo y pruebas.

1.- Clona el repositorio.

| Comando | Descripción |
| --- | --- |
| HTTP | `https://github.com/mb3mx/whatsapp-api-multidevice.git` |


2.- Importa el proyecto en Visual Code.

## Pre-requisitos 📋
 
---

| Nombre | Version |Url |
|   :---:   |   :---:   |   :---:   |
|   Node    |   >16.0   | [https://nodejs.org/en] |
|   Baileys |   >16.0   | [https://github.com/WhiskeySockets/Baileys] |
|   Express |   >16.0   | [https://github.com/expressjs/express] |


## Instalación 🔧 y despliegue 📦

### Ejecucion Local

* 1.- Ubicarse en la carpeta raiz `whatsapp-api-multidevice`
* 2.- Ejecutar el comando `npm install`
* 3.- Ejecutar el comando `npm dev`

### Ejecucion Docker

* 1.- Ubicarse en la carpeta raiz `whatsapp-api-multidevice`
* 2.- Ejecutar el comando `docker compose up -d`
  
 

### Configuracion de la base datos (Save Session)
Nota: para la configuracion de la base de datos cree un cuenta en alltras (mongo)
una vez crear el usuario y el acceso de ip remota , haga click en probar
 conexion en compass copie la url generada en el archivo .env ,como el ejemplo de abajo 
```
MONGODB_ENABLED=true
MONGODB_URL=mongodb+srv://root:publica@bcoding.sdxe4je.mongodb.net/
```

## Usage

1. `DEVELOPMENT:` Execute `npm dev`
2. `PRODUCTION:` Execute `npm start`




Allowed values:

-   `connection` - receive all connection events
-   `connection:open` - receive open connection events
-   `connection:close` - receive close connection events
-   `presense` - receive presence events
-   `messages` - receive all messages event
-   `call` - receive all events related to calls
-   `call:terminate` - receive call terminate events
-   `call:offer` - receive call terminate event
-   `groups` - receive all events related to groups
-   `group_participants` - receive all events related to group participants

You can also use the Baileys event format example: `messages.upsert`



### Using Key

Save the value of the `key` from response. Then use this value to call all the routes.
### Generar una instancia 
Para este ejemplo `terraprime` es el nombre de la instaciia
GET http://localhost:3333/instance/init?key=romeo2

### una vez generada la instacia toca escaner el QR , la api de que crear una instancia muestras api para el acceso a la siguiente api
Para este ejemplo `terraprime` es el nombre de instancia(con esta api accedemos al qr generado de esta instancia)
GET http://localhost:3333/instance/qr?key=romeo2

### Enviar mensaje type POST
Parametro key indica de que instancia queremos enviar un mensaje  
POST http://localhost:3333/message/contact?key=romeo2
{   
   "number":"67511387",
   "message":"Its Gread"
}
### Enviar mensaje typo GET
Parametro key indica de que instancia queremos enviar un mensaje  (example)
GET
http://localhost:3333/message/ContactTypeGet?key=romeo2&number=67500111&message=hola

### Routes addcionales 
Muestra una lista de instancia 
GET http://localhost:3333/instance/list




