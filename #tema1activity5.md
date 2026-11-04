## Actividad #3

# Ejercicios
**Crea un directorio llamado "dir1" y otro llamado "dir2"**

<img width="596" height="117" alt="image" src="https://github.com/user-attachments/assets/de4e7cf0-db91-4c58-a7bf-38cdfb958e6d" />

**Explica qué diferencia existe entre ambos y muestra su equivalencia con la directiva Require: (La equivalencia con Require lo mostramos en los siguientes ejercicios)**
*<Directory /var/www/example1>* 
*Order Deny,Allow*
*Deny from All*
*Allow from 192.168.1.100*
*</Directory>*

Niega el acceso a todos excepto a 192.168.1.100

*<Directory /var/www/example1>*
*Order Allow,Deny*
*Deny from All*
*Allow from 192.168.1.100*
*</Directory>*

Niega el acceso a todos
		
# Para dir1
**Permite el acceso de las peticiones provenientes de 10.3.0.100**

<img width="838" height="397" alt="image" src="https://github.com/user-attachments/assets/77a23c87-50ce-4088-8cd8-3e059d27c961" />

<img width="883" height="600" alt="image" src="https://github.com/user-attachments/assets/b24f0128-4957-428c-9f3b-4f6513d6cf68" />

**Permite el acceso desde "marisma.intranet"**

<img width="321" height="70" alt="image" src="https://github.com/user-attachments/assets/16858f4a-37ee-4870-960a-d8d8ea2552b0" />

**Permite el acceso desde cualquier subdominio de "marisma.intranet"**

<img width="321" height="70" alt="image" src="https://github.com/user-attachments/assets/bce9eb6e-fd41-46e8-b7db-a86881a648a6" />

**Permite el acceso de las peticiones provenientes de "10.3.0.100" con máscara "255.255.0.0"**

<img width="346" height="88" alt="image" src="https://github.com/user-attachments/assets/b054f409-91c1-459a-a1b8-d75c8e858a66" />

# Modifica la configuración de forma que el acceso a dir1:
**Se permita a "marisma.intranet" y no se permita desde 10.3.0.101"**

<img width="345" height="112" alt="image" src="https://github.com/user-attachments/assets/b76906dc-c12c-4085-bd1a-21c580a8d55b" />
	
# Modifica la configuración de forma que el acceso a dir2:
**Se permita a "10.3.0.100/8" y no a "marisma.intranet"**

<img width="1066" height="669" alt="image" src="https://github.com/user-attachments/assets/03723db0-e99b-4b74-aaf8-cc60807b23ae" />
<img width="672" height="46" alt="image" src="https://github.com/user-attachments/assets/220ab132-1e4a-49ef-b4ec-4324c2defeb6" />

