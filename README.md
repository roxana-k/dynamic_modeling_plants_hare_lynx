# Dynamic Modeling Plants-Hare-Lynx
This code describes a three-species ecological food chain using a system of ordinary differential equations (ODEs). The model tracks the rate of change in the population sizes of plants (dydt[0]), hares (dydt[1]), and lynx (dydt[2]) over time.

## The Model
Plants: Grow independently up to a natural carrying capacity (logistic growth) but are continuously grazed by hares.
Hares: Grow solely by consuming plants. Their population decreases through natural mortality and by being hunted by the lynx.
Lynx: As apex predators, they grow strictly by consuming hares and decline solely through natural mortality.

The predator-prey interactions follow a "Holling Tanner" model. This means predators cannot eat infinite amounts of prey; their consumption slows down as they get "full". Also the hares get full at one point and will stop grazing. 

### Parameters 
The code involves several parameters. 

#### General parameters
t: time in months. 
y: The state vector containing the current populations of [plants, hares, lynx].

#### The b parameters refer to how full the two animals are 
They determine how quickly the hares (b1) and lynx (b2) get full. 
Higher values mean the animals reach satiation faster, capping their maximum consumption rate.

#### The a parameters refer to 'how efficient [animal] is at eating ___'
a1 is how effectively hares hunt plants.
a2 is how effectively lynx hunt hares.

#### The d parameters refer to the deaths
The natural death rates of the hares (d1) and lynx (d2), independent of predation.


