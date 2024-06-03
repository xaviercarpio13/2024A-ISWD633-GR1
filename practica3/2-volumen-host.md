# VOLUMEN TIPO HOST
Un volumen host (o bind mount) es un tipo de volumen donde se monta un directorio o archivo específico del sistema de archivos del host en un contenedor.

```
docker run -d --name <nombre contenedor> -v <ruta carpeta host>:<ruta carpeta contenedor> <imagen> 
```

### Crear un volumen tipo host con la imagen nginx:alpine, para la ruta carpeta host: directorio en donde se encuentra la carpeta html en tu computador y para la ruta carpeta contenedor: /usr/share/nginx/html esta ruta se obtiene al revisar la se obtiene desde la documentación
![Volúmenes](imagenes/volumen-host.PNG)
```
docker run -d --name prac3 -v "C:\Users\xavic\OneDrive\Documentos\EPN\2024 - A\Construccion\Practica3":/u
sr/share/nginx/html nginx:alpine
```

### ¿Qué sucede al ingresar al servidor de nginx?
Existe el error 403 producido por la ausencia del archivo index.html en el contenedor, por lo tanto, no permite acceder a este archivo.

### ¿Qué pasa con el archivo index.html del contenedor?
No existe archivo index.html en el contenedor

### Ir a https://html5up.net/ y descargar un template gratuito, descomprirlo dentro de nginx/html
### ¿Qué sucede al ingresar al servidor de nginx?
Ahora se accede al documento index.html dentro del contenedor y al acceder al servidor se tiene la pagina descrita en el archivo index: 
![image](https://github.com/xaviercarpio13/2024A-ISWD633-GR1/assets/94008723/5a955b3e-4833-4a71-8f34-f1f55d2a0e0e)


### Eliminar el contenedor
# COMPLETAR CON EL COMANDO

### ¿Qué sucede al crear nuevamente el mismo contenedor con volumen de tipo host a los directorios definidos anteriormente?
La información almacenada en la carpeta host se refleja en la carpeta del contenedor, por lo que la configuración realizada es persistida.

### ¿Qué hace el comando pwd?
Muestra el directorio actual en el que se está trabajando

Si quieres incluir el comando pwd dentro de un comando de Docker, lo puedes hacer de diferentes maneras dependiendo del shell que estés utilizando.


### Volumen tipo host usando PWD y PowerShell
```
docker run -d --name <nombre contenedor> --publish published=<valorPuertoHost>,target=<valor> -v ${PWD}/<ruta relativa>:<ruta absoluta> <nombre imagen>:<tag> 
```

### Volumen tipo host usando PWD (Git Bash)

```
docker run -d --name <nombre contenedor> --publish published=<valorPuertoHost>,target=<valor> -v $(pwd -W)/html:/usr/share/nginx/html <nombre imagen>:<tag> 
```

### Volumen tipo host usando PWD (en Linux)

```
docker run -d --name <nombre contenedor> --publish published=<valorPuertoHost>,target=<valor> -v $(pwd)/html:/usr/share/nginx/html <nombre imagen>:<tag> 
```

