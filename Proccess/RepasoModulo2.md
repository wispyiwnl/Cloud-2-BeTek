## 1. Incidente la aplicación está lenta

- ¿Qué revisarán primero? **Respuesta:** Mirar el CloudWatch, revisar la arquitectura de la app, revisar capacidades.
- ¿Qué servicio AWS les ayuda a identificar el problema? **Respuesta:** CloudWatch
- ¿Qué componente podría estar ocasionado lentitud? **Respuesta:** CPU de la instancia por falta de capacidad. Como buena práctica se recomienda aplicar un grupo de auto scaling con load balancer.


## 2. Incidente la base de datos está lenta

Después de que aumentaron los pedidos, la base de datos responde lento.
Algunas consultas SQL tardan demasiado.

- ¿Qué tipo de base de datos creen que se está usando? **Respuesta:** RDS Base de datos relacional.
- ¿Qué revisarán? **Respuesta:** Capacidad de recursos, cantidad de conexiones.
- ¿En qué casos podría seguir siendo una BD relacional y en qué casos podría
pensarse en NoSQL, Compara entre RDS - Aurora y DynamoDB? **Respuesta:** **_NoSQL:_** Correos de noticias o suscripciones a boletines de promoción

**_RDS:_** Disponibilidad en una 1 sola AZ SQL
**_Aurora:_** De alta disponibilidad SQL 
**_Dynamo:_** Relacionales NoSQL


## 3. Incidente credenciales expuestas
Un desarrollador dejó el usuario y contraseña de la base de datos dentro del
código de la aplicación.

- ¿Qué está mal? **Respuesta:** Imprimir valores sensibles.
- ¿Qué servicio usarían para solucionarlo? **Respuesta:** Secret manager y IAM para dar permisos sobre el secreto que solo lo use quien deba usarlo.
- ¿Con qué servicio cifrarán ? **Respuesta:** KMS


## 4. Incidente Borraron un recursos 
Alguien borro un grupo de seguridad importante para funcionamiento de la
aplicación

- ¿Qué servicio usarían para auditar? **Respuesta:** CloudTrail
- ¿Qué tipo de información esperarían encontrar? **Respuesta:** La información en formato JSON: hora desde donde se origino el evento, incluye el usuario o la llave que uso


## 5. Incidente Archivos mal almacenados
La aplicación guarda imágenes de productos dentro del mismo servidor
donde corre la aplicación.

- ¿Qué problema ven? **Respuesta:** Que se pueda borrar el EBS si se recrea una instancia y se pierde el EBS y solo 1 instancia puede ver el contenido alternativo EFS
- ¿Dónde debería guardarse ese tipo de archivos? **Respuesta:** S3
- ¿Qué riesgo hay si la app escala o el servidor falla? **Respuesta:** Puede ocurrir que se borre el EBS y con ello la información de la aplicación
