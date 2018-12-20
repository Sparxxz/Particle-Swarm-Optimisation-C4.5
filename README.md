# Optimisation Technique
   ## Particle Swarm Optimisation + C4.5

## Used as Gene Selection Algorithm
- When we work on Gene Datasets usually they contains very high dimension of features which makes it difficult to process.
- But usually all the features aren't requrired for optimal results.
- So Gene Selection Algorithm like  ( PSO+C4.5) is applied to extract the essential features from the pool of all features

### Introduction

- Particle swarm optimization (PSO) is a population based stochastic optimization technique developed by Dr. Eberhart and Dr. Kennedy     in 1995, inspired by social behavior of bird flocking or fish schooling.

- PSO shares many similarities with evolutionary computation techniques such as Genetic Algorithms (GA). The system is initialized with   a population of random solutions and searches for optima by updating generations. However, unlike GA, PSO has no evolution operators     such as crossover and mutation. In PSO, the potential solutions, called particles, fly through the problem space by following the       current optimum particles.


### The algorithm

As stated before, PSO simulates the behaviors of bird flocking. Suppose the following scenario: a group of birds are randomly searching food in an area. There is only one piece of food in the area being searched. All the birds do not know where the food is. But they know how far the food is in each iteration. So what's the best strategy to find the food? The effective one is to follow the bird which is nearest to the food. 

PSO learned from the scenario and used it to solve the optimization problems. In PSO, each single solution is a "bird" in the search space. We call it "particle". All of particles have fitness values which are evaluated by the fitness function to be optimized, and have velocities which direct the flying of the particles. The particles fly through the problem space by following the current optimum particles. 

PSO is initialized with a group of random particles (solutions) and then searches for optima by updating generations. In every iteration, each particle is updated by following two "best" values. The first one is the best solution (fitness) it has achieved so far. (The fitness value is also stored.) This value is called pbest. Another "best" value that is tracked by the particle swarm optimizer is the best value, obtained so far by any particle in the population. This best value is a global best and called gbest. When a particle takes part of the population as its topological neighbors, the best value is a local best and is called lbest.

After finding the two best values, the particle updates its velocity and positions with following equation (a) and (b).

v[] = v[] + c1 * rand() * (pbest[] - present[]) + c2 * rand() * (gbest[] - present[]) (a)
present[] = persent[] + v[] (b)

v[] is the particle velocity, persent[] is the current particle (solution). pbest[] and gbest[] are defined as stated before. rand () is a random number between (0,1). c1, c2 are learning factors. usually c1 = c2 = 2. 
