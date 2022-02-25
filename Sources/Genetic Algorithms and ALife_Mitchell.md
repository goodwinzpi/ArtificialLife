# Mitchell, Melanie. Genetic Algorithms and Artificial Life. Artificial Life 1: 267-289. 1994. doi: 10.1162/artl.1994.1.3.267
A brief overview of Genetic Algorithms as they apply to evolution and natural selection. Ignoring those fields which use them as a means of creating of controling a useful system.

A simple GA example without inversion:
1. Initialize a random population of chromosomes
2. Calculate the fitness of each chromosome in the population
3. Perform selection and genetic operations to obtain a new population
4. Go to step 2

Selection and genetic operations may take many different forms:
- Remove the lowest fitness 50% of the population (Selection) and duplicate remaining 50% with some genetic drift (genetic)
  - duplicate remaining 50% in proportion to their relative fitness with some genetic drift (genetic)

Genetic Algorithm Applications (Non-Exhaustive):
 - Optimization
 - Automatic Programming
 - Machine and Robot Learning
 - Economic Models
 - Immune System Models
 - Ecological Models
 - Interactions between evolution and learning
 - Models of Social Systems
 - Viruses and Cyber Terrorism
 - Robust-First Computing

### Modeling and Proving the Baldwin Effect
- The Idea that desirable learned traits eventually become hard coded evolved traits as a result of selecting according to the potential of producing the desired trait.
- Hilton and Nowlan
  - Create a Neural network with 20 potential connections which may take values of 0, 1 or ? where ? allows the link to take values of 0 or 1 as a random guess at each time step
  - Goal is to create a specific network
  - Fitness is calculated as inversely to the number of guesses required to reach the correct solution
  - Organisms with more ? links require more guesses while organisms with incorrect links could never be perfectly accurate. There is a trade off between efficiency of fixed links and ability to reach desired outcome with ? links. 
  - Short coming was that guessing as a learning method is far too simple
- Ackley and Littman Evolutionary Reinforced Learning
  - Agents move on a 2D lattice encountering food, hiding places, predators, etc.
  - Agents contain 2 networks, one evaluating how good the agents state is based upon what they can see and the internal energy of the agent and an action network
  - The evaluation network outputs to the action network.
  - The evaluation network has links and weights fixed at birth, determining the agent's needs
  - The weights between the evaluation network and the action network change with a reinforcement learning algorithm throughout the agent's life time

### Ecosystems and Evolutionary Dynamics
- Holland's Echo - Model of ecological systems
  - Focuses on Agent-Agent and Agent-Environment interactions
  - significant due to generality and ambitious scope - flow of resources and competitions amongst networks of agents
  - interactions are based upon an agent's genome and appearance stored in a string tag.
- Measuring Evolutionary Activity - Bedau and Packard - Strategic Bugs
  - Model only contained agents "bugs" moving on a 2D lattice in search of food
  - Bugs could breed asexually or sexually
  - The goal was to define a measure of evolutionary activity over time (informally: "the rate at which useful genetic innovations are absobed into the population" - measured by the persistent use of new genes
  - Bug's genomes are represented as a look-up table with genes being an entry on that table. The number of times a situation arose and was used on the look-up table was easily determined using a counter
    - A gene's counter is passed with the gene. Only new genes are initialized at 0
  - By plotting a dynamic histogram displaying the genes and their usage counters over time, wave like behavior was displayed indicating that genes were constantly being innovated and persistently used before being replaced.
  - defined evolutionary activity A(t) - "roughly measures the degree to which the population is acquiring new and useful genetic material at time t"
    - A(t) > 0 - evolution is occuring at time t
  - Significance lies in defining macroscopic quantity for evolution - in this case too model specific but such a metric is necessary in more complex models  

### Learning Classifier Systems
- Classifier Systems: "based on learning, intermittent feedback from the environment, and hierarchies of interal models that represent the environment"
- Used in models of social and economic behavior, categorizing, and maze running.
- Classifier Systems compute with messages and control their state using if-then statements whcih control the flow of messages
  - Lowest level = performance 
  - second level = credit assignment with bucket brigade
  - highest level = genetic algorithm discovering useful rules (if-then statements)
- Classifier systems allow for the creation of internal models which make predictions with incomplete information while integrating new information

### Immune Systems
- Learning in immune systems occurs using evolutionary mechanisms similar to those in biology
- Immune system models for Forrest er al. involve randomly generated populations of antibodies and antigens
  - antigen recognition is simplified using binary strings to represent complex chemistry
    - used to study detection of common patterns (schema) in noisy environments
    - maintain knowledge of diverse antigen population
    - learning ability with incomplete information 
  - Antigens are held constant and antibodies evolve under a GA in most experiments; sometimes coevolution is permitted
  - antigens are presented sequentially to anitbodies, antibodies whose bits match at many positions accrue fitness

### Social Systems
- GAs are particularly useful inthose models involving the evolution of cooperation
- In Axelrod's experiments evolving strategies for the prisoners dilemma, a GA competed with 8 fixed strategies
  - determined that Gas are good at developing highly specialized adaptations, since they came up with strategies that found specific weaknesses in some of the fixed strategies
- Axelrod's experiments with both populations evolving their strategy
  - Early generations defected often (uncooperative strategies)
  - Later generations learn to evolve strategies which reciprocate cooperation and punish defection (variants of TIT FOR TAT)
- Lindgren's PD experiments were similar to those of Axelrod, but he included noise so that players could make mistakes, an allowed the memory for a given strategy to change dynamically.
  - Result was periods of relative stasis followed by mass extinction

### **Open Problems and Future Directions**
- Suggenstion: How to construct artificial life OR Natural Phenomena
- How do we evaluate artificial life systems? - Criteria and Methods
- It is difficult to retrieve quantitative data from ALife models due to high levels of abstraction from real world quantities.
  - Genetic programming and Messy GAs are supposed to be innovative proposed solutions to this issue
- Mechanisms of rearranging genetic material (from molecular biology)
  - Jumping Genes, gene deletion, duplication, introns, extrons)
- Explicit fitness evaluation is unrealistic, look at coevolutionary, endogenous fitness metrics
