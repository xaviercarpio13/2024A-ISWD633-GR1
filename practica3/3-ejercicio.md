## Esquema para el ejercicio
![Imagen](imagenes/esquema-ejercicio3.PNG)

### Crear red net-wp
```
docker network create net-wp
```
### Creacion contenedor wordpress
```
docker run -d --name wordpress -v "C:\Users\xavic\OneDrive\Documentos\EPN\2024 - A\Construccion\Practica4\www" -p 9500:80 --network net-wp wordpress
```

### Creacion contenedor mysql
```
docker run -d --name mysql -v "C:\Users\xavic\OneDrive\Documentos\EPN\2024 - A\Construccion\Practica4\db":/var/lib/mysql -P --network net-wp --env-file="C:\Users\xavic\OneDrive\Escritorio\pass.txt" mysql:8
557dc5100a8c163e13533fd85daca30ade73458df55e2ce4e7909d946b521949
```

### Para que persista la información es necesario conocer en dónde mysql almacena la información.
En el esquema del ejercicio la carpeta contenedor (a) es /var/lib/mysql
Ruta carpeta host: C:\Users\xavic\OneDrive\Documentos\EPN\2024 - A\Construccion\Practica4\db


### ¿Qué contiene la carpeta db del host?
Contiene toda la informacion que se encuentra en el contenedor en el directorio /var/lib/mysql


### Crear un contenedor con la imagen mysql:8  en la red net-wp, configurar las variables de entorno: MYSQL_ROOT_PASSWORD, MYSQL_DATABASE, MYSQL_USER y MYSQL_PASSWORD
```

docker run -d --name mysql -v "C:\Users\xavic\OneDrive\Documentos\EPN\2024 - A\Construccion\Practica4\db":/var/lib/mysql -P --network net-wp --env-file="C:\Users\xavic\OneDrive\Escritorio\pass.txt" mysql:8
557dc5100a8c163e13533fd85daca30ade73458df55e2ce4e7909d946b521949
```

### ¿Qué observa en la carpeta db que se encontraba inicialmente vacía?
![image](https://github.com/xaviercarpio13/2024A-ISWD633-GR1/assets/94008723/3122453e-8984-490a-95e0-c9460b511b61)

### Para que persista la información es necesario conocer en dónde wordpress almacena la información.
# COMPLETAR LA SIGUIENTE ORACIÓN. REVISAR LA DOCUMENTACIÓN DE LA IMAGEN EN https://hub.docker.com/)
En el esquema del ejercicio la carpeta contenedor (b) es /var/www/html
Ruta carpeta host: .../ejercicio3/www

### Crear un contenedor con la imagen wordpress en la red net-wp, configurar las variables de entorno WORDPRESS_DB_HOST, WORDPRESS_DB_USER, WORDPRESS_DB_PASSWORD y WORDPRESS_DB_NAME (los valores de estas variables corresponden a los del contenedor creado previamente)
```
docker run -d --name wordpress -v "C:\Users\xavic\OneDrive\Documentos\EPN\2024 - A\Construccion\Practica4\www":/var/www/html -p 9500:80 --env-file="C:\Users\xavic\OneDrive\Escritorio\pass-wordpress.txt" --network net-wp wordpress
```

### Personalizar la apariencia de wordpress y agregar una entrada
![image](https://github.com/xaviercarpio13/2024A-ISWD633-GR1/assets/94008723/eafa0faf-902a-4dd9-9d84-dcf06f6a5cb5)

### Eliminar el contenedor y crearlo nuevamente, ¿qué ha sucedido?
Al crear los volumenes e inicializar los contenedores en esas mismas rutas, la configuracion de los contenedores
fue persistida y recuperada

