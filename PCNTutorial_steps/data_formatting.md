# Formatting Data to Run the PCN-toolkit Functions

This is an overview on the way data should be formatted in order to be used by the PCN-toolkit normative modelling functions such as evaluate. Usually, it is important to follow how the dataset in first organized in dataframes to be able to pass it through this function. **Covariates** such as sex, age and site of the data need to be concatenated with **brain measures or features** of interest (e.g. cortical thickness maps of different brain regions). Hence, it is essential to preprocess your data to have those brain measures which can take quite some time in itself.

A dataframe combining these two elements in bold is presented below, where the 2nd to 4th columns are covariates and others are example brain features (all values are only example values with no scientific usefulness):

| participant_id| age | sex     |site     |lh_fusiform thickness     |rh_fusiform thickness     |lh_frontalpole thickness  |...|
| :---  |    :----:   |          :----: |          :----: |:----: |:----: |   :----: | ---: |
| sub-001      | 27       | 1   |hcp     |2.9     |2.6     |2.5     |...     |
| sub-002   | 42        | 2      |ixi     |2.8     |2.8     |3.2     |...     |
| ...   | ...        | ...      |...     |...    |...   |...   |...   |

However, to pass these informations through the model, covariate and brain measure informations need to be separated in two different text files. However, before separating them, it is essential to remove subjects with too many Nan values. After, these separate dataframes are splitted up into train and test folds (e.g. 80-20 training-test split). 

Finally, when passing these new dataframes to the evaluate function, it is necessary to loop through the chosen regions of interest (ROIs). As expected, having more ROIs will take longer to run. Obtained output evaluation metrics from the model will be saved in a pre-formatted dataframe of metrics of interest. These metrics can be the:
- Explained variance (EV)
- Mean standardize log-loss (MSLL)
- Standardized Mean Squared Error (SMSE)
- Pearson orrelation between true/predicted responses (Rho)
- Z-score or deviation score (Z)
- And [others](https://pcntoolkit.readthedocs.io/en/latest/pages/glossary.html?highlight=smse#key-abbreviations)...

Now, you are ready to analyze and format your data accordingly! Happy formatting!

