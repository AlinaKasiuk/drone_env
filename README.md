# The modified drone environment that actually installs with pip (Still has some bugs)

_I am working on a task of visulal field coverage with drones using Deep Reinforcement learning. 
So I need to code the implementation of my algorithm.
As I see for that task I will need to create my custom OpenAI gym environment that will describe the area as a simple grid with values but permit me to work with multiple agents._

So this enviroment is one that I just downloaded by mistake using:

```
pip install gym_drone
```

This enviroment uses pybullet module and works with an URDF body _Drone.urdf_
```
self.droneid =p.loadURDF(os.path.join(urdfRootPath, "drone/Drone.urdf"))
```
But I could not find the _Drone.urdf_ itself. 

I downloaded some model from here, added orientation parameters and put it to the _pybullet_data_ folder
https://github.com/mmyself/ros_ardrone/blob/master/ardrone_launch/launch/drone.urdf

It still does not work correctly and this enviroment is not exactly what I am looking for but I fixed some bugs in it and learned something about the constructing enviroments with OpenAI gym and pybullet and I want to temporally save it here because it can help me with my future work.
____

What did I actually wanted to download was _drone_env_ hosted in https://github.com/JNC96/drone-gym#installation.
There I have some problems with registration but I guess it would fit better for my purposes if I could modify it for the multiagend case and change some parameters.
