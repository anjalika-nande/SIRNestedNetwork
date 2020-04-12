# SIRNestedNetwork

This Python code generates the simulations presented in Figure 3 of the manuscript "Crowding dictates the epidemic intensity of COVID-19 transmission across China" by Rader et al. 

**Method summary**: We simulated a simple stochastic SIR model of infection spread on weighted networks created to represent hierarchically-structured populations. Individuals were first assigned to households using the distribution of household sizes in China (data from UN Population Division, mean 3.4 individuals). Households were then assigned to “neighborhoods” of ~100 individuals, and all neighborhood members were connected with a lower weight. A randomly-chosen 10% of individuals were given “external” connections to individuals outside the neighborhood. The total population size was N=1000. Simulations were run for 300 days and averages were taken over 20 iterations. The SIR model used a per-contact transmission rate of 𝛽=0.15 and recovery rate 𝛾=0.1. For the simulations without interventions, the weights were wHH = 1, wNH = 0.01, and wEX = 0.001  for the “crowded” prefecture and wEX = 0.0001 for the “sparse” prefecture. For the simulations with interventions, the  household and neighborhood weights were the same but we used wEX = 0.01 for the “crowded” prefecture and wEX = 0.001 for the “sparse” prefecture. The intervention reduced the weight of all connections outside the household by 75%. 
