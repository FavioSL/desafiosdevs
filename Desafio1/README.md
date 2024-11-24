# Desafio 1
Este desafio está dividio en 2 jobs
1. practica 1 - creacion
2. practica 1 - eliminacion

## Creación job

Este job recibe los siguientes parámetros:

- **login**: ID o nombre de inicio de sesión del usuario.
- **nombre**: Nombre del usuario.
- **apellido**: Apellido del usuario.
- **departamento**: Departamento a escoger.  
  Se utilizó un parámetro de tipo **"choice"** para que el usuario seleccione uno de los departamentos disponibles mediante un **dropdown**.

### Flujo del job

1. El pipeline comienza mostrando los datos del usuario.
2. Genera una contraseña aleatoria para el usuario.
3. Si el usuario no existe, se crea en el sistema y se le asigna la contraseña, esta es regresada al usaurio. 
4. Si el usuario ya existe, el proceso muestra un mensaje indicando que no se puede crear el usuario.


## Eliminar job

# Proceso de Eliminación de Usuario

Este job se encarga de eliminar un usuario que es recibido como parámetro
- **idUsuario**: ID o nombre de inicio de sesión del usuario.

### Flujo del job
1. El pipeline retorna el usuario que llegó como parámetro como un check para el usuario
2. Valida si el usuario existe, para poder eliminarlo, en caso ya existir, termina el ciclo
3. Eliminar el usuario y avisar el usuario

# Requerimientos

El job, al utilizar comandos de alto nivel, se requiere permisos de sudo, por lo que el usuario de jenkins, requiere tener 
permisos para ejecutar los comandos 
1. **`useradd`**: Crear nuevos usuarios en el sistema.
2. **`userdel`**: Eliminar usuarios existentes.
3. **`usermod`**: Modificar los detalles de los usuarios (por ejemplo, agregar a un usuario a un grupo).
