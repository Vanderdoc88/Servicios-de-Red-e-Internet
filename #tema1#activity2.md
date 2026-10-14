# Activity#2 - Configuración básica de Apache
## Pon en marcha el servidor Apache y lleva a cabo los siguientes cambios en el archivo de configuración
1. Apache utilizará el puerto 81 además del 80

2. Añadir el dominio “marisma.intranet” en el fichero “hosts”
	
3. Cambia la directiva “ServerTokens” para mostrar el nombre del producto.
	
4. Comprueba si se visualiza el pie de página en las páginas generadas por Apache (por ejemplo, en las páginas de error). Cambia el valor de la directiva “ServerSignature” y comprueba que funciona correctamente. 
	
5. Crea un directorio “prueba” y otro directorio “prueba2”. Incluye un par de páginas en cada una de ellas.
	
6. Redirecciona el contenido de la carpeta “prueba” hacia “prueba2”
	
7. Es posible redireccionar tan solo una página en lugar de toda la carpeta. Pruébalo.
	
8. Usa la directiva userdir
	
9. Usa la directiva alias para redireccionar a una carpeta dentro del directorio de usuario.
	
10. ¿Para qué sirve la directiva Options y dónde aparece. Comprueba si apache indexa los directorios. Si es así, ¿cómo lo desactivamos?

# Actividad 2.2
## Trabajando con scripts
1. Crea un script que añada un puerto de escucha en el fichero de configuración de Apache. El puerto se recibirá como parámetro en la llamada y se comprobará que no esté ya presente en el fichero de configuración.
2. Crea un script que añada un nombre de dominio y una ip al fichero hosts. Debemos comprobar que no existe dicho dominio en el fichero hosts
3. Crea un script que nos permita crear una página web con un título, una cabecera y un mensaje
