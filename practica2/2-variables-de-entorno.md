# Variables de Entorno
### ¿Qué son las variables de entorno?
Las variables de entorno en Docker son una forma de configurar y personalizar el comportamiento de los contenedores durante su ejecución. Estas variables pueden ser utilizadas para pasar información, como credenciales, configuración de aplicaciones o cualquier dato que se requiera
### Para crear un contenedor con variables de entorno

```
docker run -d --name <nombre contenedor> -e <nombre variable1>=<valor1> -e <nombre variable2>=<valor2>
```

### Crear un contenedor a partir de la imagen de nginx:alpine con las siguientes variables de entorno: username y role. Para la variable de entorno rol asignar el valor admin.

# COMPROBACIÓN DE LA CREACIÓN DE LAS VARIABLES DE ENTORNO DEL CONTENEDOR ANTERIOR
![image](https://github.com/xaviercarpio13/2024A-ISWD633-GR1/assets/94008723/d9b2715d-97fb-4289-86fd-f2316d7b9165)

### Crear un contenedor con mysql:8 , mapear todos los puertos
```
docker run -P -d --name mysqlP2 mysql:8
```

### ¿El contenedor se está ejecutando?
```
docker container ls -l
```
El contenedor se encuentra detenido

### Identificar el problema
El contenedor no se ejecuta incluso cuando manualmente se lo inicializa

### Eliminar el contenedor creado con mysql:8 
```
docker rm mysqlP2
```

### Para crear un contenedor con variables de entorno especificadas
- Portabilidad: Las aplicaciones se vuelven más portátiles y pueden ser desplegadas en diferentes entornos (desarrollo, pruebas, producción) simplemente cambiando el archivo de variables de entorno.
- Centralización: Todas las configuraciones importantes se centralizan en un solo lugar, lo que facilita la gestión y auditoría de las configuraciones.
- Consistencia: Asegura que todos los miembros del equipo de desarrollo o los entornos de despliegue utilicen las mismas configuraciones.
- Evitar Exposición en el Código: Mantener variables sensibles como contraseñas, claves API, y tokens fuera del código fuente reduce el riesgo de exposición accidental a través del control de versiones.
- Control de Acceso: Los archivos de variables de entorno pueden ser gestionados con permisos específicos, limitando quién puede ver o modificar la configuración sensible.

Previo a esto es necesario crear el archivo y colocar las variables en un archivo, **.env** se ha convertido en una convención estándar, pero también es posible usar cualquier extensión como **.txt**.
```
docker run -d --name <nombre contenedor> --env-file=<nombreArchivo>.<extensión> <nombre imagen>
```
**Considerar**
Es necesario especificar la ruta absoluta del archivo si este se encuentra en una ubicación diferente a la que estás ejecutando el comando docker run.

### Crear un contenedor con mysql:8 , mapear todos los puertos y configurar las variables de entorno mediante un archivo

# COMPROBACIÓN DE LA CREACIÓN DE LAS VARIABLES DE ENTORNO DEL CONTENEDOR ANTERIOR 
![image](https://github.com/xaviercarpio13/2024A-ISWD633-GR1/assets/94008723/6f8b8708-b521-4bc5-a116-ac8e02b7c534)


### ¿Qué bases de datos existen en el contenedor creado?
![image](https://github.com/xaviercarpio13/2024A-ISWD633-GR1/assets/94008723/19c425fd-e892-4908-a6f1-253afdbe5441)

