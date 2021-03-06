# Virtual-Ecosystem

This project aims to simulate evolution of animals (called boids) competing in a ecosystem with regards to vision, speed, size and 'brain' structure. The first objective of the project will be to use reinforcement learning to train boids to look for food and avoid obstacles/traps. Study of the evolution of cooperative behaviour will be the second objective of this project. The third objective would be to simulate specialization by introducing different 'nutrition' needs for different attributes of the boids.

Personal Goals:
Learn and apply reinforcement learning in developing the decision-making process of the boids.
Increase familiarity with usage of classes, matplotlib and pillow(PIL).
Learn to develop graphics and interfaces for this project (potentially using pygame)

Different versions of Boids:

Simple Boid - first version of boids developed. This boid only contains the bare minimum, ie movement, eating, energy meter and collision with other boids. It does not possess any pathfinding or decision-making process. Additionally, the environment is a numpy array and there can only exist 1 environment at any 1 time. Displaying the environment can also be confusing, as the colours will change depending on whether there are boids alive in the environment (matplotlib cmap gives colours based on a gradient). 

Brainy Boid - second version of boids developed (This is still a work in progress). This boid is capable of decision-making and pathfinding and possess vision. It is not capable of directly interacting with other boids (for now), manipulating the environment or reproduction (hence evolution). Environment is represented by a class which record the locations of boids and food within it. Representing the environment in a class allows multiple environments to be set up and for interactions between boids to be theoretically possible. Later on, this boid (maybe) will be capable of preying on other boids and may possess the attribute size.

To do:
1. Implement neural network, test for most successful strategies developed by boids who can learn but possess no vision
    - try manually setting up a neural network node by node first
    - have a look at Q learning algorithm (might use keras)
    - have a look at using NEAT algorithm
2. Add vision of boids
3. Add obstacles into environment
4. Add traps into environment

-in no particular order-
Allow manipulation of food (likely to change the boid to interact with pixels around it)
Add a health bar and allow boids to attack each other
Allow donation of energy between 2 boids
Have 2 types of obstacles/traps, manipulable and non-manipulable 
Add reproduction, have baby phase where boid has limited movement
Add evolution system (maybe have differing energy consumption during baby phase according to attributes passed down from parents)
Add different types of food and different nutrition (not just energy), let size and speed needing different combinations of nutrition
Add memory for boids
Place boids with different strategies within the same environment and observe the results
Sexual reproduction (?)
