# INFO6205_525 - SOLVING TRAVELLING SALESMAN PROBLEM USING GENETIC ALGORITHM
## ABSTRACT
To develop the genetic algorithm for solving the Travelling Salesman Problem, we implemented 5 Classes: Genotype, TraversalPath, Population, City and Driver class.
Genotype mainly focus on defining the DNA and how the DNA was translated to real point of locations and the Crossover/ Mutate process. The Population class consists of methods to initialize the population, keeps list of genotypes and base order in which the initial list of cities is generated. TraversalPath contains methods to generate phenotype and methods to calculate fitness score and the distance. Driver class runs the main method to generate the population maintain generations and also contains a method which creates random cities for base order.

## IMPLEMENTATION
1) Considering the Population Class it contains five major methods: Constructor, initializePopulation, sortPopulation, regeneration and crossover. It also contains some other supplement methods like genoTypeComparator and getRandomGenotypeIndex.
• InitializePopulation method is used to initialize the initial population randomly. It creates Genotypes which has a 4-bit string representation of binary number of each city.
• SortPopulation method is used to sort the population based on the fitness score generated for each phenotype.
• Regeneration method is used to generate new population or generation using crossover method by choosing random parents from the population. The population is maintained constant in the process.
• Mutation – the population is sorted based on the fitness function and mutation is induced every 3 generations once on the population where the fitness function is highest.
2) In the Genotype Class, we are using two different constructors two differ the type to initialize a phenotype. The class contains phenotype generation method and compareTomethod.
• Phenotype is generated by converting the 4-bit binary code into index to get the city from the baseOrder ArrayList.
• CompareTo method is used to compare two genotypes.
3) In TraversalPath Class, we are having CalculateFitnessScore and CalculateDistance methods.
• CalculateFitnessScore is used to calculate FitnessScore based on the total distance calculated in CalculateDistance                                   method. FitnessScore is obtained by using the follow formula.
FitnessScore = (1/TotalDistance).
• CalculateDistance method is used to calculate Distance between a pair of cities using the xcoordinate and ycoordinate of the cities.
4) In Driver Class, we have implemented the main function which runs the whole algorithm. Along with the main function generateBaseOrder method is implemented in the driver class.
• Array of Random order of cities and along with (X,Y) coordinate is generated using generateBaseOrder.

## CONCLUSION
Our problem is to find a shortest path to access all the points without duplicate by using genetic algorithm. According to our tests, the genetic algorithm will generate a result which is quite close to the optimal result. In a relative small size of problem (5 locations), the program generates the result which is close to the optimal result (or maybe is the optimal result) in less than 10 generations (rare improvement after that) but in a larger size of problem (15 locations), the program will need more generations to reach a result (the program took around 24 generations)which is close to the optimal.
