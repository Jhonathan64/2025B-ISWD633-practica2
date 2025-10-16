# Redes
Las redes son un componente fundamental que permite la comunicación entre contenedores, así como la comunicación de los contenedores con el mundo exterior. 
![Imagen](redes.PNG)
- Bridge: Esta es la red por defecto en Docker. Permite la comunicación entre contenedores en el mismo host. Cada contenedor conectado a la red bridge tiene una IP propia en la subred de la red bridge.
    -  Brige por default: Cuando se ejecuta un contenedor, Docker crea automáticamente una red de tipo bridge por default. Esta red se utiliza para permitir la comunicación entre contenedores en el mismo host. Cada contenedor conectado a esta red obtiene su propia dirección IP en la subred de la red bridge.
    - Bridge creada por nosotros: Un usuario también puede crear sus propias redes de tipo bridge en Docker. Esto puede ser útil para organizar y segmentar los contenedores de una aplicación de manera más controlada. Al crear una red bridge personalizada, se puede especificar un rango de direcciones IP y otras configuraciones de red específicas. Los contenedores conectados a esta red utilizarán las direcciones IP de la subred definida por el usuario.
- Host: Con esta red, los contenedores comparten la red del host en lugar de tener su propia interfaz de red. Esto puede mejorar el rendimiento de red, pero los contenedores pueden entrar en conflicto con los puertos del host si intentan utilizar los mismos puertos.
- None: Con esta red, se deshabilita la configuración de red. Los contenedores que usan esta red tienen su propia red de loopback y no pueden comunicarse con otros contenedores a menos que se conecten explícitamente a una red.

### Crear una red de tipo bridge

```
docker network create <nombre red> -d bridge
```
<img width="821" height="60" alt="image" src="https://github.com/user-attachments/assets/2b75e99f-6b16-4327-84e6-041d6eb1f554" />

### Crear un contenedor vinculado a una red

```
docker run -d --name <nombre contenedor> --network <nombre red> <nombre imagen>
```
<img width="969" height="75" alt="image" src="https://github.com/user-attachments/assets/7b5c9af1-0bc3-4556-bc52-35888ca0895b" />

### Para saber a qué red está conectado un contenedor

```
docker inspect <nombre contenedor>
```
<img width="1113" height="547" alt="image" src="https://github.com/user-attachments/assets/4ddef5a2-8ae2-423a-98cd-113eb4143ff8" />

ó
```
docker network inspect <nombre red> 
```

### Vincular contenedor a una red
```
docker network connect <nombre red> <nombre contenedor>
```
<img width="628" height="55" alt="image" src="https://github.com/user-attachments/assets/fbe42a6a-c5a9-4b4e-9637-7f8e24fb4d91" />

### Para desvincular un contenedor de una red
```
docker network disconnect <nombre red> <nombre contenedor>
```
<img width="671" height="52" alt="image" src="https://github.com/user-attachments/assets/ba23f089-c5f8-4c6b-aebe-44d2addf3a49" />

### Para listar las redes existentes
```
docker network ls
```
<img width="561" height="173" alt="image" src="https://github.com/user-attachments/assets/80b1fb53-109a-48bb-9b40-5f8dd210aecb" />

### Crear los contenedores y las redes que se presentan en el esquema. Usar para todos los contenedores la imagen de nginx:alpine

![Imagen](esquema-ejercicio-redes.PNG)

# COLOCAR UNA CAPTURA DE LAS REDES EXISTENTES CREADAS
<img width="593" height="210" alt="image" src="https://github.com/user-attachments/assets/6b847841-4f42-44c0-bf09-4f343f6dc11d" />


# COLOCAR UNA(S) CAPTURAS(S) DE LOS CONTENEDORES CREADOS EN DONDE SE EVIDENCIE A QUÉ RED ESTÁN VINCULADOS
Contenedor 1
<img width="1393" height="577" alt="image" src="https://github.com/user-attachments/assets/076c7cb1-452f-4b0f-90dd-12db2e89a579" />
Contenedor 2
<img width="1370" height="660" alt="image" src="https://github.com/user-attachments/assets/3f9dc371-562a-4d62-ac1c-e8f96a575116" />
Contenedor 3
<img width="1323" height="725" alt="image" src="https://github.com/user-attachments/assets/2fdff35a-3e55-4ef2-bab1-18a0c0c2161b" />
Contenedor 4
<img width="1442" height="711" alt="image" src="https://github.com/user-attachments/assets/ef678a59-348b-40f0-be5d-d82651a4e795" />


### Para eliminar las redes creadas
```
docker network rm <nombre de la red>
```

