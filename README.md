# Patron_MVC_con_Symfony

Para la solución al ejercicio de probar un framework que utilice el patron MVC e implementarlo en una aplicación básica, se usa el framework Symfony.

El framework symfony se basa en un pratron clásico de diseño web conocido como arquitectura MVC, que está formado por tres niveles.

* El modelo: El Modelo representa la información con la que trabaja la aplicación, es decir, su lógica de negocio.
* La Vista transforma el modelo en una página web que permite al usuario interactuar con ella.
* El Controlador se encarga de procesar las interacciones del usuario y realiza los cambios apropiados en el modelo o en la vista.

En este caso el modelo se representa como una entidad y al crear el modelo se crea en una carpeta llamada entity

![alt text](https://firebasestorage.googleapis.com/v0/b/restaurant-687a2.appspot.com/o/Symfony%2F1.PNG?alt=media&token=79d6f1d6-9bd5-4fde-a95e-6c8d7df13b40)

El modelo contiene los metodos que se encargan de obtener y cambiar el valor de los datos de la base de datos.

![alt text](https://firebasestorage.googleapis.com/v0/b/restaurant-687a2.appspot.com/o/Symfony%2F2.PNG?alt=media&token=8bf3bfe6-5435-4c40-916d-7c8ea9ba09f7)

Luego está el controlador, el controlador es donde se crea el codigo que liga la logica de negocio(El modelo) con la presentación(La vista).

![alt text](https://firebasestorage.googleapis.com/v0/b/restaurant-687a2.appspot.com/o/Symfony%2F3.PNG?alt=media&token=bd124864-acf6-4c57-857c-736324527d48)

Dentro del controlador se encuentran las funciones: 

* index: Esta funcion se encarga de obtener los datos de la base de datos y mostrarlos en la vista al usuario.

En el siguiente codigo, le estamos diciendo que en una variable llamada $data obtenga los datos de nuestra entidad por medio de un objeto Doctrine llamado getRepository y le pasamos el nombre de la entidad o el modelo y le decimos al final que muestre todos los registros.

Estos registros se nos mostraran en una vista que esta dentro de una carpeta llamada main y un fichero llamada index.

![alt text](https://firebasestorage.googleapis.com/v0/b/restaurant-687a2.appspot.com/o/Symfony%2F4.PNG?alt=media&token=413a7f81-110b-4a13-aec7-29786c55642b)

Las vistas se crean dentro de una carpeta llamada Templates.

Como se pude ver ya hay varias vistas creadas, la vista index muestra los datos de la base de datos, mediante la funcion que hicimos en el metodo index del controlador.

![alt text](https://firebasestorage.googleapis.com/v0/b/restaurant-687a2.appspot.com/o/Symfony%2F5.PNG?alt=media&token=c53e99eb-0b4a-405e-a9f0-34d9c00759df)

Dentro de la vista index creamos una tabla para mostrar nuestros registros, creamos un ciclo for para recorrer los registros de la base de datos en una varible llamada data en nuestra lista.

![alt text](https://firebasestorage.googleapis.com/v0/b/restaurant-687a2.appspot.com/o/Symfony%2F6.PNG?alt=media&token=85c01504-bc11-414e-bdd0-b9d3f9d34b40)

![alt text](https://firebasestorage.googleapis.com/v0/b/restaurant-687a2.appspot.com/o/Symfony%2F7.PNG?alt=media&token=756a6598-7ff1-4f74-9c72-df8f391ab1ab)

Mas abajo podemos ver los botones que se encargan de las acciones de actualizar y eliminar con sus rutas, estas se crean en el controlador a como se ve a continuación:

Esta es la funcion para crear un nuevo registro:

![alt text](https://firebasestorage.googleapis.com/v0/b/restaurant-687a2.appspot.com/o/Symfony%2F8.PNG?alt=media&token=081131a4-49b3-4155-bac4-da0eec632da7)

Esta es la funcion para modificar un registro:

![alt text](https://firebasestorage.googleapis.com/v0/b/restaurant-687a2.appspot.com/o/Symfony%2F9.PNG?alt=media&token=8d3c1abb-f965-4c30-a793-b35ff0a412e6)

Y está es la funcion para eliminar un registro:

![alt text](https://firebasestorage.googleapis.com/v0/b/restaurant-687a2.appspot.com/o/Symfony%2F10.PNG?alt=media&token=166bb5bd-9708-4428-9900-a13bfe8aa32c)

Las demas vistas con las que interactua el usuario son estas:

La vista princial, el index que se encarga de mostrar los datos: 

![alt text](https://firebasestorage.googleapis.com/v0/b/restaurant-687a2.appspot.com/o/Symfony%2F11.PNG?alt=media&token=3a726fbd-04ca-402c-b0f0-0c85e9c3ec70)

La vista update para actualizar los registros:

![alt text](https://firebasestorage.googleapis.com/v0/b/restaurant-687a2.appspot.com/o/Symfony%2F12.PNG?alt=media&token=bee9e192-bbb3-41f3-8730-632286938596)

Y para eliminar simplemete usamos el boton eliminar ya que solamente se usa el ID del registro.

Em conclucion Symfony como en otros frameworks se basa en el patron MVC y funciona de manera que un usuario ingresa a una aplicación y hace una peticion mediante una ruta, cuando se realiza la peticion, esta se envia a un controlador, el controlador se encarga de recuperar los datos a travez del modelo(entity), el modelo devuelve los datos al controlador y el controlador envia los datos a la vista(Twig), la vista crea o muestra la pagina HTML con los datos formateados, por ejemplo en una tabla, la vista devuelve el HTML al controlador y el controlador devuelve una pagina al usuario.