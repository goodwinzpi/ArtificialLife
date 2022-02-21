# ChromosomeOrganism
The ChromosomeOrganism is a python object containing the following basic properties:
1. It contains an ordered list of chromosomes or genetic code 
  - initialized from some finite alphanumeric set.
  - Contains items only in that alphanumeric set
2. It begins with a fitness score of 0
3. It has a method for breeding with different ChromosomeOrganisms of the same variety such that: 
  - the resultant organisms vary in genetic code from their parents
  - and eachother in the case of multiple resultant organisms
4. It has a method for selecting a breeding partner which is:
  - dependent upon the fitness of both organisms 
  - they will be more likely to mate the higher their combined fitness.  
