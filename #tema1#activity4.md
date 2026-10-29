## Busca información sobre las siguientes directivas. Indica para que se usan y escribe un ejemplo que hayas encontrado.

<IfModule>

Se utiliza para condicionalmente ejecutar bloques de configuración según si un módulo específico de Apache está cargado o no. Esto es muy útil para evitar errores de inicio en el servidor si un módulo opcional está deshabilitado.

Ejemplo:
<IfModule mod_rewrite.c>
    # Activar el motor de reescritura solo si el módulo está disponible
    RewriteEngine On
    RewriteRule ^old-page\.html$ /new-page.html [R=301,L]
</IfModule>

LoadModule

  Carga un módulo u objeto compartido dinámico (DSO) en Apache al iniciar el servidor para añadir funcionalidades adicionales (como seguridad, compresión, reescritura de URLs, etc.).

  Ejemplo:
  LoadModule rewrite_module modules/mod_rewrite.so
  
Include

	Permite incluir otros ficheros de configuración dentro del fichero de configuración principal de Apache (httpd.conf o apache2.conf). Facilita la modularización y organización del código.

  Ejemplo: (Incluir todas las configuraciones de los hosts virtuales desde un directorio externo)
  Include conf/extra/httpd-vhosts.conf
  
<Directory>

Envuelve un grupo de directivas de configuración que se aplicarán exclusivamente al directorio del sistema de ficheros indicado y a todos sus subdirectorios.

Ejemplo:
<Directory "/var/www/html/secure">
    AuthType Basic
    AuthName "Área Restringida"
    AuthUserFile /etc/apache2/.htpasswd
    Require valid-user
</Directory>

<Files>

Aplica las directivas contenidas en su interior únicamente a ficheros específicos (coincidiendo con nombres de archivo o patrones con comodines), sin importar en qué directorio se encuentren.

Ejemplo: (Proteger el fichero de configuración de WordPress contra accesos web directos)
<Files "wp-config.php">
      Require all denied
</Files>

<Location>

	A diferencia de <Directory> (que actúa sobre rutas físicas del disco), <Location> actúa sobre URLs (rutas web). Es ideal para aplicar directivas a endpoints o recursos lógicos.

  Ejemplo:
<Location "/status">
    SetHandler server-status
    Require ip 192.168.1.0/24
</Location>
  
<VirtualHost>

Permite alojar múltiples sitios web (dominios o subdominios) en un mismo servidor físico, asignando configuraciones independientes (como la ruta raíz, logs o certificados SSL) a cada uno.

Ejemplo:
<VirtualHost *:80>
    ServerName misitio.com
    ServerAlias www.misitio.com
    DocumentRoot /var/www/misitio
    ErrorLog logs/misitio-error.log
    CustomLog logs/misitio-access.log combined
</VirtualHost>
	
## ¿Qué son los ficheros .htaccess?
Un fichero .htaccess (Hypertext Access) es un fichero de configuración distribuido que utiliza el servidor web Apache. Permite a los administradores o usuarios definir directivas de configuración de forma local para un directorio específico y todos sus subdirectorios, sin necesidad de modificar el fichero de configuración principal del servidor (httpd.conf).

* Principales usos: *

1. Crear redirecciones de URLs (por ejemplo, forzar HTTPS o redirigir páginas antiguas).

2. Proteger directorios mediante contraseñas (autenticación básica).

3. Bloquear el acceso por direcciones IP.

4. Personalizar páginas de error (como el error 404 - Página no encontrada).

5. Habilitar compresión o definir reglas de caché para mejorar el rendimiento.
