# Cómo instalar la pila Linux, Apache, MySQL y PHP (LAMP) en Ubuntu 20.04

Comenzamos
Paso 1: Instalar Apache y actualizar el firewall
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

Paso 2: Instalar MySQL
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
