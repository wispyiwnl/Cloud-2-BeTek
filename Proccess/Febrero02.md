Me conecto mediante `ssh santiagow3b@35.175.199.96` 

`santiagow3b` es el user y `35.175.199.96` es la ip del server

y luego coloco la password

![coneccion](../media/coneccion-server.png)



Creacion de volume

![creacion volumen](../media/creacion-volumen.png)

Que el volume este correctamente en la misma `Availability Zone` este en `use1-az4 (us-east-1c)`

![Availability Zone](../media/availability-zone.png)


Para cuando hagamos el `Attach volume`, atachemos el volume a una `instance` correctamente gracias a que estoy en la misma `Availability Zone`

![Attach volume](../media/attach-volume.png)

![instance](../media/instance.png)

Atachamos correctamente

![successfully-attached](../media/successfully-attached.png)

Se monta el disco que se seleccion al atachar el volume con la instancia, mediante linux ssh con:

```bash
sudo mkdir /santiagow3b

sudo mount /dev/sdd/santiagow3b

df -h
```

y ahi ya aparecen todos los discos

![disco montado](../media/disco-montado.png)

![disco montado](../media/lsblk.png)


Y doy todos los permisos con `sudo chmod 777 /santiagow3b` y creo un log de prueba


![log creado](../media/log-prueba.png)