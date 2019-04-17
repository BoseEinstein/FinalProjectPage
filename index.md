## Unnamed Game Engine


## Download!

[Click here to download!](https://drive.google.com/file/d/1PyzGENBetStNtAaP_eVr0y1MNYDckj6W/view?usp=sharing)


## Documentation
[Click here for documentation](Docs/html/index.html)

## Gameplay Trailer


<iframe width="560" height="315" src="https://www.youtube.com/embed/8ErkCVNB56s" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>



## Screenshots

![img1](/images/screenshot1.png)
![img2](/images/screenshot2.png)
![img3](/images/screenshot3.png)


## Game Engine Post Mortem
There were some significant challenges on this project. The primary cause was the use of pybind, the documentation was limited and we were fighting it the whole way through. This primarily impacted the core design of our main game object class. Initially we wanted to have a structure of components that could be iterated through, added to or removed from. Our lack of experience left us unable to properly cast from a generic component type to a specific one to get access to important functions at the python level. This led to the poor design of every game object having one of every comonent whether it needed it or not.

This led into the second largest issue. We initally wanted C++ to call a python update function on every game object, similar to Unity. However the documentation was unclear on how to call specific python functions from withing C++ and what the specific scope/lifetime of those variables would be. After this project I feel I have a better handle on pybind and could implement this feature if given even one more week or even a few days.

There are also some inconsistent seg faults. 9/10 times a script will run fine and then seg fault for no discernable reason. Some more time to hunt down this memory issue would have been appreciated.

### Team Game Makers
- Marcos Lopez
- James Thomas
- Ian Meyers
- Sawyer Warden
