## Esquema para el ejercicio
![image](https://github.com/xaviercarpio13/2024A-ISWD633-GR1/assets/94008723/47c22bad-fe1d-4d87-a354-6e81ce435157)


### Crear la red
```
docker network create net-wp
```

### Crear el contenedor mysql a partir de la imagen mysql:8, configurar las variables de entorno necesarias

```
docker run -P -d --name mysqlP2 --env-file="C:\Users\xavic\OneDrive\Escritorio\pass.txt" --network net-wp mysql:8
```

### Crear el contenedor wordpress a partir de la imagen: wordpress, configurar las variables de entorno necesarias
```
docker run -d --name wordpress -p 9300:80 --network net-wp wordpress
```

De acuerdo con el trabajo realizado, en la el esquema de ejercicio el puerto a es **9300**

Ingresar desde el navegador al wordpress y finalizar la configuración de instalación.
![image](https://github.com/xaviercarpio13/2024A-ISWD633-GR1/assets/94008723/1f412805-9909-4d23-8059-72ae076507ed)
![Captura de pantalla 2024-05-27 230316](https://github.com/xaviercarpio13/2024A-ISWD633-GR1/assets/94008723/048bee76-3a41-470b-82ad-9db9320f3e9b)



Desde el panel de admin: cambiar el tema y crear una nueva publicación.
Ingresar a: http://localhost:9300/ 
recordar que a es el puerto que usó para el mapeo con wordpress
![image](https://github.com/xaviercarpio13/2024A-ISWD633-GR1/assets/94008723/8a29e85c-33d9-4dc9-8a66-71f3bcd51ac7)


### Eliminar el contenedor wordpress
```
docker stop wordpress
docker rm wordpress
```

### Crear nuevamente el contenedor wordpress
Ingresar a: http://localhost:9300/ 
recordar que a es el puerto que usó para el mapeo con wordpress

### ¿Qué ha sucedido, qué puede observar?
Al borrar y volver a crear el contenedor, se reinicia la configuración de wordpress





