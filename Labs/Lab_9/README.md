The goal of the lab 9 is to write a local-search algorithm (eg. an EA) able to solve the *Problem* instances 1, 2, 5, and 10 on a 1000-loci genomes, using a minimum number of fitness calls.

To solve this problem i decided to implement the Island model. 
I wrote 3 different functions to select the parents from which to create children: 
*select_parent*, *roulette_wheel_selection*, *elitism_selection*. 

I wrote 4 different functions for the mutation: 
*mutate_one*, *mutate_add_one* (where i add change the value to 1 in different random positions), *mutate_copy* (where i copy the value of a random position in 10 consecutive positions) and *mutate_two*.

In the *migrate* function some individuals from the islands are chosen and "migrate" to other islands. This procedure helps diversify the population. The migrate function is called at every generation. For each island, some individuals are selected (migrants_each) who are then added to the population of other islands. To select the individuals to migrate I have used the choice function to randomly select individuals.

I wrote different xover functions: *one_cut_xover*, *two_cut_xover*, *three_cut_xover*, *uniform_xover*

*Islands* is the array containing the different islands with different population.

With this model using the *roulette_wheel_selection*, a random mutation function and a random xover function, with 
POPULATION_SIZE = 50, OFFSPRING_SIZE = 10, MUTATION_PROBABILITY = 0.2, MUTATION_TRESHOLD = 0.2, TOURNAMENT_SIZE = 2, NUM_LOCI = 1000, NUM_ISLANDS = 100, MIGRANTS_EACH = 5, NUM_GENERATIONS = 500
- with the *Problem* instances 1 i can reach the fitness value = 1 with about 1000000 fitness calls
- with the *Problem* instances 2 i can reach the fitness value = 0.568 with about 1000000 fitness calls
- with the *Problem* instances 5 i can reach the fitness value = 0.4147 with about 1000000 fitness calls
- with the *Problem* instances 10 i can reach the fitness value = 0.2744 with about 1000000 fitness calls


