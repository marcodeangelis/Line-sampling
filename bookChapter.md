## The state of the art of line sampling simulation.

*Line sampling* is a reliability method developed in the late 90s (<font color="red">check</font>) for the purpose of computing the probability of rare events in a simulation model.

Monte Carlo simulation methods have been incredibly successful in solving the probability forward propagation problem for numerous reasons, including the ability to deal with high-dimensional problems, and highly non-linear black-box problems. The sampling generating mechanism draw variates of the underlying process' probability distribution turning the mathematical problem into a simulation one. While this mechanism is the key to the success of this methods, it also introduces a limitation: because the underlying process is simulated, rare events may require an enormous number of replicates, which can make the methods inefficient.

Importance sampling and other advanced sampling schemes were developed to defeat this limitation, by tricking the sampling generating mechanism to produce samples in the targeted regions of the probability space where the rare event holds  with very low probability of occurrence.

*Line sampling* falls in the category of advanced Monte Carlo simulation method. Samples are arranged on a whole number of one-dimensional manifolds (lines) produced by the sampling generating mechanism to cover the region of the probability space responsible for a targeted rare event.  The method is commonly implemented with a static semi-deterministic generating mechanism, which is set by the analyst a priori. This mechanism is univocally identified by an important direction, i.e. a unit vector array carrying the same dimension of the probability distribution (dimension=number of random variates) pointing towards the region of interest.

Non-standard implementations of the method can work with dynamic sampling generating mechanisms that twist around the geometry of the region of interest, and with adaptive self-updating important directions, as well as can provide sensitivity measures of the target probability. With non-standard implementations, *line sampling* has demonstrated to be a valid contender of the very popular methods for advanced Monte Carlo simulation, such as subset simulation and importance sampling.

In this book chapter we review the state-of-the-art software and methods that implement this powerful reliability simulation tool, and show their performance when applied to famously difficult reliability test case problems.
