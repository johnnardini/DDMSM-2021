# Learning DE models for stochastic ABMs
 Code for "Learning differential equation models from stochastic agent-based model simulations," by John Nardini, Ruth Baker, Mat Simpson, and Kevin Flores. Article available at https://arxiv.org/abs/2011.08255 .
 
 All code is implemented using Python (version 3.7.3). The folders listed in this repository implement code to run agent-based models (ABMs), perform equation learning (EQL), or store previously-computed data from ABM simulations.
 
 The **ABM** folder contains the code used to implement the ABMs from our study, which include the birth-death-migration (BDM) process and the susceptible-infected-recovered (SIR) model.  The jupyter notebook `plot_ABM_DE_BDM.ipynb` can be used to simulate the BDM ABM and compare its output to its mean-field model. The jupyter notebook `plot_ABM_DE_SIR.ipynb` can be used to simulate the BDM ABM and compare its output to its mean-field model. Both of these notebooks rely on `ABM_package.py` to implement the ABMs.
 
The **EQL** folder contains code used to implement the EQL methods. We provide a basic introduction in  `EQL Tutorial.ipynb`, and then the five case studies from our manuscript are available in `Case Study 1 Varying parameters for BDM.ipynb`, `Case study 2 varying number of ABM Simulations.ipynb`, `Case Study 3a Varying data resolution.ipynb`, `Case study 3b predicting unobserved dynamics.ipynb`, `Case study 4 model selection with EQL.ipynb`, and 'Case study 5 SIR Varying params.ipynb'. Each of these files rely on the files `PDE_FIND3.py`, which conducts the EQL methods and `PDEFind_class_online.py`, which processes the data and calls the EQL methods.
 
 Please contact John Nardini at jtnardin@ncsu.edu if you have any questions, thank you.
