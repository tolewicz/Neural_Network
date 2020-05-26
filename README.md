# Neural_Network# Cryptocurrencies
Unsupervised machine learning

## Project Overview
Harnesting the neural network machine learning technology to improve data classification  

## Module challenge

### Objective
Perform data cleaning and processing using dataframes and use neural network technology to classify non-profit organizations.
Develop the model that predicts if non-profit organization is successful

### Results 
#### Data processing
*	Charity organization data was examined for repetition and prepared for processing
* After confirming that there is no repetition in organization name and EIN, the column EIN was dropped and name was set as dataframe index
*	The columns with object data was converted into numerical data
* The data with more than 10 unique values was backed into class "Other"
* The threshold of "Other" class was determined by analyzing density and data distribution using hvplot


<p align="center">
<img src="https://github.com/tolewicz/Neural_Network/blob/master/Fig/density.JPG" width="450" height= "200">
</p>

<p align="center">
<img src="https://github.com/tolewicz/Neural_Network/blob/master/Fig/bar.JPG" width="450" height= "200">
</p>

* Afterwards the data was normalized by using Standard Scaler
*	After pre processing the data, for additional visualization the data was converted into primary components PC1,PC2 and plotted to get an idea about potential class distribution. However 2D and 3D plots did not show any obvious clusters

<p align="center">
<img src="https://github.com/tolewicz/Neural_Network/blob/master/Fig/PC.JPG" width="450" height= "200">
</p>

#### Model

* I used 7 hidden layers with following neuron count: 2,4,8,16,32,64,128
* I tested various activation function including tanh, relu, linear, sigmoid
* I combined tanh and relu: hidden layers 1,2 (tanh) 3-7 relu, the reason was to include negative values in the 1st layer of processing and ractify them with the next layers based on results from tensorflow playground (fig). 
* The result was not better than for 3x layer model with 16,8,2 neuron layers i.e. the performance for both models was 73% (goal 75%)
* To tackle the issue using diffrent machine learnign model i would use Random Forest Classifier because the following:
1. It is the best, most accurate a classifier model
2. Takes multiple variables
3. Is the closest to neural network model but with much faster learning

 
## Resources

- Technologies used: Python, sklearn package, tensorflow package, hvplot package, tensorflow playground web site 
- Programs: AlphabetSoupChallenge.ipynb
- Resources: Resources/ charity_data.csv


