## ***ROS SERVICES & PARAMETERS ***

**COMANDOS:**

- ROSSERVICE:

    Con este comando podemos ver información acerca de nuestro paquete o llamar a un servicio presente.

       $ rosservice list         print information about active services
       $ rosservice call         call the service with the provided args
       $ rosservice type         print service type
       $ rosservice find         find services by service type
       $ rosservice uri          print service ROSRPC uri

- ROSPARAM:
  
  Con este comando podemos manipular parámetros de nuestro paquete durante su ejecución.

      rosparam set            set parameter
      rosparam get            get parameter
      rosparam load           load parameters from file
      rosparam dump           dump parameters to file
      rosparam delete         delete parameter
      rosparam list           list parameter names
      
      
Para ver gráficamente la relación y profundizar más, podemos ir a http://wiki.ros.org/ROS/Tutorials/UnderstandingServicesParams y seguir los pasos allí descritos.
