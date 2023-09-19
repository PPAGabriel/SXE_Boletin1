# PRÁCTICA: DOCKER - COMANDOS BÁSICOS

### **1. Descarga la imagen 'ubuntu y comprueba que está en tu equipo:**

En el siguiente apartado, es necesario aplicar el siguiente comando en la terminal.

> `docker run ubuntu`

De esta manera, si la imagen no es encontrada, la descargará automáticamente. Una manera de comprobar que la imagen fue  descargada exitosamente con el siguiente comando.

> `docker image ls -a`

>[!NOTE]
>*Cabe destacar: el hecho de descargar la imagen y que corra, no implica que este abierto para recibir comandos en consola.*

### **2. Crea un contenedor sin ponerle nombre. ¿Está arrancado? Obtén el nombre**

Para crear el repositorio, previamente empleamos el mismo comando.

> `docker run ubuntu`

Ahora bien, al no especificar un nombre ni que este sea arrancado, se mantiene en segundo plano. Por ende, empleamos el siguiente comando para ubicar todos los contenedores creados.

> `docker ps -a`

Un pequeño ejemplo de cómo muestra el siguiente comando es el siguiente

| CONTAINER ID  | IMAGE | COMMAND | CREATED | STATUS | PORTS | NAMES |
|---------------|-------|---------|---------|--------|------|-------|
|079d6e5b2f1d        |ubuntu | "/bin/bash/"  | 35 minutes ago    | Exited (0) 35 minutes ago    |    | Inspiring_mendel  |

Y, en efecto, el contenedor no está arrancado, y su nombre es "Inspiring_model" ya que lo hace de manera automatica el sistema si no lo especificamos.

### **3. Crea un contenedor con el nombre 'dam_ubu1'. ¿Cómo puedes acceder a él?**

Con el siguiente comando, especificamos el nombre con el cual queremos crear el contenedor.

> `docker run -it --name dam_ubuntu ubuntu`

Accedemos a él gracias al uso de la variable/opción "it", permitiendo así interactuar con el contenedor.

De la misma manera utilizamos la variables "--name" para que seguidamente nombremos nuestro contenedor.

