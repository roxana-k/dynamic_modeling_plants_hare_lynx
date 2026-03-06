# Dynamic Modeling Plants/Hare/Lynx
The code describes the rate of change in population over time of plant, hare and lynx. The first derivative dydt[0] over time describes the plant evolution, the second dydt[1] describes the hare's and the last describes the lynxes dydt[2] population. They follow chaotic behavior, since it is a three-species model.


### Parameters 
The code involves several parameters. 

#### General parameters
t: time in months. 
y: vector containing population of plants, hares, and lynx. 

#### The b parameters refer to how full the two animals are 
b1 is the maximum amount of plants that can be eaten.
b2 is the maximum amount of bunnies that can be eaten.

#### The a parameters refer to 'how efficient [animal] is at eating ___'
a1 is the rate of bunnies eating the plants.
a2 is the rate of lynxes eating the bunnies.

#### The d parameters refer to the deaths
d1 is the death of the bunnies (excluding being eaten by lynx).
d2 is the death of the lynxes (only way for lynx to exit the system).


