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
	
6. Crea un directorio “prueba” y otro directorio “prueba2”. Incluye un par de páginas en cada una de ellas.
	
7. Redirecciona el contenido de la carpeta “prueba” hacia “prueba2”
	
8. Es posible redireccionar tan solo una página en lugar de toda la carpeta. Pruébalo.
	
9. Usa la directiva userdir
	
10. Usa la directiva alias para redireccionar a una carpeta dentro del directorio de usuario.
	
11. ¿Para qué sirve la directiva Options y dónde aparece. Comprueba si apache indexa los directorios. Si es así, ¿cómo lo desactivamos?

# Actividad 2.2
## Trabajando con scripts
1. Crea un script que añada un puerto de escucha en el fichero de configuración de Apache. El puerto se recibirá como parámetro en la llamada y se comprobará que no esté ya presente en el fichero de configuración.
2. Crea un script que añada un nombre de dominio y una ip al fichero hosts. Debemos comprobar que no existe dicho dominio en el fichero hosts
3. Crea un script que nos permita crear una página web con un título, una cabecera y un mensaje
