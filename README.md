Welcome to the ``Learning differential equation models from stochastic agent-based model simulations'' team (also known as the **BEST** team)!

In this reposity, I have provided too much code from a recent article that I and others wrote. First thing I would recommend is starting to read through [this article](https://github.com/johnnardini/DDMSM-2021/blob/master/helpful_papers/ABM_EQL_review.pdf). Next, I recommend half of the group split into 1. ABM simulation team and the other half split into 2. EQL Simulation team. 

The ABM simulation team is directed to the **ABM** folder, especially the `plot_ABM_DE_SIR.ipynb` notebook, which can be used to simulate the SIR ABM and compare its output to its mean-field model. This notebook relies on `ABM_package.py` to implement the ABMs, and the Gillespie Algorithm is used for model implementation.

The EQL simulation team is directed to the **EQL** folder, especially the `Case study 5 SIR Varying params.ipynb` notebook, which performs some equation learning on the SIR ABM output data over several model parameters. This notebook relies on `PDE_FIND3.py`, which conducts the EQL methods, and `PDEFind_class_online.py`, which processes the data and calls the EQL methods.

# Learning DE models for stochastic ABMs
 Code for "Learning differential equation models from stochastic agent-based model simulations," by John Nardini, Ruth Baker, Mat Simpson, and Kevin Flores. Article available at https://arxiv.org/abs/2011.08255 .
 
 All code is implemented using Python (version 3.7.3). The folders listed in this repository implement code to run agent-based models (ABMs), perform equation learning (EQL), or store previously-computed data from ABM simulations.
 
 The **ABM** folder contains the code used to implement the ABMs from our study, which include the birth-death-migration (BDM) process and the susceptible-infected-recovered (SIR) model.  The jupyter notebook `plot_ABM_DE_BDM.ipynb` can be used to simulate the BDM ABM and compare its output to its mean-field model. The jupyter notebook `plot_ABM_DE_SIR.ipynb` can be used to simulate the SIR ABM and compare its output to its mean-field model. Both of these notebooks rely on `ABM_package.py` to implement the ABMs.
 
The **EQL** folder contains code used to implement the EQL methods. We provide a basic introduction in  `EQL Tutorial.ipynb`, and then the five case studies from our manuscript are available in `Case Study 1 Varying parameters for BDM.ipynb`, `Case study 2 varying number of ABM Simulations.ipynb`, `Case Study 3a Varying data resolution.ipynb`, `Case study 3b predicting unobserved dynamics.ipynb`, `Case study 4 model selection with EQL.ipynb`, and `Case study 5 SIR Varying params.ipynb`. Each of these files rely on the files `PDE_FIND3.py`, which conducts the EQL methods and `PDEFind_class_online.py`, which processes the data and calls the EQL methods.
 
 The **data** folder contains pre-simulated and saved ABM output data. For the BDM process, the files are named as: "logistic_ABM_sim_rp_" + str(rp) + "\_rd\_" + str(rd) + "\_real" + str(N) + ".npy", where rp = {0.001,0.01, 0.05, 0.1, 0.5, 1} is the agent proliferation rate, rd = {rp, rp/2, rp/4} is the agent death rate, and N = { 1,10,15,25, 50 } is the number of ABM simulations over which we computed the averaged ABM data. For the SIR model, the files are named as: "SIR_ABM_ri_" + str(ri) + "\_ri\_" + str(rr) + "\_real" + str(N) + ".npy", where ri = {0.001, 0.005, 0.01, 0.05, 0.1, 0.25 } is the agent infection rate, rr = {ri, ri/4, ri/2 ri/10} is the agent recovery rate, and N = { 3,5,10,15,25, 50} is the number of ABM simulations over which we computed the averaged ABM data.
 
 Please contact John Nardini at jtnardin@ncsu.edu if you have any questions, thank you.
