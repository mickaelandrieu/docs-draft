# Processes

Procesos relativos a Bamboo. Cada uno de estos capítulos tiene el siguiente 
formato, teniendo en cuenta que todos los enlaces funcionan teniendo una 
instalación limpia de Bamboo en http://localhost:8000

Given - Premisas y entorno inicial
When - Cual es nuestra acción elemental
Then - Acciones directamente relacionadas que se ejecutan con dicha acción. En 
esta parte también se tienen en cuenta posibles emails mandados y eventos 
lanzados.

## We load any page

Todas las páginas tienen un conjunto de elementos comunes que trataremos de 
explicar a continuación. Dichos elementos pertenecen al propio marco de la 
aplicación, por lo que son aplicables a todas las peticiones.

Given - Como un usuario cualquiera
When - Cuando queremos visitar cualquiera de las páginas disponibles en la 
aplicación
Then - Suceden los siguientes procesos

* La petición es gestionada por la aplicación de Bamboo utilizando las librerías 
de Elcodi
* Se carga el usuario utilizando la información de sesión.
* Se analiza si el usuario, con sus credenciales actuales, puede acceder a la 
página en cuestión. En caso afirmativo, la ejecución continua con normalidad. 
En caso negativo, se hará una redirección hacia la página de login.
* Se cargan algunas variables relativas al usuario cargado
* Se carga el idioma de página, utilizando información del usuario cargado si 
este existe, o trabajando con información almacenada en sesión
* Se carga la moneda de la misma forma que el idioma de la página
* Se procede a cargar la página en cuestión, teniendo en cuenta todas las 
variables de entorno cargadas.

Eventos - 
Emails mandados -
Enlaces de interés -


## We load the home page

La pagina principal suele comportarse como una página de categoría, teniendo en 
cuenta que en dicha página se muestran los productos marcados como `inHome`.

Given - Como un usuario cualquiera
When - Cuando queremos visitar la homepage, http://localhost:8000
Then - Podemos visualizar los n primeros productos

Eventos - 
Emails mandados -
Enlaces de interés -

## We load the product page
## We load the category page
## We register

Given - Como un usuario no registrado ni logead
When - Cuando queremos registrarnos, http://localhost:8000/register
Then - Una vez añadido nuestra información básica y presionado el botón de 
registrarnos, un nuevo usuario es añadido en la base de datos. Es importante 
saber que la contraseña introducida nunca es, bajo ningún concepto, guardada de 
forma plana y desencriptada. La encriptación que se utiliza hace imposible saber 
el password por parte del servidor.

Eventos - 
Emails mandados - Su cuenta se ha creado correctamente
Enlaces de interés -

## We log-in

Given - Como un usuario no registrado ni logead
When - Cuando queremos logearnos, http://localhost:8000/login
Then - Una vez añadido nuestro username y contraseña y presionado el botón de 
entrar, se comprueba que dicho usuario existe en el sistema, se comparan 
contraseñas y en caso que ambas sean la misma, se procede a autenticar al 
usuario para la sesión actual, permitiendo acceder a su zona privada. En caso 
contrario, el usuario será redirigido a la misma página con los errores 
pertinentes.

Eventos - 
Emails mandados -
Enlaces de interés -

## We log-out

Given - Como un usuario registrado y logeado
When - Cuando queremos salir del sistema, http://localhost:8000/logout
Then - Una vez añadido nuestro username y contraseña y presionado el botón de 
entrar, se comprueba que dicho usuario existe en el sistema, se comparan 
contraseñas y en caso que ambas sean la misma, se procede a autenticar al 
usuario para la sesión actual, permitiendo acceder a su zona privada. En caso 
contrario, el usuario será redirigido a la misma página con los errores 
pertinentes.

Eventos - 
Emails mandados -
Enlaces de interés -

## We add a Product in our Cart
## We remove a Product from our Cart
## We add a Coupon in our Cart
## We remove a Coupon from our Cart
## We make a buy, step by step
