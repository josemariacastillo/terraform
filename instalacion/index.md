# Instalación de Terraform

Para instalar Terraform, descargamos el paquete apropiado para nuestro sistema desde
la página oficial de Terraform.

Sistemas operativos compatibles con Terraform:
* Linux: 32­bit | 64­bit | Arm
* Windows:  32­bit | 64­bit
* Mac OS X:  64­bit
* FreeBSD:  32­bit | 64­bit | Arm
* OpenBSD:  32­bit | 64­bit
* Solaris:  64­bit

### Instalación en sistema operativo Linux
Vamos a la página oficial https://www.terraform.io/downloads.html. En ella
encontramos los binarios.

![](imagenes/install_linux/1.png)

Seleccionamos el sistema operativo y la arquitectura, en nuestro caso elegiremos Linux 64­bit puesto que lo instalaremos en una maquina Debian jessie.

![](imagenes/install_linux/2.png)

Creamos un directorio para los binarios de Terraform.

![](imagenes/install_linux/3.png)

Moveremos el fichero descargado anteriormente al interior de la carpeta.

![](imagenes/install_linux/4.png)

Nos situamos en el directorio terraform.

![](imagenes/install_linux/5.png)

Descomprimimos los binarios de Terraform con el comando unzip.

![](imagenes/install_linux/6.png)

Exportamos las variables de entorno de Terraform.

![](imagenes/install_linux/7.png)

Por último comprobamos que se ha instalado bien ejecutando el comando siguiente:

![](imagenes/install_linux/8.png)

### Instalación en sistema operativo Windows
Vamos a la página oficial https://www.terraform.io/downloads.html. En ella
encontramos el ejecutable.

![](imagenes/install_win/1.png)

Seleccionamos   el   sistema   operativo   y   la   arquitectura,   en   nuestro   caso   elegiremos Windows 64­bit puesto que lo instalaremos en una maquina Windows 10.

![](imagenes/install_win/2.png)

Creamos un directorio para el ejecutable de Terraform.

![](imagenes/install_win/3.png)

Copiamos el fichero descargado anteriormente al directorio terraform.

![](imagenes/install_win/4.png)

Nos situamos en el directorio terraform.

![](imagenes/install_win/5.png)

Descomprimimos el ejecutable en el interior del directorio creado anteriormente.

![](imagenes/install_win/6.png)
Ahora añadimos la variable de entorno de Terraform para el usuario, para ello en el menú inicio de Windows hacemos clic derecho en sistema.

![](imagenes/install_win/7.png)

Hacemos clic en Configuración avanzada del sistema.

![](imagenes/install_win/8.png)

Hacemos clic en Variables de entorno.

![](imagenes/install_win/9.png)

En la siguiente pantalla pulsamos el botón Nueva.

![](imagenes/install_win/10.png)

Asignamos un nombre a la variable y en el botón Examinar archivo buscamos la ruta del
ejecutable de Terraform.

![](imagenes/install_win/11.png)

Aceptamos y comprobamos que se ha guardado la variable de entorno.

![](imagenes/install_win/12.png)

Ahora desde una ventana de símbolo de sistema comprobamos que Terraform funciona.

![](imagenes/install_win/13.png)
