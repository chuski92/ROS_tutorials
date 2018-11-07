
## ***RQT_CONSOLE Y ROSLAUNCH***

- **Rqt_console y rqt_logger_level:**

  Si ejecutamos en 2 consolas diferentes los siguientes comandos:

      $ rosrun rqt_console rqt_console
 
 Con rqt_console obtenemos una consola que nos mostrará el output de cada NODO.

      $ rosrun rqt_logger_level rqt_logger_level

Con rqt_logger_level podemos especificar qué nivel tienen que tener los mensajes de salida para mostrarse en la consola (DEBUG, WARN, INFO, and ERROR)

**Después de tener las consolas entonces podemos ejecutar nuestro paquete.**

- **ROSLAUNCH:**

Este comando nos permite ejecutar un paquete especificando diferentes parámetros sin tener que ponerlos manualmente en la consola.

Para ello hay que crear un archivo launch.xml como el siguiente:

    <launch>

      <group ns="turtlesim1">
        <node pkg="turtlesim" name="sim" type="turtlesim_node"/>
      </group>

      <group ns="turtlesim2">
        <node pkg="turtlesim" name="sim" type="turtlesim_node"/>
      </group>

      <node pkg="turtlesim" name="mimic" type="mimic">
        <remap from="input" to="turtlesim1/turtle1"/>
        <remap from="output" to="turtlesim2/turtle1"/>
      </node>

    </launch>
    
Y al ejecutar:

    $ roslaunch beginner_tutorials turtlemimic.launch

Nos creará dos tortugas, cada una en ventanas separadas.

Para crear un grafo que nos muestre sus relaciones ejecutar:

      $ rqt_graph
