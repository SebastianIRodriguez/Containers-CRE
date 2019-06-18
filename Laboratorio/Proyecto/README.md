En este proyecto existen dos carpetas llamadas: api y web.
Estas dos carpetas corresponden al codigo de dos microservicios que se quieren lanzar simultaneamente
en dos contenedores distintos. Para ello rellena el codigo en los dockerfile presente en cada una de 
las carpetas y completa el docker-composer.

El docker-composer es una nueva herramienta que se integra a docker que permite generar varios containers
a la vez en forma de microservicios y los 'pega con goma' para asi generar la aplicacion final que utilice
varios containers
