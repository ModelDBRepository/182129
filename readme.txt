Model files in the NEURON simulation environment from the paper:
"Computational modeling of inhibitory transsynaptic signaling in hippocampal and cortical neurons expressing intrabodies against gephyrin"
by Lupascu CA, Morabito A, Ruggeri F, Parisi C, Pimpinella D, Pizzarelli R, Meli G, Marinelli S, Cherubini E, Cattaneo A, Migliore M
Frontiers in Cellular Neuroscience, 2020, in press

Compile the mod files with mknrndll (mswin or graphical mac) or nrnivmodl (unix/linux). 

To run the fitting procedure:

1) on all the traces of the dataset "exp5" using 100 different initial parameter values 
(uniformly randomized within a large, 5 orders of magnitude, range) and up to 3000 iteration steps for each run:

nrniv config-exp5.txt exp5.txt ProbGABAAB_EMS_GEPH_g.mod True False False 3 -python fitting.py

2) on the trace number 3 of the dataset "exp5" using 20 different initial parameter values 
(uniformly randomized within a large, 5 orders of magnitude, range) and up to 3000 iteration steps for each run:

nrniv config-exp5.txt exp5.txt ProbGABAAB_EMS_GEPH_g.mod False True False 3 -python fitting.py

3) on the trace number 3 of the dataset "exp5" using 5 different initial parameter values 
(uniformly randomized within a large, 5 orders of magnitude, range) and up to 3000 iteration steps for each run:

nrniv config-exp5.txt exp5.txt ProbGABAAB_EMS_GEPH_g.mod False False True 3 -python fitting.py

At the end of the simulation a file called test.csv is created. The file contains the ensemble of parameters fitting each experimental trace with a root mean squared error (RMSE)
 <=10% of the maximum current.

All the simulations can be run locally or interactively leveraging HPC resources on the Human Brain Project collab https://collab.humanbrainproject.eu/#/collab/83942/nav/571536

Access to this resource requires free user registration with an institutional email at the following link:
https://iam.ebrains.eu/auth/realms/hbp/login-actions/registration?client_id=xwiki&tab_id=ET6tN9uN5s4
 
All the experimental data and other resources can be found in a Live Paper at the following link: https://humanbrainproject.github.io/hbp-bsp-live-papers/2020/lupascu_et_al_2020/lupascu_et_al_2020.html

Questions on the NEURON simulation should be addressed to
(replace -at- with the usual @ symbol):
carmen.lupascu-at-pa.ibf.cnr.it
michele.migliore-at-cnr.it