# creacion_rsa
documento de creacion de un rsa


Para crear una rsa y añadirla al azure DevOps.

 

 

Abre un terminal y genera una clave RSA. Para ello:
 

ssh-keygen -C "nombre@evolutio.com"

 

 

Presiona Enter y deja el todo en blanco.
 

Te deberia aparecer algo asi:

 

Generating public/private rsa key pair.

Enter file in which to save the key (/c/Users/TU_USUARIO/.ssh/id_rsa):

Enter passphrase (empty for no passphrase):

Enter same passphrase again:

Your identification has been saved in /c/Users/TU_USUARIO/.ssh/id_rsa.

Your public key has been saved in /c/Users/TU_USUARIO/.ssh/id_rsa.pub.

The key fingerprint is: SHA256:******************************************* nombre@evolutio.com

The key's randomart image is: +---[RSA 3072]----+ |+. +yX*o . | |... ..E+*=o | | ..o.=E=.o | | . * =.o . | | . S o o.. | | + .oo | | S+. . | | ..+.+ | | o*.. | +----[SHA256]-----+

 

 

Nos habrá generado ya la clave publica(.pub) y privada
Cogemos esa clave publica con:
Cat id_rsa.pub

 

En azure, arriba a la derecha pinchamos en user settings y ssh public keys

Pinchamos en add y añadimos la clave publica. Deberia empezar por ssh-rsa …
Con esto ya podemos hacer un clone y un push sin necesidad de estar ingresando nuestro usuario, contraseña y token de verificacion cada vez que vayamos a hacer una accion.
