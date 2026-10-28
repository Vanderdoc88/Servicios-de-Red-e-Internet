## Busca información sobre las siguientes directivas y el valor que toman por defecto y el lugar donde se encuentra definida.

# Directivas de identificación

**ServerName:**  Permite hospedar cientos de páginas web en un único servidor y la misma IP. No viene definido por defecto de forma explícita; si no se especifica, Apache intenta deducirlo mediante una búsqueda inversa de la dirección IP del servidor o usa el nombre de host del sistema. Fichero de configuración principal (httpd.conf o apache2.conf) o en archivos de configuración de Virtual Hosts.

**ServerAdmin:** La dirección de correo definida aquí se muestra automáticamente en las páginas de error estándar de Apache (como la 404 o 500) para que el visitante sepa a quién notificar la falla. No tiene un valor por defecto predefinido (suele aparecer comentado como you@example.com). Lugar de definición en Fichero de configuración principal (httpd.conf) o dentro de bloques <VirtualHost>.

**ServerTokens:** Se usa para reducir la información que se expone a posibles atacantes u orquestadores de escaneo de vulnerabilidades. Cambiarlo a ServerTokens Prod evita revelar qué versión exacta de Apache o versión del SO se ejecuta, dificultando la explotación de vulnerabilidades conocidas, aunque su valor por defecto es full. Fichero de configuración principal (httpd.conf) o en ficheros de configuración global de seguridad (ej. security.conf en Debian/Ubuntu).

# Directivas de localización de ficheros

**DocumentRoot:** Impide que los usuarios o scripts web naveguen por carpetas sensibles del sistema operativo. Define la frontera raíz a partir de la cual el servidor entregará archivos. /usr/local/apache2/htdocs (en instalaciones desde código fuente) o /var/www/html (en distribuciones Linux como Ubuntu, Debian o RHEL). Fichero principal httpd.conf o en el archivo de configuración por defecto de los Virtual Hosts (000-default.conf).

**ErrorLog:**	Los desarrolladores lo consultan para ver fallos sintácticos de PHP, Python o Perl, así como errores de permisos en disco. logs/error_log (relativo al ServerRoot) o /var/log/apache2/error.log (en Debian/Ubuntu) / /var/log/httpd/error_log (en RHEL/CentOS). Fichero principal httpd.conf o archivos de configuración de Virtual Hosts.

**CustomLog:** Registra las IPs, páginas visitadas, navegadores y tiempo de respuesta. logs/access_log combinado con el formato common (o /var/log/apache2/access.log en sistemas basados en Debian). Fichero principal httpd.conf o archivos de configuración de Virtual Hosts.	

**ServerRoot:** Sirve como punto de referencia global para no tener que escribir rutas absolutas en cada directiva. /usr/local/apache2 (en instalaciones estándar) o /etc/apache2 (en Debian/Ubuntu) / /etc/httpd (en RHEL/CentOS). Viene preconfigurado de forma interna al compilar o instalar el paquete del servidor, y se define al principio del fichero principal httpd.conf / apache2.conf.

# Directivas de control de la conexión

**Timeout:** Evita la congelación de recursos cerrando conexiones lentas o colgadas que ocupan memoria innecesariamente. 60 segundos de valor por defecto(en versiones recientes de Apache 2.4; antiguamente era 300). Fichero principal de configuración (httpd.conf o apache2.conf).

**KeepAlive, MaxKeepAliveRequests, KeepAliveTimeout:** Permiten que el navegador descargue múltiples archivos (HTML, CSS, JS, imágenes) reutilizando el mismo canal TCP. On (habilitado por defecto en Apache). En otros como MaxKeepAliveRequest tiene de valor por defecto 100, y en el Timeout 5. Fichero principal de configuración (httpd.conf o apache2.conf).

# Otras

**LogLevel:** Si el servidor tiene poco espacio, se establece un LogLevel alto (warn o error) para evitar que el archivo de logs crezca gigabytes en pocas horas. warn como valor por defecto. Los niveles comunes van desde debug hasta emerg. Fichero principal de configuración (httpd.conf o apache2.conf), aplicándose de forma global o específica para ciertos módulos y Virtual Hosts.

**LogFormat:** Permite agregar campos personalizados en las trazas de log, como el tiempo exacto que tarda en procesarse la petición (%D), la IP real detrás de un balanceador de carga o CDN (%{X-Forwarded-For}i), o las cookies de sesión. Esto facilita el análisis de rendimiento a nivel micro. Define formatos predeterminados como el Common Log Format (CLF) ("%h %l %u %t \"%r\" %>s %b") y el formato Combined. Fichero principal de configuración (httpd.conf o en un archivo dedicado como logwatch.conf / apache2.conf).

