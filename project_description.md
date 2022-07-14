# Project Title: Exploratory Work on the Predictive Clinical Neuroscience (PCN) Toolkit


## Background
The PCN toolkit aims at providing diffferent tools of normative modelling for understanding psychiatric disorders at the individual level including data selection, data preparation, algorithm & modelling and evaluation & interpretation (Rutherford et al., 2022). The figure 1 below illustrates concepts involved in normative modelling: 
* The sub-figure **a** represents how classical normative models are utilized using pediatric growth charts as examples. 
* Sub-figure **b** highlights assumptions made during studies where different groups being studied are usually considered as homogeneous, when in fact there within-group heterogeneity.  
* Sub-figure **c** shows how normative modelling can be used to predict brain variables (in this case, mean cortical thickness) against age. This modelling is only possible by combining an enormous quantity of multi-site data from a certain interest population.
* Finally, sub-figure **d** illustrates the regression model used to obtain results shown in c.

<a href="https://pcntoolkit.readthedocs.io/en/latest/pages/pcntoolkit_background.html">
   <img src="https://pcntoolkit.readthedocs.io/en/latest/_images/blr_fig1.png" width:500px;" alt=""/>
   <br /><sub><b>Figure 1. Concepts involved in normative modelling... an image is worth 1000 words</b></sub>
</a>

## Objectives
The aim of this project will be decomposed into three sub-objectives:
* Start off with the available tutorial on the PCN toolkit documentation to get familiar to it
* Use another set of data to follow through the available steps that this toolkit offers (to name them here...)
* Adapt some functionnalities which were found to be less intuitive to work with
All of these three sub-objectives will be documented throughout the weeks to be able to be reproduced in later or other exploratory works. 

## Data at Hand
First, the available data in the tutorials will be used. Then, the Calgary Preschool Dataset (Reynolds et al., 2020) will be analyzed using the PCN toolkit. This interesting and publicly available pediatric dataset is interesting in that it offers longitudinal data. Indeed, it contains T1-weighted images of around 64 subjects aged 2-8 years old.

## Tools Used:
- [PCN Toolkit](https://pcntoolkit.readthedocs.io/en/latest/) and their [GitHub page](https://github.com/amarquand/PCNtoolkit)
- Python Scripting
- Machine Learning
- Bash Terminal

## References
- Reynolds, J. E., Long, X., Paniukov, D., Bagshawe, M., & Lebel, C. (2020). Calgary Preschool magnetic resonance imaging (MRI) dataset. Data Brief, 29, 105224. 
- Rutherford, S., Kia, S. M., Wolfers, T., Fraza, C., Zabihi, M., Dinga, R., Berthet, P., Worker, A., Verdi, S., Ruhe, H. G., Beckmann, C. F., & Marquand, A. F. (2022). The normative modeling framework for computational psychiatry. Nature Protocols. https://doi.org/10.1038/s41596-022-00696-5
