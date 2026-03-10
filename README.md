# Dynamic Modeling Plants-Hare-Lynx
This code describes a three-species ecological food chain using a system of ordinary differential equations (ODEs). The model tracks the rate of change of the population sizes of plants (dydt[0]), hares (dydt[1]), and lynx (dydt[2]) over time.

## The Model
In this model, plants grow independently up to a natural carrying capacity (logistic growth) but are continuously grazed by hares.
Hares grow solely by consuming plants. Their population decreases through natural mortality and by being hunted by the lynx.
Lynx, as apex predators, grow strictly by consuming hares and decline solely through natural mortality.

The predator-prey interactions follow a Holling Type II model. This means predators cannot eat infinite amounts of prey; their consumption slows down as they get full. Hares also become satiated and therefore stop grazing once their consumption limit is reached. 

## Parameters 
The model uses several parameters for the interactions between plants, hares, and lynx: 

#### General parameters
t: time in months. \
y: the state vector containing the current populations of [plants, hares, lynx].

#### Attack Rate (a)
a1 and a2 represent how effectively hares and lynx respectively hunt (plants and hares).  

#### Satiation constants (b) 
b1 and b2 determine how quickly hares and lynx become satiated.
Higher values mean the animals reach satiation faster.

#### Natural death rates (d) 
d1 and d2 represent the natural death rates of hares and lynx, independent of predation.


