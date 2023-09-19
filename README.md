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

<a name="e1">### **3. Crea un contenedor con el nombre 'dam_ubu1'. ¿Cómo puedes acceder a él?**</a>

Con el siguiente comando, especificamos el nombre con el cual queremos crear el contenedor.

> `docker run -it --name dam_ubu1 ubuntu`

Accedemos a él gracias al uso de la variable/opción "it", permitiendo así interactuar con el contenedor.

De la misma manera utilizamos la variables "--name" para que seguidamente nombremos nuestro contenedor.

<a name="e2"></a>### **4. Comprueba qué IP tiene y si puede hacer un ping a google.com**

Primero, hay que actualizar la lista de paquetes con el comando siguiente.

> `apt update`

Ahora, se instala *net-tools*, el cual nos permitirá visualizar nuestra ip

> `apt install net-tools`

> `ifconfig`

Este ultimo nos muestra nuestra IP, siendo esta: 172.17.0.2.

Adicionalmente, con el paquete *iputils-ping*, podemos hacer ping a Google. 

>`apt install iputils-ping`

> `ping google.com`

### **5. Crea un contenedor con el nombre 'dam_ubu2'. ¿Puedes hacer ping entre los contenedores?**

Repetimos el procedimiento del [apartado 3](#e1), y asi creamos el segundo contenedor llamado 'dam_ubu2'.

Igualmente, usamos  el [apartado 4](#e2) para hacer ping con el contenedor, utilizando la IP del contenedor de 'dam_ubu1'.


