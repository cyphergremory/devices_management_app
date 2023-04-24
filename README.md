A continuación se presenta la planificación del proyecto con las características solicitadas:

---

# Plan de desarrollo de la aplicación web

## Resumen ejecutivo

La empresa desea construir una aplicación web para una nueva solución wifi que permita comprar dispositivos, alquilar dispositivos y comprar planes de datos en varios idiomas y países. El equipo de desarrollo utilizará PHP, Laravel, React, Vue y MySQL y Bitbucket para almacenar el código fuente. Se utilizarán sistemas de back-end en AWS. El CTO desea un prototipo en 2 meses. Para el manejo de roles y permisos se utilizará Laravel Spatie y para el manejo de divisas se utilizará una API de currency. Se utilizarán pipelines en Bitbucket para garantizar la calidad del código y la implementación de pruebas unitarias y de integración. Se considerará la opción de una sola instancia para la aplicación web, pero si se utiliza múltiples instancias, se utilizarán microfrontends con Nuxt o Next.

## Tecnologías

- PHP para el back-end utilizando Laravel.
- React y Vue para el front-end.
- MySQL para la base de datos.
- Laravel Spatie para el manejo de roles y permisos.
- API de currency para el manejo de divisas.
- Bitbucket para el almacenamiento del código fuente.
- AWS para los sistemas de back-end.
- Pipelines de Bitbucket para garantizar la calidad del código y las pruebas unitarias e integración.
- Microfrontends con Nuxt o Next en caso de utilizar múltiples instancias.

## Desarrollo

### Idiomas y países

Para la implementación de varios idiomas y países, se utilizará un paquete de internacionalización en Laravel. Este paquete permitirá la creación de diferentes archivos de idiomas, uno para cada idioma, que contendrán todas las cadenas de texto utilizadas en la aplicación. Se utilizará un middleware para detectar el idioma de la solicitud del usuario y, a continuación, se cargará el archivo de idioma correspondiente.

### Manejo de divisas

Se utilizará una API de currency para la conversión de monedas en la aplicación. Se integrará la API en la aplicación web utilizando el patrón de diseño adaptador. Se creará un servicio en el back-end que interactuará con la API de currency y se encargará de realizar la conversión de monedas. Este servicio se utilizará en los controladores de Laravel para convertir los precios de los productos en la moneda local del usuario.

### Manejo de roles y permisos

Para el manejo de roles y permisos se utilizará Laravel Spatie. Se crearán diferentes roles y permisos, por ejemplo, el permiso de agregar o eliminar inventario, y se asignarán a los usuarios según sus roles. Se utilizarán middleware de Laravel para verificar si el usuario tiene el permiso correspondiente antes de realizar cualquier acción.

### Pipelines de Bitbucket

Se utilizarán pipelines de Bitbucket para garantizar la calidad del código y la implementación de pruebas unitarias e integración. En cada confirmación de código, se ejecutará el conjunto completo de pruebas de la aplicación. Además, se utilizarán herramientas de análisis estático de código para garantizar que se sigan las mejores prácticas de codificación y se mantenga una alta calidad del código.

### Formato de desarrollo y pruebas:

Se utilizará el enfoque de Desarrollo Dirigido por Pruebas (TDD) para garantizar la calidad del código y la funcionalidad. Además, se realizarán pruebas de usuario para validar la experiencia del usuario final.

En cuanto al testeo de APIs, se utilizarán herramientas como Postman y Swagger para probar exhaustivamente todas las rutas y endpoints disponibles. También se incluirán pruebas de carga para verificar la escalabilidad del sistema y su capacidad para manejar un gran número de solicitudes simultáneas.

### Herramientas para el testeo de APIs
Existen varias herramientas para el testeo de APIs, algunas de las más populares son:

Postman: Es una aplicación que permite realizar peticiones HTTP a APIs y analizar las respuestas. Permite enviar diferentes tipos de peticiones como GET, POST, PUT, DELETE, etc., y también permite agregar headers y parámetros a las peticiones. Además, Postman permite guardar las peticiones como colecciones para poder reutilizarlas en el futuro.

Insomnia: Similar a Postman, Insomnia es una aplicación de escritorio que permite enviar peticiones HTTP a APIs y analizar las respuestas. Una de las características interesantes de Insomnia es que permite crear entornos, lo que facilita la gestión de diferentes configuraciones para diferentes entornos (desarrollo, producción, etc.).

Swagger: Swagger es una herramienta para diseñar, construir y documentar APIs. Permite crear especificaciones de la API en formato JSON o YAML, que pueden ser utilizadas por otras herramientas para generar la documentación, el código cliente y el servidor.

Newman: Newman es una herramienta de línea de comandos que permite ejecutar colecciones de Postman. Esto es útil si se desea integrar las pruebas de la API en un sistema de integración continua o si se desea automatizar las pruebas.

### Entorno de desarrollo local
Mi entorno de desarrollo local incluiría las siguientes herramientas:

Visual Studio Code: Un editor de código fuente con soporte para múltiples lenguajes de programación y extensiones que permiten agregar nuevas funcionalidades.

Docker: Utilizaría Docker para crear contenedores de la aplicación y de la base de datos. Esto facilita la configuración del entorno de desarrollo y asegura que todos los desarrolladores estén trabajando con el mismo entorno.

Laravel Valet: Valet es una herramienta de desarrollo web para macOS que permite crear un servidor web local y configurar rápidamente los sitios web.

Postman: Utilizaría Postman para probar las APIs durante el desarrollo.

GitHub Desktop: Para manejar el control de versiones, utilizaría GitHub Desktop.

Nuxt o Next: Dependiendo de si se decide utilizar una sola instancia o varias, se utilizaría Nuxt o Next para implementar los microfrontends.

En resumen, con estas herramientas podría tener un entorno de desarrollo local rápido y fácil de configurar, lo que me permitiría enfocarme en el desarrollo de la aplicación.


### Suposiciones surgidas
Durante el desarrollo del plan, surgieron algunas suposiciones que se deben tener en cuenta:

- Se espera que la API de currency se mantenga estable durante el desarrollo del proyecto.
- Los desarrolladores tendrán un conocimiento sólido de las herramientas y tecnologías mencionadas en el plan.
Se tendrán en cuenta los posibles costos adicionales asociados con el uso de herramientas y servicios externos.

- Suponiendo que se trabajará con el equipo de derecho interno de la empresa y que no se cuenta con un presupuesto ilimitado para el proyecto, es importante considerar que habrá limitaciones en términos de recursos financieros y humanos disponibles. Por lo tanto, se deberá priorizar cuidadosamente los requisitos y funcionalidades del proyecto para asegurar que se cumplan los objetivos principales dentro de los límites presupuestarios y de tiempo. Esto puede implicar la eliminación o la postergación de ciertas características no esenciales, así como la búsqueda de soluciones rentables y eficientes para la implementación del proyecto.
Para escribir una lista en Markdown, se pueden utilizar dos formatos: el formato con viñetas (con asteriscos, guiones o signos más) y el formato numerado (con números seguidos de un punto). 
 - Se considerará el uso de una sola instancia de la aplicación para todos los países, ya que esto simplifica la gestión de la aplicación y reduce los recursos necesarios para su mantenimiento. Además, se utilizarán microfrontends para separar la lógica del front-end, lo que permitirá tener diferentes interfaces de usuario para cada país sin necesidad de crear diferentes instancias de la aplicación.
