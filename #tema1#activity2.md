# Activity#2 - Configuración básica de Apache
## Pon en marcha el servidor Apache y lleva a cabo los siguientes cambios en el archivo de configuración
1. Apache utilizará el puerto 81 además del 80

<img width="779" height="156" alt="image" src="https://github.com/user-attachments/assets/eeeaad75-6247-4751-bdd3-24598d3759aa" />

Nos metemos al siguiente directorio y al siguiente fichero, te tienes que meter con "sudo"

<img width="853" height="295" alt="image" src="https://github.com/user-attachments/assets/444635c7-effc-4f34-8bca-eef97cea35da" />

Añadimos "Listen 81", luego guardamos el documento y nos salimos

<img width="687" height="20" alt="image" src="https://github.com/user-attachments/assets/b46b7141-9ea5-44d7-9fda-96a46cc6f2fa" />

Reiniciamos

<img width="1065" height="667" alt="image" src="https://github.com/user-attachments/assets/d90293af-1586-4f22-aecd-01fc2c1837b5" />

Ponemos "localhost:81" en el navegador y nos saldrá la siguiente página

2. Añadir el dominio “marisma.intranet” en el fichero “hosts”

<img width="747" height="107" alt="image" src="https://github.com/user-attachments/assets/c18b0674-7745-4865-8d44-eb889d3295b1" />
<img width="855" height="244" alt="image" src="https://github.com/user-attachments/assets/c49a7505-bccd-40ef-988d-5080e792edbb" />
<img width="1072" height="667" alt="image" src="https://github.com/user-attachments/assets/12694952-c4e4-4207-ad0c-b1b97dfb1255" />
Poniendo el dominio en el navegador, volvemos a la misma página
	
3. Cambia la directiva “ServerTokens” para mostrar el nombre del producto.

<img width="749" height="109" alt="image" src="https://github.com/user-attachments/assets/f47ae660-30d3-4291-99eb-fa329de9f6ec" />

Nos metemos al siguiente archivo

<img width="1067" height="667" alt="image" src="https://github.com/user-attachments/assets/1ff807c4-601d-4551-83f8-e7923b13dce1" />

Añadimos lo siguiente en la ultima linea

4. Comprueba si se visualiza el pie de página en las páginas generadas por Apache (por ejemplo, en las páginas de error). Cambia el valor de la directiva “ServerSignature” y comprueba que funciona correctamente.

<img width="1065" height="668" alt="image" src="https://github.com/user-attachments/assets/8bd3e361-0b97-4624-bad9-37e3adf49cb0" />

Añadimos esta línea en el mismo archivo del ejercicio 3

<img width="1071" height="670" alt="image" src="https://github.com/user-attachments/assets/f827d4ff-5790-4347-b377-e41b5e7300a8" />

Nos volvemos a meter en la página del dominio, pulsamos la tecla F12 y buscamos que contenga Apache
	
5. Crea un directorio “prueba” y otro directorio “prueba2”. Incluye un par de páginas en cada una de ellas.
<img width="793" height="132" alt="image" src="https://github.com/user-attachments/assets/36f3742c-f353-4b3e-aaf9-e5399e467243" />
<img width="606" height="114" alt="image" src="https://github.com/user-attachments/assets/a0d5c15f-2455-4fa9-8d3f-a1d242bf44a6" />
	
6. Redirecciona el contenido de la carpeta “prueba” hacia “prueba2”
<img width="1067" height="100" alt="image" src="https://github.com/user-attachments/assets/25759eef-75bf-4308-baa9-184f9e2b7736" />

Nos vamos al fichero de configuración de apache

<img width="1070" height="665" alt="image" src="https://github.com/user-attachments/assets/2296d3aa-5c96-452b-b008-fcc28ef8edea" />

Añadimos la siguiente línea al final

7. Es posible redireccionar tan solo una página en lugar de toda la carpeta. Pruébalo.
<img width="1068" height="665" alt="image" src="https://github.com/user-attachments/assets/3d4439dc-593c-4c7f-a182-80c8a0030407" />

En el mismo documento, ponemos la siguiente línea al final, guardamos y nos salimos

<img width="976" height="53" alt="image" src="https://github.com/user-attachments/assets/24f8f53f-3f41-42ef-83bb-314b68092e32" />

Y reiniciamos el servicio para que se apliquen los cambios
	
8. Usa la directiva userdir

<img width="592" height="131" alt="image" src="https://github.com/user-attachments/assets/68981483-9de6-4066-ab4b-b55daaa028ad" />

La utilizamos y reiniciamos apache con el comando de systemctl

<img width="684" height="23" alt="image" src="https://github.com/user-attachments/assets/02f77e85-02fb-44f1-a066-a7e2745ed1d6" />

Creamos el siguiente directorio

