Clasificacion HTTP:
Safe o seguro: Es un metodo de "solo lectura". Algunos de los metodos seguros son: OPTIONS, GET O HEAD. Algunos metodos seguros tambien son 'idempotent'. Los metodos safe no realizan cambios o cargas innecesarias en el servidor.
Idempotent:Al realizar una operacion muchas veces obteniendo el mismo resultado dejando el servidor en el mismo estado. Los metodos GET, HEAD, PUT Y DELETE forman parte de este grupo.

Peticiones HTTP:
- GET: recupera cualquier informacion (en forma de entidad), recupera datos. El recurso se ha obtenido y se transmite en el cuerpo del mensaje.
- OPTIONS: solicitud de informacion sobre las opciones de comunicacion disponible en el canal de solicitud/respuesta. Se usa para describir las opciones de comunicacion en el recurso destino.
	Los encabezados de entidad están en el cuerpo del mensaje.
- HEAD: es similar al 'GET' pero en este caso el servidor responde con lineas y headers, pero no con el body de la respuesta.
- PUT: es usado para solicitar que el servidor almacene el cuerpo de la entidad en una ubicación específica dada por el URL. El recurso que describe el resultado de la acción se transmite en el cuerpo del mensaje.
- POST:es usado cuando se requiere enviar información al servidor como, por ejemplo, un archivo de actualización, información de formulario, etc. Se usa cuando se necesita enviar una entidad para algún recurso determinado. No es un metodo idempotente como 'PUT'.
	El recurso que describe el resultado de la acción se transmite en el cuerpo del mensaje.
- DELETE: este metodo elimina archivos en la ubicacion dada mediante la url.
- CONNECT: establece la conexion de red con un servidor web mediante HTTP.
- TRACE: se utiliza para realizar pruebas de eco (de retornos) de mensajes en el camino que existe hacia un recurso determinado. Usado para depuracion y desarrollo. El cuerpo del mensaje contiene el mensaje de solicitud recibido por el servidor.

Las respuestas se agrupan en cinco clases. Respuestas HTTP:

1. Respuestas informativas (100–199):
	- CONTINUE:Indica que todo hasta el momento va bien.
	- SWITCHING PROTOCOL: indica que el servidor acepta el cambio de protocolo propuesto.
	- PROCESSING: indica que el servidor ha recibido la respuestay la está procesando.
	- EARLY HINTS:Este código de estado está pensado principalmente para ser usado con el encabezado Link, permitiendo que el agente de usuario empiece a pre-cargar recursos mientras el servidor prepara una respuesta.

2. Respuestas satisfactorias (200–299):
	- OK: la solicitud fue exitosa.
	- CREATED: La solicitud ha tenido éxito y se ha creado un nuevo recurso como resultado de ello.
	- ACCEPTED:La solicitud se ha recibido, pero aún no se ha actuado. 
	- NO CONTENT: La petición se ha completado con éxito pero su respuesta no tiene ningún contenido, aunque los encabezados pueden ser útiles.
	- RESET CONTENT: La petición se ha completado con éxito, pero su respuesta no tiene contenidos y el usuario tiene que inicializar la página desde la que se realizó la petición,

3. Redirecciones (300–399):
	- FOUND:Este código de respuesta significa que el recurso de la URI solicitada ha sido cambiado temporalmente.
	- NOT MODIFIED: Le indica al cliente que la respuesta no ha sido modificada. Entonces, el cliente puede continuar usando la misma versión almacenada en su caché.

4. Errores de los clientes (400–499):
	- BAD REQUEST: Esta respuesta significa que el servidor no pudo interpretar la solicitud dada una sintaxis inválida.
	- FORBIDDEN: El cliente no posee los permisos necesarios para cierto contenido, por lo que el servidor está rechazando otorgar una respuesta apropiada.
	- NOT FOUND: El servidor no pudo encontrar el contenido solicitado.

5. Errores de los servidores (500–599):
	- INTERNAL SERVER ERROR: El servidor ha encontrado una situación que no sabe cómo manejarla.
	- BAD GATEWAY: significa que el servidor mientras trabaja como una puerta de enlace para obtener una respuesta necesaria para manejar la petición, obtuvo una respuesta inválida.
	