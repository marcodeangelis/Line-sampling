## The state of the art of line sampling simulation.

*Line sampling* is popular reliability method [1] derived from early development based on directional sampling [2-4] for the purpose of computing efficiently the probability of rare events in a simulation model. .

Monte Carlo simulation methods have been hugely successful in solving the probability forward propagation problem for numerous reasons, including the ability to deal with high-dimensional problems, and highly non-linear black-box problems. The sampling generating mechanism draw variates of the underlying process' probability distribution turning the mathematical problem into a simulation one. While this mechanism is the key to the success of this methods, it also introduces a limitation: because the underlying process is simulated, rare events may require an enormous number of replicates, which can make the methods inefficient.

Importance sampling and other advanced sampling schemes were developed to defeat this limitation [5-7], by tricking the sampling generating mechanism to produce samples in the targeted regions of the probability space where the rare event holds  with very low probability of occurrence.

*Line sampling* falls in the category of advanced Monte Carlo simulation method [8-9]. Samples are arranged on a whole number of one-dimensional manifolds (lines) produced by the sampling generating mechanism to cover the region of the probability space responsible for a targeted rare event. The method is commonly implemented with a static semi-deterministic generating mechanism, which is set by the analyst a priori (<font color="red">ref</font>). This mechanism is univocally identified by an important direction, i.e. a unit vector array carrying the same dimension of the probability distribution (dimension=number of random variates) pointing towards the region of interest (<font color="red">ref</font>).

Non-standard implementations of the method can work with dynamic sampling generating mechanisms that twist around the geometry of the region of interest, and with adaptive self-updating important directions, as well as can provide sensitivity measures of the target probability.

With non-standard implementations, *line sampling* has demonstrated to be a strong contender of the very popular methods for advanced Monte Carlo simulation,
such as subset simulation and importance sampling.

In this book chapter we review the state-of-the-art software [10] and methods that implement this powerful reliability simulation tool, and show their performance when applied to famously difficult reliability test case problems [11]. 
Applications of Line Sampling for performing sensitivity analysis and reliability-based optimisation are also presented [12-13]

References
1.	Schuëller GI. Computational stochastic mechanics – recent advances. Computers and Structures 2001,79, 2225-2234.
2.	Bjerager P. Probability integration by directional simulation. J Eng Mech 1988;114(8):1285- 1302. 
3.	Harbitz A. An efficient sampling method for probability of failure calculation. Structural Safety 1986;3:109-115. 
4.	Bucher CG. Adaptive sampling – an iterative fast Monte-Carlo procedure. Structural Safety 1988;5:119-126. 
5.	Schuëller, G.I. and Pradlwarter, H.J. and Koutsourelakis, P. S. A critical appraisal of reliability estimation procedures for high dimensions, Probabilistic Engineering Mechanics, 2004, 19(4), 463-474
6.	Au, S. K. & Beck, J. L, Important sampling in high dimensions, Structural Safety, 2013, 25, 139-163
7.	Au, S.K., Patelli, E., 2016. Subset Simulation in finite-infinite dimensional space. Reliability Engineering & System safety 148, 66–77. 
8.	Koutsourelakis, P.S. and Pradlwarter, H.J. and Schuëller, G.I., Reliability of structures in high dimensions, part I: algorithms and application, Probabilistic Engineering Mechanics 2004, 19(4), 409-717 
9.	de Angelis, M., Patelli, E., Beer, M., 2015. Advanced line sampling for efficient robust reliability analysis. Structural safety 52, 170–182.
10.	Patelli, E., George-Williams, H., Sadeghi, J., Rocchetta, R., Broggi, M., Angelis, M. de, 2018. OpenCossan 2.0: an efficient computational toolbox for risk, reliability and resilience analysis, in: Beck, A.T., Souza, G.F.M. de, Trindade, M.A. (Eds.), Proceedings of the Joint ICVRAM ISUMA UNCERTAINTIES Conference.
11.	Rozsas A., Slobbe A. (2019). Repository and Black-box Reliability Challenge 2019. https://gitlab.com/rozsasarpi/rprepo/.
12.	M.A. Valdebenito, H.A. Jensen, H.B. Hernández, L. Mehrez, Sensitivity estimation of failure probability applying line sampling, Reliability Engineering & System Safety, 171, 2018, 99-111,
13.	Zhenzhou Lu, Shufang Song, Zhufeng Yue, Jian Wang, Reliability sensitivity method by line sampling, Structural Safety, 30(6), 2008, 517-532,