<img width="665" height="42" alt="image" src="https://github.com/user-attachments/assets/e9233516-d28f-4fc2-b931-845a5d9a6d87" />

Y dentro del directorio, creamos el siguiente archivo

<img width="867" height="292" alt="image" src="https://github.com/user-attachments/assets/e9df92d6-5c5c-485d-aabd-3cd8eb7021b4" />

Dentro del archivo, creamos una pagina en html, como quieras, lo guardamos y nos salimos

<img width="1013" height="82" alt="image" src="https://github.com/user-attachments/assets/c07174ad-c10f-41ce-92c4-356386345535" />

Comprobamos que no haya errores de sintaxis

<img width="576" height="36" alt="image" src="https://github.com/user-attachments/assets/79ed14e1-a721-4c69-848d-28b2385e0559" />

Reiniciamos el servicio

<img width="639" height="34" alt="image" src="https://github.com/user-attachments/assets/2a9bbd93-9d5a-4497-9ad9-31bbb83806af" />

Y le damos permisos al usuario

9. Usa la directiva alias para redireccionar a una carpeta dentro del directorio de usuario.
<img width="686" height="105" alt="image" src="https://github.com/user-attachments/assets/dc05d66d-044b-4595-8378-d05e51d3d606" />

Volvemos a ir al fichero de configuración apache

<img width="1066" height="665" alt="image" src="https://github.com/user-attachments/assets/9a4304f1-afbb-4962-9049-e5dc8ce8a329" />

Añadimos las siguientes líneas al final del documento, guardamos y cerramos

<img width="653" height="37" alt="image" src="https://github.com/user-attachments/assets/84111a0c-6148-435f-9526-8d8e28aa6803" />

Creamos el directorio, y añadimos ficheros en el

<img width="978" height="53" alt="image" src="https://github.com/user-attachments/assets/6f8581b8-823b-4bc8-a7c4-b95676fe3cb7" />

Reiniciamos el servicio

Comprobamos con navegador

10. ¿Para qué sirve la directiva Options y dónde aparece. Comprueba si apache indexa los directorios. Si es así, ¿cómo lo desactivamos?
*Explicar teoria Options
Si, apache indexa, rl directory /var/www, la prueba esta en /etc/apache2/apache2.conf
<img width="1071" height="667" alt="image" src="https://github.com/user-attachments/assets/37b2460e-65de-46c8-9542-cd6dedeb3df5" />

Aquí tenemos la prueba

<img width="1066" height="670" alt="image" src="https://github.com/user-attachments/assets/1cb34d8f-23bb-4ab3-a291-ecf543f1fd13" />

Modificamos la siguiente línea, simplemente le ponemos "-" a Indexes y "+" a FollowSymLinks, guardamos y nos salimos del documento

<img width="751" height="148" alt="image" src="https://github.com/user-attachments/assets/b25be68c-856e-41f5-97fc-6fc9c3ea55e0" />

Y luego reiniciamos el servicio Apache

# Actividad 2.2
## Trabajando con scripts
1. Crea un script que añada un puerto de escucha en el fichero de configuración de Apache. El puerto se recibirá como parámetro en la llamada y se comprobará que no esté ya presente en el fichero de configuración
<img width="758" height="117" alt="image" src="https://github.com/user-attachments/assets/96f57761-978d-4a92-b9a7-f734caf04749" />

Vamos a empezar metiéndonos en el directorio /etc/apache2

<img width="620" height="18" alt="image" src="https://github.com/user-attachments/assets/261d3d92-3292-45bd-bc29-b89518c5d74b" />

Y creamos el siguiente fichero .sh

<img width="871" height="557" alt="image" src="https://github.com/user-attachments/assets/fa12c15d-47da-46ea-b409-60d4afbef4de" />

Este es mi shellscript, guardamos y cerramos.

<img width="1009" height="132" alt="image" src="https://github.com/user-attachments/assets/4a168932-5c63-4011-a03d-d4aa41f5b970" />

Ejecutamos el script, y vemos que se nos a añadido el puerto bien

2. Crea un script que añada un nombre de dominio y una ip al fichero hosts. Debemos comprobar que no existe dicho dominio en el fichero hosts
<img width="793" height="109" alt="image" src="https://github.com/user-attachments/assets/fd0ddf7a-4998-4bb1-a4c2-1dd2b457e466" />

Nos salimos del directorio apache2, y en el directorio /etc creamos el fichero .sh (en el directorio /etc es donde se encuentra el fichero host.conf)

<img width="811" height="451" alt="image" src="https://github.com/user-attachments/assets/da0d102e-4cca-425c-a0d2-2b12819be932" />

Así sera nuestro script, guardamos y cerramos

3. Crea un script que nos permita crear una página web con un título, una cabecera y un mensaje
