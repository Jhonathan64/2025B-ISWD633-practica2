# Variables de Entorno
### ¿Qué son las variables de entorno?
# COMPLETAR
Las variables de entorno son valores dinámicos con nombre, definidos en el sistema operativo, que proporcionan información y configuraciones a los procesos en ejecución. Permiten a las aplicaciones acceder a datos como la ruta a un directorio, el nombre del usuario o la configuración de una base de datos, sin tener que codificar estos valores directamente en el programa. Son externas, es decir, su valor se configura fuera del código, lo que permite cambiar la configuración de una aplicación sin modificar su código. 
### Para crear un contenedor con variables de entorno

```
docker run -d --name <nombre contenedor> -e <nombre variable1>=<valor1> -e <nombre variable2>=<valor2>
```

### Crear un contenedor a partir de la imagen de nginx:alpine con las siguientes variables de entorno: username y role. Para la variable de entorno rol asignar el valor admin.
<img width="1535" height="313" alt="image" src="https://github.com/user-attachments/assets/d5c33376-8462-4337-a53e-cfe8f5759bbd" />

# COMPLETAR

# CAPTURA CON LA COMPROBACIÓN DE LA CREACIÓN DE LAS VARIABLES DE ENTORNO DEL CONTENEDOR ANTERIOR
<img width="1486" height="146" alt="image" src="https://github.com/user-attachments/assets/d2974645-b0e8-4d57-8011-bb9e614d301e" />

### Crear un contenedor con la imagen de mysql, mapear todos los puertos
# COMPLETAR
<img width="1159" height="395" alt="image" src="https://github.com/user-attachments/assets/4c23a283-b3b9-4f66-9d5a-639eeac1db21" />
<img width="1473" height="206" alt="image" src="https://github.com/user-attachments/assets/bb50639c-e6d4-43af-95ac-655e91ed3106" />


### ¿El contenedor se está ejecutando?
# COMPLETAR
Ambos contenedores que se crearon anteriormente se estan ejecutando de manera correcta, como nos muestra en la imagen anterior tenemos que el estado es Up, lo que nos dice que esta activo.
### Identificar el problema
No hubo ningún problema 
# COMPLETAR

### Para crear un contenedor con variables de entorno especificadas
- Portabilidad: Las aplicaciones se vuelven más portátiles y pueden ser desplegadas en diferentes entornos (desarrollo, pruebas, producción) simplemente cambiando el archivo de variables de entorno.
- Centralización: Todas las configuraciones importantes se centralizan en un solo lugar, lo que facilita la gestión y auditoría de las configuraciones.
- Consistencia: Asegura que todos los miembros del equipo de desarrollo o los entornos de despliegue utilicen las mismas configuraciones.
- Evitar Exposición en el Código: Mantener variables sensibles como contraseñas, claves API, y tokens fuera del código fuente reduce el riesgo de exposición accidental a través del control de versiones.
- Control de Acceso: Los archivos de variables de entorno pueden ser gestionados con permisos específicos, limitando quién puede ver o modificar la configuración sensible.

### ¿Qué bases de datos existen en el contenedor creado?
# COMPLETAR
Solo se inició el servidor MySQL y se estableció la contraseña de root. Como no se incluyeron variables de entorno adicionales (-e) como MYSQL_DATABASE o MYSQL_USER para crear bases de datos personalizadas, el contenedor contiene únicamente las siguientes bases de datos internas necesarias para el funcionamiento de MySQL:

information_schema
mysql
performance_schema
sys

<img width="1051" height="296" alt="image" src="https://github.com/user-attachments/assets/7e26d662-a6ab-4cf2-b98f-d6241b9ddca3" />

