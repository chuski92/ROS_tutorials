## ***Instalación y configuración del entorno ROS***

Lo primero es seguir las indicaciones para instalar ROS:
http://wiki.ros.org/melodic/Installation

Para UBUNTU:
 Ejecutar los siguientes comandos:
 
    sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
    sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 421C365BD9FF1F717815A3895523BAEEB01FA116
    sudo apt update
    sudo apt install ros-melodic-desktop-full

  Instalar Rosdep:
  
    sudo rosdep init
    rosdep update
    
Para que no se tenga que ejecutar este comando cada vez que abras un terminal, lo añadimos al bashrc:

    echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
    source ~/.bashrc
    
Instalar dependencias:
    
    sudo apt-get install python-rosinstall python-rosinstall-generator python-wstool build-essential

Ahora crearemos un area de trabajo de catkin:


    mkdir -p ~/catkin_ws/src
    cd ~/catkin_ws/
    catkin_make
    source devel/setup.bash
    
Hay que comprobar que está correcto en el path:


    echo $ROS_PACKAGE_PATH
    
Debería salir algo como lo siguiente:

    /home/youruser/catkin_ws/src:/opt/ros/kinetic/share

