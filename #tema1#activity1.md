# Cómo instalar la pila Linux, Apache, MySQL y PHP (LAMP) en Ubuntu 20.04

Comenzamos
## Paso 1: Instalar Apache y actualizar el firewall

<img width="1616" height="744" alt="image" src="https://github.com/user-attachments/assets/4aca5964-2af9-4769-9f82-aace745c56ae" />

Vamos a comenzar actualizando la máquina

<img width="1619" height="745" alt="image" src="https://github.com/user-attachments/assets/3b3689ab-68b5-4655-9a33-1a851a8ffaad" />

Y luego instalamos apache

<img width="1617" height="737" alt="image" src="https://github.com/user-attachments/assets/d6cfdf5a-c0a2-45e2-8a7c-e41967902633" />

Instalado, con el comando de la captura anterior, podemos ver todos los perfiles de aplicaciones ufw instalados

<img width="624" height="219" alt="image" src="https://github.com/user-attachments/assets/556707e2-c21a-4f0e-824b-e47c6bc9e649" />

Vamos a irnos solamente al puerto 80 (el de apache) para permitir el tráfico por ahi

<img width="1610" height="747" alt="image" src="https://github.com/user-attachments/assets/cbd30688-ea10-44d8-a05a-5b8fafbde7dc" />

He comprobado que mi servidor esta correctamente instalado accediendo a el desde el navegador localmente, puedo acceder correctamente al servidor desde mi firewall

<img width="708" height="334" alt="image" src="https://github.com/user-attachments/assets/69cc9975-afd9-4fdb-a41f-3002d47647d2" />

He instalado el comando curl, y he comprobado la IP publica de mi servidor

## Paso 2: Instalar MySQL

<img width="1070" height="96" alt="image" src="https://github.com/user-attachments/assets/02cc8ab4-7bae-42af-b850-017a29cae260" />

Comando para instalar MySQL

<img width="1039" height="659" alt="image" src="https://github.com/user-attachments/assets/6674961f-67f6-4a7f-bb29-39fac6a91dd4" />

Instalado

<img width="606" height="34" alt="image" src="https://github.com/user-attachments/assets/0c5db196-b152-46dd-b866-70f57fb3cb84" />

Y seguidamente instalamos unas configuraciones de seguridad para el MySQL

<img width="828" height="528" alt="image" src="https://github.com/user-attachments/assets/72eb8220-fee4-4e03-8bd3-9ed35b3e5ad3" />

En las flechitas aparece lo que tenemos que introducir en las preguntas que nos va haciendo el instalador

<img width="712" height="446" alt="image" src="https://github.com/user-attachments/assets/0bd9870a-7350-42c3-8771-87db539f01fb" />

Y esto

<img width="541" height="248" alt="image" src="https://github.com/user-attachments/assets/93ce93a1-1e64-4d0d-b5e7-f4adda2295f9" />

Luego, comprobé que podía iniciar sesión en myslq, y luego me sali con el comando exit

## Paso3: Instalar PHP

<img width="1606" height="744" alt="image" src="https://github.com/user-attachments/assets/701b09e3-d068-414f-ac4a-6ec76021806d" />

Instalamos PHP con el siguiente comando

<img width="681" height="113" alt="image" src="https://github.com/user-attachments/assets/4898ab42-ac47-49bb-a100-f82b41a13be6" />

Y con este comando comprobamos la versión

## Paso4: Crear un host virtual para su sitio web

<img width="618" height="40" alt="image" src="https://github.com/user-attachments/assets/d64f6201-7c33-4f7c-86d2-a559c184df05" />

Creo el directorio "Yourdomain" en la siguiente ruta

<img width="715" height="47" alt="image" src="https://github.com/user-attachments/assets/7776ec38-fd5b-484b-8455-a2f09053ac71" />

Y lo asigno a mi usuario con $USER

<img width="815" height="63" alt="image" src="https://github.com/user-attachments/assets/21c1df08-e2c3-42c9-98cc-55df96bdd0ce" />

Una vez hecho esto, se crea un fichero de configuración nuevo al que debemos acceder

<img width="1060" height="666" alt="image" src="https://github.com/user-attachments/assets/5e54fb93-03f7-4b18-8391-0dc1b7a2edbf" />

Escribimos lo siguiente en el fichero y lo guardamos

<img width="591" height="88" alt="image" src="https://github.com/user-attachments/assets/cd57e821-bef1-455f-a550-ed1449604f2f" />

Ahora podemos habilitar un nuevo host virtual con a2ensite

<img width="606" height="80" alt="image" src="https://github.com/user-attachments/assets/27051d53-7e59-4469-aee1-91eee725c66b" />

Con el siguiente comando desabilitámos el sitio web predeterminado de Apache

<img width="1003" height="77" alt="image" src="https://github.com/user-attachments/assets/22179ebe-f244-459c-85a4-a7eb3784e6cc" />

Con el siguiente comando comprobamos si hay algún error de sintaxis, tenia un error ya que en el nano no había cerrado bien el <virtualhost><virtualhost>, pero lo repare

<img width="783" height="132" alt="image" src="https://github.com/user-attachments/assets/d9e396cd-4ca0-417b-8062-b5df390aa0bd" />

Aquí se puede ver, que intente actualizar el apache para aplicar los cambios pero no me fue, asique me metí en el ultimo fichero, lo arregle y volví a recarga y ya iba

<img width="722" height="104" alt="image" src="https://github.com/user-attachments/assets/a695a6ac-64e7-49c5-9be1-94e44d1e5399" />

Luego, creamos un archivo html dentro del directorio que aún sigue vacio, para comprobar que el host virtual funciona

<img width="1059" height="666" alt="image" src="https://github.com/user-attachments/assets/0fdf42e0-4b5f-4f87-af86-6ec2feaedd40" />

