## ***Construyendo un paquete ROS***

Si queremos construir un paquete ROS e instalarlo directamente podemos usar el comando catkin_make:

    $ catkin_make [make_targets] [-DCMAKE_VARIABLES=...]

Esto sería lo mismo que ejecutar la siguiente ristra de comandos:

    $ mkdir build
    $ cd build
    $ cmake ..
    $ make
    $ make install  # (optionally)
    
Para más info ejecutar:

    $ catkin_make --help
