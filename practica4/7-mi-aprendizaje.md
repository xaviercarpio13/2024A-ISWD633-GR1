# COMPLETAR  
# Principales Aprendizajes
## Uso de Recursos:
Antes de la práctica, no tenía una comprensión clara de cómo Docker maneja y limita el uso de recursos como CPU y memoria. Ahora, he aprendido a utilizar opciones como --cpus y --memory para asignar y restringir los recursos a los contenedores, asegurando así que una aplicación no consuma más de lo debido y afecte el rendimiento de otras aplicaciones en el mismo host. Este conocimiento es crucial para optimizar el rendimiento y la eficiencia de los sistemas en entornos de producción.

## Dockerfile:
La creación de Dockerfiles era un área que solo conocía superficialmente. A través de esta práctica, aprendí a escribir Dockerfiles eficientes y bien estructurados, especificando las instrucciones necesarias para construir una imagen Docker. Entendí la importancia de cada instrucción, como FROM, COPY, RUN, y cómo utilizar CMD y ENTRYPOINT para definir el comportamiento predeterminado del contenedor. Este aprendizaje me ha permitido automatizar la construcción de imágenes y mejorar la portabilidad y consistencia de mis aplicaciones.

## Healthcheck:
Antes de esta práctica, no estaba familiarizado con la implementación de healthchecks en Docker. Ahora sé cómo definir un healthcheck en un Dockerfile usando la instrucción HEALTHCHECK, permitiendo que Docker monitorice la salud de un contenedor y tome acciones si algo falla. Esta habilidad es vital para mantener la alta disponibilidad y resiliencia de las aplicaciones, ya que facilita la detección y recuperación de fallos.

## Políticas de Inicio:
El concepto de políticas de inicio era algo nuevo para mí. Durante la práctica, aprendí a configurar políticas como --restart para controlar el comportamiento de reinicio de los contenedores. Ahora sé cómo asegurarme de que los contenedores se reinicien automáticamente en caso de fallo (always), nunca se reinicien (no), o se reinicien bajo ciertas condiciones (on-failure). Esta capacidad es esencial para gestionar la disponibilidad y el tiempo de actividad de los servicios desplegados en contenedores.

# Conclusión 
Estos aprendizajes son invaluables para mi formación profesional. El dominio de Docker y sus funcionalidades avanzadas me permite desarrollar y gestionar aplicaciones de manera más eficiente y robusta. La capacidad de optimizar el uso de recursos, automatizar la construcción de imágenes, implementar verificaciones de salud y gestionar políticas de inicio son habilidades que me preparan mejor para enfrentar desafíos en entornos de producción
