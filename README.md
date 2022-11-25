# creacion_rsa

########## PASOS A SEGUIR PARA LA CREACION DE UN RSA Y SUBIR LA CLAVE A TU USUARIO DE AZURE ##########

 

 

1 . Abre un terminal y genera una clave RSA. Para ello:
 
     ssh-keygen -C "nombre@evolutio.com"

 

 

2. Presiona Enter y deja el todo en blanco. Te deberia aparecer algo asi:

 

     Generating public/private rsa key pair.

     Enter file in which to save the key (/c/Users/TU_USUARIO/.ssh/id_rsa):

     Enter passphrase (empty for no passphrase):

     Enter same passphrase again:

     Your identification has been saved in /c/Users/TU_USUARIO/.ssh/id_rsa.

     Your public key has been saved in /c/Users/TU_USUARIO/.ssh/id_rsa.pub.

     The key fingerprint is: SHA256:  nombre@evolutio.com

     The key's randomart image is:
     
     +---[RSA 3072]----+
    |+.   +yX*o .     |
    |... ..E+*=o      |
    |  ..o.=E=.o      |
    |   . * =.o .     |
    |    . S o o..    |
    |       + .oo     |
    |        S+.  .   |
    |        ..+.+    |
    |          o*..   |
    +----[SHA256]-----+

 

 

3. Nos habrá generado ya la clave publica(.pub) y privada. Cogemos esa clave publica con:

      cat id_rsa.pub

 

4. En azure, arriba a la derecha pinchamos en user settings y ssh public keys

    (imagen)

5. Pinchamos en add y añadimos la clave publica. 
   Deberia empezar por ssh-rsa …

6. Con esto ya podemos hacer un clone y un push sin necesidad de estar ingresando nuestro usuario, contraseña y token de verificacion cada vez que vayamos a hacer una accion.
