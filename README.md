# Deber
En esta tarea, hemos implementado y mejorado una API web para gestionar libros, con un enfoque particular en el manejo de excepciones y el envío de mensajes personalizados.

# Modificaciones Realizadas

1. Control de Excepciones

Se implementó una clase global de manejo de excepciones llamada GlobalExceptionHandler. Esta clase captura y maneja las excepciones LibroException que pueden ocurrir cuando se intenta obtener un libro que no existe en la base de datos.

![Control de Excepciones](https://github.com/AslyAlvarezNegrete/Deber-Web-API-de-Libro-con-control-de-excepciones/assets/170276678/81a5465c-2c37-47f2-8634-008eff23566d)

2. Excepción Personalizada (LibroException)

Se creó una excepción personalizada llamada LibroException que se lanza cuando no se encuentra un libro con el ID especificado. Esta excepción permite proporcionar un mensaje detallado sobre el error ocurrido.

![Excepción Personalizada ](https://github.com/AslyAlvarezNegrete/Deber-Web-API-de-Libro-con-control-de-excepciones/assets/170276678/4b899ec7-bdd1-4ac9-9bc8-42faf2b3ccaf)

3. Modificaciones en el Controlador

Se realizaron cambios en el controlador LibroController para manejar correctamente las excepciones y establecer las rutas adecuadas para obtener y crear libros.

![Modificaciones en el Controlador](https://github.com/AslyAlvarezNegrete/Deber-Web-API-de-Libro-con-control-de-excepciones/assets/170276678/f0003361-b12a-4f70-9497-27879b57a65f)

4. Servicio de Libro

Se implementó una lógica de negocio en la clase LibroServiceImpl para manejar la obtención y creación de libros. La excepción LibroException se lanza si no se encuentra un libro con el ID especificado.

![Servicio de Libro](https://github.com/AslyAlvarezNegrete/Deber-Web-API-de-Libro-con-control-de-excepciones/assets/170276678/a0b2d649-c66e-42c5-af3c-2854815ff91d)

# Comprobación
# Obtener un Libro por ID

Se obtiene un libro específico por su ID. Si el libro no se encuentra, se lanza una excepción LibroException y se envía una respuesta con estado NOT_FOUND y un mensaje personalizado.
 
![libro-id](https://github.com/AslyAlvarezNegrete/Deber-Web-API-de-Libro-con-control-de-excepciones/assets/170276678/41080a01-d512-4de4-bcca-db9a37cc6cfc)

# Crear un Nuevo Libro

Se crea un nuevo libro y se envía una respuesta con estado CREATED

![Crear un Nuevo Libro](https://github.com/AslyAlvarezNegrete/Deber-Web-API-de-Libro-con-control-de-excepciones/assets/170276678/8355ec52-eced-424d-98aa-56893cf975fb)

Y para confirmar que se allá creado hacemos un GET consultando la id que creamos, en la siguiente imagen se muestra el resultado:

![Nuevo libro-buscar por id](https://github.com/AslyAlvarezNegrete/Deber-Web-API-de-Libro-con-control-de-excepciones/assets/170276678/9b93dd12-d929-4dd5-9472-cc243af4746e)
