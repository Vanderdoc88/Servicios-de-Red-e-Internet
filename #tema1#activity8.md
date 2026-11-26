¿Como configurar virtual host de de Apache en Ubuntu?

Paso 1: Crear estructura de directorios

<img width="782" height="125" alt="image" src="https://github.com/user-attachments/assets/d078f074-dd19-41bc-852e-879bb408e257" />

Paso 2: Otorgar permisos

<img width="857" height="137" alt="image" src="https://github.com/user-attachments/assets/da441aa5-10bd-420d-9620-16904739376a" />

Paso 3: Crear una página de prueba para cada virtual host

<img width="799" height="97" alt="image" src="https://github.com/user-attachments/assets/2b721303-cc81-4dd8-816c-06235d8ce77e" />

Abrimos el siguiente archivo para editarlo

<img width="894" height="210" alt="image" src="https://github.com/user-attachments/assets/9a9fe6f3-e6c4-4bc4-9aa2-17f607182d13" />

Escribimos lo siguiente, guardamos y nos salimos

<img width="1066" height="111" alt="image" src="https://github.com/user-attachments/assets/f3893dce-1ea0-49cc-a5b5-d67e9890b02a" />

Copiamos el contenido del anterior archivo en el otro fichero que creamos

<img width="806" height="98" alt="image" src="https://github.com/user-attachments/assets/31e39d42-f6e0-45fc-b42f-e733607e665d" />

Luego abrimos el archivo en el que hemos copiado todo el contenido para hacer algunas modificaciones

<img width="900" height="223" alt="image" src="https://github.com/user-attachments/assets/49692a2a-50b5-48d5-9203-2644f53580af" />

Modificamos el nombre del texto para que aparezca el titulo de dicho archivo, nos salimos y guardamos

Paso 4: Crear nuevos archivos virtual host
Crear el archivo virtual host

<img width="1022" height="144" alt="image" src="https://github.com/user-attachments/assets/18e4021c-da88-406b-9337-43c9bc361d01" />

Copiamos el contenido del archivo para el primer dominio

<img width="849" height="96" alt="image" src="https://github.com/user-attachments/assets/3189208c-8129-473b-9967-ed6ecde2fc0e" />

Abrimos el archivo

<img width="903" height="524" alt="image" src="https://github.com/user-attachments/assets/c066eb68-857e-43b7-ba48-f696db0e2b2c" />

Tiene que verse así el archivo una vez hayamos hecho los cambios, lo que he resaltado en amarillo es lo que tienes que editar, luego nos salimos y guardamos

Copiar el primer archivo Virtual Host y cambiarlo para el segundo dominio 

<img width="1069" height="141" alt="image" src="https://github.com/user-attachments/assets/398eaec8-f9ff-478b-a4a4-127f9bf15226" />

Lo copiamos

<img width="843" height="97" alt="image" src="https://github.com/user-attachments/assets/0802eb52-eac7-468d-bf34-ecd8a3a7262f" />

Lo abrimos

<img width="903" height="529" alt="image" src="https://github.com/user-attachments/assets/cd478c87-6996-4cd0-b7b9-6ebe18f90f82" />

Y modificamos lo siguiente para el segundo dominio, de tal forma que quede asi, luego guardamos y cerramos

Paso 5: Habilita los nuevos archivos virtual host

<img width="1258" height="331" alt="image" src="https://github.com/user-attachments/assets/b138a7e4-513a-43b8-a53c-2f6658d495e1" />

Los habilitamos con la herramienta a2ensite, luego, reiniciamos el servicio apache para que los cambios surgan efecto

Paso 6: Configura archivos locales

<img width="750" height="93" alt="image" src="https://github.com/user-attachments/assets/e2161d9d-213c-49b2-baef-ec92c3817000" />

Vamos a meternos en el archivo local para editarlo

<img width="890" height="265" alt="image" src="https://github.com/user-attachments/assets/376f8c41-5acf-4955-803b-3e68c59a7991" />

Agregamos las 2 siguientes lineas al archivo, guardamos y nos salimos

Paso 7: Prueba tus resultados

<img width="1382" height="181" alt="image" src="https://github.com/user-attachments/assets/cc8e65b5-7518-4c85-aed0-af9620e72bdf" />
<img width="1377" height="181" alt="image" src="https://github.com/user-attachments/assets/f5edd275-5c03-4cb0-a43b-fab4337521e6" />

Al escribir en el navegador el nombre de los dominios, nos aparece que están activos


