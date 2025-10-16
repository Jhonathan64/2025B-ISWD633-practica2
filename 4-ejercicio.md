## Esquema para el ejercicio
![Imagen](esquema-4-ejercicio.PNG)

### Crear la red
# COMPLETAR
<img width="828" height="64" alt="image" src="https://github.com/user-attachments/assets/1ec40cd1-875d-485e-8479-cfa04eee3cb5" />

### Crear el contenedor mysql a partir de la imagen mysql:8, configurar las variables de entorno necesarias
# COMPLETAR
<img width="1454" height="85" alt="image" src="https://github.com/user-attachments/assets/4a35e4e6-3652-4ca2-bec2-de06293e9caa" />

### Crear el contenedor wordpress a partir de la imagen: wordpress, configurar las variables de entorno necesarias
# COMPLETAR
<img width="1453" height="88" alt="image" src="https://github.com/user-attachments/assets/8e514645-bc3c-4592-acef-74329139524e" />

De acuerdo con el trabajo realizado, en el esquema del ejercicio el puerto a es **(completar con el valor)**

Ingresar desde el navegador al wordpress y finalizar la configuración de instalación.
# COLOCAR UNA CAPTURA DE LA CONFIGURACIÓN

Desde el panel de admin: cambiar el tema y crear una nueva publicación.
Ingresar a: http://localhost:9300/ 
recordar que a es el puerto que usó para el mapeo con wordpress
# COLOCAR UNA CAPTURA DEL SITO EN DONDE SEA VISIBLE LA PUBLICACIÓN.
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/3d796c90-f8ff-4ba0-acbb-3310e1d4fa41" />

### Eliminar el contenedor wordpress
# COMPLETAR
<img width="536" height="66" alt="image" src="https://github.com/user-attachments/assets/af207913-8bfc-4d3a-a179-71489acce0f8" />

### Crear nuevamente el contenedor wordpress
Ingresar a: http://localhost:9300/ 
recordar que a es el puerto que usó para el mapeo con wordpress
<img width="1450" height="86" alt="image" src="https://github.com/user-attachments/assets/0d17f0e9-3433-4aaf-9291-afe45db338e9" />

### ¿Qué ha sucedido, qué puede observar?
# COMPLETAR
Lo que se observa es que el sitio web de WordPress mantiene exactamente el mismo estado (mismo tema, misma publicación, mismo usuario) que tenía antes de eliminar y recrear el contenedor.

