# Dynamic Modeling Plants/Hare/Lynx
This code describes a three-species ecological food chain using a system of ordinary differential equations (ODEs). The model tracks the rate of change in the population sizes of plants (dydt[0]), hares (dydt[1]), and lynx (dydt[2]) over time

## The Model
Plants: Grow independently up to a natural carrying capacity (logistic growth) but are continuously grazed by hares.
Hares: Grow solely by consuming plants. Their population decreases through natural mortality and by being hunted by the lynx.
Lynx: As apex predators, they grow strictly by consuming hares and decline solely through natural mortality.

The predator-prey interactions follow a "Holling Tanner" model. This means predators cannot eat infinite amounts of prey; their consumption slows down as they get "full". Also the hares get full at one point and will stop grazing. 

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


