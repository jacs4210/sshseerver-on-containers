## Instalación y configuración de servidor SSH en contenedor Docker

Dentro del contenedor es posible hacer la conexión ssh al servidor iniciado que está en el mismo contenedor, de la siguiente manera
ssh <user>@localhost -p <port>

En caso de no cambiar el puerto por defecto, la opción -p <port> sería opcional.

Cuando se quiere evitar que se añada al archivo 'know_hosts', se debe añadir al comando de ssh la opción "**-o StrictHostKeyChecking=no**"

Se debe tener en cuenta que la contraseña que se desee a colocar al usuario root, es una contraseña unicamente como ejercicio, ya que no se considera una buena practica tenerla definida en el dockerfile y tampoco acceder con contraseña y usuario root por ssh. Se debe considerar que el usuario root es aquel dueño de todo en el sistema y puede ocasionar fallos si no se utiliza con responsabilidad.