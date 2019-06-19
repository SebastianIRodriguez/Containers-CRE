Esta es una primera aproximacion a docker donde primero crearemos un container individual desde una imagen bajada desde el servidor de docker, oportunamente llamado DockerHub, para luego crear nuestro propia imagen con el codigo provisto y crear un container con este.

Levantar un container para ejecutar una tarea:

Vamos a correr el comando ls desde un container con alpine que es una distribucion de linux para ver los contenidos de la raiz en el container.

Para eso vamos a correr 'docker container run alpine ls'.

Ese ultimo comando contiene varias cosas. 'docker' es el comando principal que se escribe para pasarle instrucciones a docker. Una de esas instrucciones es 'container' que permite administrar los containers y dentro de esa instruccion podemos especificar una subinstruccion para administrarlos que es 'run'.

'run' basicamente corre una instruccion en un nuevo container. De esta forma 'run' simultaneamente crea un nuevo contenedor con la imagen que le pasamos como parametro 'alpine' y corre una instruccion que le pasamos como segundo parametro, en este caso 'ls'.


Luego de correr este comando vamos a ver que docker bajo la imagen oficial desde la pagina y que creo el container para por ultimo correr el comando ls y mostrar la estructura del directorio en la raiz del container.

Podemos ver corriendo 'docker container ls --all' que nuestro container sigue vivo y con un estado que nos indica que ya no se esta utilizando. Ademas, podemos ver que nuestro  container tiene un id y una imagen asociados; en este caso la imagen es alpine.

Correr un container interactivo de ubuntu:

Para este ejemplo vamos a correr una sesion de bash desde un container levantado con una imagen de ubuntu. Para eso vamos a utilizar nuevamente el comando 'run' del ejemplo anterior con un par de parametros extras.

Vamos a correr 'docker container run --interactive --tty --rm ubuntu bash'. 

Este comando utiliza los parametros 'interactive', 'tty' y 'rm'. Estos parametros en orden son:
    - Interactive relaciona el input producido desde el teclado del host con la entrada del container para la sesion de bash
    - Tty muestra, como estamos acostumbrados, el usuario actual tanto como el directorio haciendolo mas parecido aun a una terminal corriente
    - Rm elimina el container luego de terminar la sesion. De esta forma no se vera mas al correr 'docker container ls --all'

Luego de eso podemos correr un par de comandos sobre el nuevo container que instanciamos:
    - 'ls /' nos mostrara lo mismo que previamente hicimos para alpine
    - 'ps aux' nos muestra todos los procesos corriendo actualmente en el contenedor
    - 'cat /etc/issue' nos va a mostrar la distribucion de linux sobre la que estamos

Este ultimo ejemplo es especialmente util ya que de esta manera podemos ingresar a un contenedor, configurar todo el entorno para nuestra aplicacion, administrar las dependecias requeridas y testear la aplicacion; y una vez que tenemos el contenedor como queremos podemos generar una imagen desde este y de esta forma distribuir libremente la imagen para que puedan utilizar tu aplicacion y tener el mismo container.

Correr un contenedor en background:

Esta va a ser la manera en que vamos a correr la 