## ***Crear un paquete ROS***

Para poder crear un paquete ROS con catkin, la carpeta de nuestro paquete tiene que contener como mínimo 2 ficheros:

    my_package/
    - CMakeLists.txt
    - package.xml

Es decir, en nuestro entorno debemos tener el siguiente orden:

    workspace_folder/        -- WORKSPACE
      src/                   -- SOURCE SPACE
        CMakeLists.txt       -- 'Toplevel' CMake file, provided by catkin
        package_1/
          CMakeLists.txt     -- CMakeLists.txt file for package_1
          package.xml        -- Package manifest for package_1
        ...
        package_n/
          CMakeLists.txt     -- CMakeLists.txt file for package_n
          package.xml        -- Package manifest for package_n

Para empezar vamos al directorio que creamos como nuestro workspace de catkin:

    $ cd ~/catkin_ws/src

Y ejecutamos el siguiente comando:

    $ catkin_create_pkg beginner_tutorials std_msgs rospy roscpp

Esto nos crea la carpeta beginner_tutorials, indicando que tiene 3 dependencias: std_msgs rospy y roscpp, y creando los dos archivos necesarios en cualquier paquete catkin.

Ejecutamos el make para crear el paquete:

    $ catkin_make
    
Añadimos el workspace al entorno ROS:

    $ . ~/catkin_ws/devel/setup.bash

Y ya estaría.

En el tutorial hay varias cosas extra para visualizar dependencias o modificar nuestro package.xml, pero no lo veo de importancia para ponerlo aquí así que quien quiera puede ir a http://wiki.ros.org/ROS/Tutorials/CreatingPackage y leerlo.

