MDP is represented by a tuple M: (P, R), where P: S x A - > distribution(A) is the transition matrix and R: S x A -> [0, 1] is the reward function

opt methods should be implemented as classes with a step function. 
the step function should take the form step(M, current_policy) -> (next_policy, relevant stats). 
in other words step function should take one iteration of the optimization method and output the updated policy alongside any relevant stats for quantitative analysis (convergence rate etc.)

then we can write one general optimize() function which takes in an MDP, an initialized optimization method, and some sort of stopping condition (epsilon for relative improvement?)