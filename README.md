# Project 4 Group 5

# Classifying credit card applications

<img width="400" alt="Screenshot 2024-04-03 at 7 33 PM" src="https://cdn.britannica.com/02/160902-050-B58BAD84/Credit-cards.jpg">


### Contents
- [Project Overview](#Project-Overview)
- [Repository Structure](#Repository-Structure)
- [Data Files](#Data-Files)  
- [Jupyter Notebooks](#Jupyter-Notebooks)]
- [How to Run the Code](#How-to-Run-the-Code)
- [References](#References)
- [Contributors](Contributors)

## Project Overview

This project uses historical credit card data to predict the future behaviour of customers who are applying for credit cards. The behaviours prodicted are:  

- Balance paid off each month
- Balance owing or overdue each month
- No credit card loan taken out each month

To do the prediction we explored different ways of modelling the data. Namely;

- Recurrent neural networks
- Logistic regression
- Random forest

The main motivation for this project was to explore the best method for financial predictions in order to help make the best informed decisions on applications.

## Repository Structure  
The root directory contains the following folders:  
- [Data_Cleaned](Data_Cleaned) - Contains the cleaned and scrubbed data files
- [Data_Original](Data_Original) - Contains the original data files obtained from Kaggle
- [Jupyter_notebooks](Jupyter_notebooks) - Contains the Jupyter notebooks used to clean the data and also contains a further three folders:
    - [Neural Networks](Jupyter_notebooks/Neural%20Networks/) - Contains the Jupyter files for the Neural Network models
    - [Random Forest](Jupyter_notebooks/Random%20Forest) - Contains the Jupyter files for the Random Forest model
    - [Logistics Regression](Jupyter_notebooks/logistics%20regression) - Contains the Jupyter files for the Logistic Regression model 


## Data Files
- [data_clean.csv](Data_Cleaned/data_clean.csv) - The initial data cleaned by the first pass through the original data 
- [dummied_data.csv](Data_Cleaned/dummied_data.csv) - The same data as data_clean.csv but with all the string variables dummied for the predictive models
- [dummied_data_add_clean.csv](Data_Cleaned/dummied_data_add_clean.csv) - The data cleaned by an additional pass through the original data after the initial predictive modelling

- [application_record.csv](Data_originial/application_record.csv) - This is one of the two original files obtained from Kaggle. It contains personal information about each customer such as gender, income, employments status etc.
- [credit_record.csv](Data_originial/credit_record.csv) - This is one of the two original files obtained from Kaggle. It contains the status of the credit card loan over a period of months

- [NN_baseline_2_layers_50_neurons.keras](Jupyter_notebooks/Neural%20Networks/NN_baseline_2_layers_50_neurons.keras) - The saved model for the baseline Neural Network model
- [NN_baseline_2_layers_50_neurons.keras](Jupyter_notebooks/Neural%20Networks/NN_opt_fully_3_layers_100_tanh_neurons.keras) - The saved model for the optimised Neural Network model 


## Jupyter Notebooks
- [Data_Cleaning.ipynb](Data_Cleaning.ipynb) - The Python code used for the initial data clean to create the data file [data_clean.csv](Data_Cleaned/data_clean.csv)
- [Data_reduced_and_dummied.ipynb](Data_reduced_and_dummied.ipynb) - The Python code used to create dummied data from [data_clean.csv](Data_Cleaned/data_clean.csv) for use by the models  
- [Data_reduced_and_dummied_additional.ipynb](Data_reduced_and_dummied_additional.ipynb) - The Python code for the second pass through the cleaning process to produce the additional data file [dummied_data_add_clean.csv](Data_Cleaned/dummied_data_add_clean.csv) 

- [NN_functions.ipynb](Jupyter_notebooks/Neural Networks/NN_functions.ipynb) - This file contains functions used to:    
    1) encode, split and scale data  
    2) define, compile and fit a neural network model    
    3) predict the outputs using test inputs    
- [NN_baseline.ipynb](Jupyter_notebooks/Neural%20Networks/NN_baseline.ipynb) - Code for a baseline Neural Network model
- [NN_Optimise_by_Red_Dim.ipynb](Jupyter_notebooks/Neural%20Networks/NN_Optimise_by_Red_Dim.ipynb) - Neural Network models in which data dimensions are reduced by dropping columns
- [NN_Optimise_by_Red_Dim_PCA.ipynb](Jupyter_notebooks/Neural%20Networks/NN_Optimise_by_Red_Dim_PCA.ipynb) - Neural Network models in which data dimensions are reduced by using Pricipal Components Analysis (PCA)
- [NN_Optimise_by_Oversampling.ipynb](NN_Optimise_by_Oversampling) - Neural Network model in which the data is oversampled to balance the distribution of output classes
- [NN_Optimise_by Structure_of NN.ipynb](NN_Optimise_by%20Structure_of%20NN.ipynb) - Several Neural Network models which explore the effect of increasing the number of neurons and layers on the target accuracy
- [NN_Optimise_by_Changing_Act_Function.ipynb](NN_Optimise_by_Changing_Act_Function.ipynb) - Neural Network model which investigate the effect of changing the activation functions
- [NN_fully_optimised.ipynb](NN_fully_optimised.ipynb) - Neural Network model which is fully optimised
- [NN_model_test_outputs.ipynb](NN_model_test_outputs.ipynb) - Predict the outputs using test inputs

- [logistic_regression_baseline.ipynb](Jupyter_notebooks/logistics%20regression/logistic_regression_baseline.ipynb) - Code for the baseline logistic regression model
- [logistic_regression_optimised.ipynb](Jupyter_notebooks/logistics%20regression/logistic_regression_optimised.ipynb) - Code for the optimised logistic regression model

- [Random_Forest.ipynb](Jupyter_notebooks/Random Forest/Random_Forest.ipynb) - Code for the Random Forest models


## How to Run the Code

To get started with this project, ensure that you have Python 3.2 installed on your system and clone the repository and install the Python packages listed below:  
- pandas
- numpy

To clone:  
    git clone https://github.com/DanielHughes1580/Project_4_Group_5.git

Create a new Conda environment for the project dependencies. Run the following command:  
- conda create --name dev python=3.2

Activate the newly created Conda environment by running:
- conda activate dev

Install the project dependencies using pip

To run the Logistic Regression and Random Forest Models use Jupyter notebooks.   
On the command line run the following command:  
- Jupyter notebook

For the Neural Network models, a google drive account is needed and Google Colab activated. The folders listed below need to   
be created and all the files in the [Neural Networks](Jupyter_notebooks/Neural Networks/)   
directory need to be copied to those folders:    
- /content/drive/My Drive/Colab Notebooks/Project_4/    
Run the neural network files. The will:  
    1) import dependencies  
    2) mount the google drive  
    3) access the notebook [NN_functions.ipynb](Jupyter_notebooks/Neural-Networks/NN_functions.ipynb) with the defined functions  
    4) import the data files from the github repository  
    5) run the function to encode, split and scale the data  
    6) run the function to define, compile and fit the neural network models  
    7) produce a model accuracy using test data  


## References
Data source:
https://www.kaggle.com/datasets/rikdifos/credit-card-approval-prediction?select=credit_record.csv

## Collaborators
- [Daniel Hughes](DanielHughes1580)
- [Mohammed Nawaz](https://github.com/MoNawaz101)
- [Ayomide Olanrewaju](Edimayo5)
- [Nana Afranie Ampadu Mensah](Mendev95)














