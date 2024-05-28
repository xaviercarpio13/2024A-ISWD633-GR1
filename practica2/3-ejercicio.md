### Crear contenedor de Postgres sin que exponga los puertos. Usar la imagen: postgres:11.21-alpine3.17
```
docker run -d --name prac2 -e POSTGRES_PASSWORD=admin postgres:11.21-alpine3.17
ae6c366fe99a4cb72dfc8e9d476807305ead6332c281f024acd379e4c42994dd

```

### Crear un cliente de postgres. Usar la imagen: dpage/pgadmin4


La figura presenta el esquema creado en donde los puertos son:
- a: 8080
- b: 80
- c: 5432

![Imagen](imagenes/esquema-ejercicio3.PNG)

## Desde el cliente
### Acceder desde el cliente al servidor postgres creado.
![image](https://github.com/xaviercarpio13/2024A-ISWD633-GR1/assets/94008723/04f4128e-4e18-4c70-8955-c01478c04661)


### Crear la base de datos info, y dentro de esa base la tabla personas, con id (serial) y nombre (varchar), agregar un par de registros en la tabla, obligatorio incluir su nombre.

![image](https://github.com/xaviercarpio13/2024A-ISWD633-GR1/assets/94008723/29860df5-fdb7-4f25-b19c-eda809912fd5)


## Desde el servidor postgresl
### Acceder al servidor
### Conectarse a la base de datos info
### Realizar un select *from personas
![image](https://github.com/xaviercarpio13/2024A-ISWD633-GR1/assets/94008723/17fd5e84-3949-49c1-a506-ce26331fd132)

