## ***Sistema de ficheros ROS***

Este tutorial nos enseña cómo movernos por el sistema de ficheros de ROS y cómo ejecutar comandos para saber paths, ver contenidos etc.

Lo primero es instalar un paquete de prueba:

    $ sudo apt-get install ros-melodic-ros-tutorials

**COMANDOS:**

  - *ROSPACK:*
    Podemos averiguar el path del paquete.
    
        $ rospack find [package_name]
        $ rospack find roscpp
        
     Debería retornar algo como:
    
        /opt/ros/melodic/share/roscpp
        
   - *ROSCD:*
     Con este comando podemos ir directamente a la carpeta de un paquete:
     
          $ roscd [locationname[/subdir]]
       
   - *ROSLS:*
    Con este comando podemos listar el contenido de una carpeta:
        
        $ rosls [locationname[/subdir]]

Si nos fijamos en el nombre de los comandos, es igual que los típicos de LINUX, ls, cd, find, así que al igual que LINUX, podemos usar el "tabulador" para que autocomplete los nombres de los paquetes.


      