Esto es lo que he añadido al fichero, guardamos y cerramos

<img width="1607" height="746" alt="image" src="https://github.com/user-attachments/assets/f58c9e7f-a0d9-4722-b096-ccc8461d304b" />

Luego, nos vamos al navegador y en el buscador url escribimos http://localhost, y nos aparecerá la pagina que hemos creado en html, nuestro host de apache está funcionando perfectamente

<img width="792" height="105" alt="image" src="https://github.com/user-attachments/assets/43af8b4a-f789-4920-b324-b29f21ed775c" />

Entrando en el siguiente archivo, podemos cambiar la prioridad de los archivos html y poner mas a los php

<img width="914" height="107" alt="image" src="https://github.com/user-attachments/assets/725b8245-9ec7-4427-b0bb-dc0a99a0195d" />

Cambiamos los ordenes de index.php e index.html, y guardamos el archivo y nos salimos

<img width="822" height="145" alt="image" src="https://github.com/user-attachments/assets/e7dfe119-699c-4808-8a2a-292ce6e254fb" />

Luego recargamos el apache y ya se nos aplica la nueva prioridad

## Paso 5: Probar el procesamiento de PHP en su servidor web

<img width="661" height="86" alt="image" src="https://github.com/user-attachments/assets/cd1b1d22-c53e-4bc1-965f-6f448e384d96" />

Vamos a crear un archivo php dentro de la siguiente ruta

<img width="751" height="123" alt="image" src="https://github.com/user-attachments/assets/a81ef425-3849-4353-bc0c-fd335b070e87" />

Dentro del archivo, ponemos lo siguiente, y guardamos y nos salimos

<img width="1456" height="691" alt="image" src="https://github.com/user-attachments/assets/2f8cc637-ebe8-4a79-afa3-0f9a95480daf" />

En el navegador escribimos la ip de nuestro servidor y el nombre del archivo creado anteriormente, y nos dirigirá a la siguiente página web

<img width="661" height="111" alt="image" src="https://github.com/user-attachments/assets/9268f870-cfd0-465c-b608-e13532c7c662" />

Luego podemos borrar el archivo, ya que puede contener información delicada

## Paso 6: Probar la conexión con la base de datos desde PHP

<img width="710" height="246" alt="image" src="https://github.com/user-attachments/assets/6df0ca0a-4eaa-44e4-899b-1f27e6d4e898" />

Comenzamos estableciendo conexión con la consola SQL

<img width="677" height="293" alt="image" src="https://github.com/user-attachments/assets/1719223f-e782-40d4-bc03-de2492c8a7b5" />

Creamos una base de datos

<img width="476" height="222" alt="image" src="https://github.com/user-attachments/assets/59c9c8ba-d0fb-4e36-b945-b03e4d20e5a3" />

Creamos un usuario y una contraseña segura

<img width="436" height="68" alt="image" src="https://github.com/user-attachments/assets/d42f087a-eb04-48f0-bb39-1d70c46ad4a5" />

Le damos privilegios al usuario creado sobre nuestra base de datos creada

<img width="267" height="64" alt="image" src="https://github.com/user-attachments/assets/d6d2cc79-5ddc-4ad7-9638-4a08130e3602" />

Y recargamos la tabla

<img width="394" height="56" alt="image" src="https://github.com/user-attachments/assets/4e626da8-3b77-49c9-8723-82e8f4dfdfa7" />

Y nos salimos de la base de datos

<img width="742" height="262" alt="image" src="https://github.com/user-attachments/assets/c3d4e440-08d8-46f5-85a1-7c192f8bb891" />

Luego, podemos comprobar que tenemos acceso a SQL con el usuario y contraseña creados

<img width="263" height="168" alt="image" src="https://github.com/user-attachments/assets/3a664789-54de-43e2-bdfa-99d849dc9066" />

Y con el siguiente comando, podemos ver las bases de datos creadas

<img width="298" height="114" alt="image" src="https://github.com/user-attachments/assets/6d9b0211-bb23-409b-96b5-5511681511ce" />

Vamos a crear una tabla de prueba con la siguiente instrucción

<img width="543" height="64" alt="image" src="https://github.com/user-attachments/assets/e1610608-bf10-4408-9de7-bc3df470018b" />

Insertamos algunos datos en la tabla de prueba

<img width="333" height="136" alt="image" src="https://github.com/user-attachments/assets/905183ec-59ff-4d16-92a5-86da4de936a9" />

Y para confirmar que todo se guardo correctamente, ejecutamos lo siguiente (podemos ver que esta todo en orden)

<img width="911" height="574" alt="image" src="https://github.com/user-attachments/assets/3e2a6904-d428-4018-beac-5cf89744ba8d" />

Abandonamos la consola sql

<img width="658" height="90" alt="image" src="https://github.com/user-attachments/assets/ec07078d-3d7d-4273-a274-37f53d8ba37e" />

Vamos a crear un archivo PHP en la siguiente ruta

<img width="700" height="321" alt="image" src="https://github.com/user-attachments/assets/d56360dd-a17b-4a65-b39e-00bbd8bd925d" />

Copiamos el siguiente contenido dentro del archivo, luego lo guardamos y nos salimos de el

<img width="437" height="150" alt="image" src="https://github.com/user-attachments/assets/5908d629-7338-4ccf-9566-5f93aabf0d41" />

Si ponemos lo siguiente en el navegador, ya tenemos acceso al contenido del archivo PHP, y podemos establecer conexión con el servidor PHP

## Conclusión

En esta guía, creamos una base flexible para presentar sitios web y aplicaciones PHP a sus visitantes usando Apache como servidor web y MySQL como sistema de base de datos
