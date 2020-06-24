# Examen para Certificación de Desarrolladores QR Vendedor de Mercado Pago (modelo atendido)
--------------------------------

¡Bienvenido al examen de certificación de integración QR Vendedor (modo atendido) de Mercado Pago!

Queremos que formes parte de nuestra comunidad de desarrolladores certificados y para ello te invitamos a que realices este examen.

Para lograr obtener esta certificación será necesario que desarrolles un ejercicio práctico y funcional implementando este ejemplo que simula ser un Softwade de Punto de venta que permite crear una sucursal, una caja y una orden, así como validar el pago de la misma, cumpliendo con los estándares de calidad de nuestro equipo de integraciones.

Desde Mercado Pago validaremos tus respuestas para determinar si se cumplió con lo solicitado en el ejercicio. Te recomendamos leer este documento en su totalidad antes de comenzar.

Conocimientos técnicos necesarios:
----------------------------------
- Front End: HTML, JavaScript/JQuery
- Backend: PHP (aunque podrías adaptar fácilmente el código a otros lenguajes a tu elección)
- Servidores: Configuraciones básicas para puesta en marcha de un servicio web en el lenguaje de backend que elijas.
- Interacción con API REST
- GitHub

Requerimientos técnicos:
------------------------
- Necesitarás subir el ejercicio a un servidor como Heroku o algún servidor que permita disponibilizar estos archivos públicamente en internet. El desarrollo tendrá una parte de front y otra parte de back.
- El lenguaje del código Backend de este ejercicio está desarrollado en PHP pero lo hemos hecho para que puedas adaptarlo fácilmente a cualquier otro lenguaje de programación.

Documentación técnica:
----------------------
Requisitos previos:
https://www.mercadopago.cl/developers/es/guides/qr-code/general-considerations/pre-requisites/

Sucursales y cajas:
https://www.mercadopago.cl/developers/es/guides/qr-code/general-considerations/stores-pos/

Introducción QR Vendedor modo atendido:
https://www.mercadopago.cl/developers/es/guides/qr-code/qr-attended/qr-attended-part-a/

Integrar el modo atendido:
https://www.mercadopago.cl/developers/es/guides/qr-code/qr-attended/qr-attended-part-b/

Video-tutoriales:
https://www.youtube.com/playlist?list=PLCazXKuqZp3hGVY3bBhEO0ItFhIic5UpK

Ejercicio
---------

Este ejercicio se basa en hacer funcional el ejemplo que compartimos en este repositorio y que funcione de forma completa desde un servidor Web público, puede ser basado en Heroku o cualquier otra plataforma.

¿Qué debe hacer este ejercicio?

1) Permitir crear una sucursal
   El external_id de la sucursal deberá ser: [suc]+[número de DNI sin puntos ni rayas]+[número correlatvo por cada prueba 001], por ejemplo: suc218545556001
2) Permiir crear un POS/QR
   El external_id del pos deberá ser: [pos]+[número de DNI sin puntos ni rayas]+[número correlatvo por cada prueba 001], por ejemplo: pos218545556001
3) Peritir crear una orden asignada a un POS/QR
4) Crea una orden y simular un pago rechazado mediante la tarjeta de crédito "American Express" y acto seguido usar otro medio de pago y usar la tarjeta de crédito Master Card para lograr un pago exitoso. Ver (*)
   El external_reference deberá ser [ref]+[tu número de DNI sin puntos ni rayas]+[número correlatvo por cada prueba 001], por ejemplo: ref218545556001
5) Escuchar las notificaciones para confirmar el pago de la orden.
6) Escuchar el servicio merchant_orders para confirmar el pago de la orden
   
Los JSON resultantes de las llamadas del ejercicio deberás copiarlos y pegados en el formulario de validación del ejercicio.

Para que todo ello funcione deberás comprobar de realizar los cambios o los añadidos necesarios en el código para que todo funcione.

Dentro del código encontrarás comentado mediante el título // REVISA AQUÍ: las acciones que deberás revisar.

Esto principalmente será en los archivos:

/assets/js/acme.js
/api/ (revisar todos los index.php y functions.php que contiene algunas variables globales)


En este video  te mostramos un flujo completo de cómo debería ser el resultado de la prueba:
VIDEO


Validación del ejercicio
------

Una vez realices el ejercicio completo y sea funcional deberás cumplimentar el siguiente formulario:

https://bit.ly/examen-QR-Vendedor-MP

La respuesta del resultado del ejercicio será inmediato. 

Si no apruebas recibirás un correo en el que te indicaremos dónde cometistes los fallos para que puedas volver a repetirlo, en caso de aprobar el examen estarás automáticamente certificado en esta modalidad. Al cabo de unos días recibirás un correo que te daría acceso a nuestra comunidad en Slack para desarrolladores certificados en inStore, así como te enviaremos el certificado y tu integrator-id (en caso de no tenerlo).


Credenciales de usuarios de TEST para las pruebas:
--------------------------------------------------

Credenciales para ejercicio en ARGENTINA:

VENDEDOR:
- access_token: APP_USR-7026946692817220-061822-8b7c9e20631faac22d9e4cfa92a37265-586728271
- collector_id: 586728271
- country_id: MLA

COMPRADOR (para usar desde la app de Mercado Pago):
- email: test_user_66671705@testuser.com
- password: qatest3881



(*) Tarjetas de crédito para pruebas: 
---------------------------------
https://www.mercadopago.com.ar/developers/es/guides/qr-code/final-steps/integration-test/#bookmark_tarjetas_de_prueba

