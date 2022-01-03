# Neural_Network_Charity_Analysis

## Project Overview
I am working with Beks at Alphabet Soup, a non-profit that focusses on providing funding for verious organizations. We are working to develop a model that will help predict whether applicants will be successful if they are funded by Alphabet Soup.  We will be using past data to build a Neural Network model to help with future predictions.  

## Resources
- Data Source: charity_data.csv
- Sofware: Jupyter Notebook 6.3.0
- Library: Pandas
- Library: tensorflow
- Library: sklearn
- Language: Python 3.6.7
- Conda Env: mlenv

## Results - DATA PREPROCESSION - ORIGINAL MODEL (DELIVERABLE 1 & 2)
### The variables that are considered targets for the model are:
- Is_Successful

### The variables that are considered features for the model are:
- Application_Type
- Affiliation
- Classification
- Use_Case
- Organization
- Status
- Income_Amt
- Special_Consideration
- Ask_Amt

### The variables that are neither features or targets for the model are:
- EIN
- Name

### Original Model Performance:
![Model Performance](https://github.com/tessiertodd/Neural_Network_Charity_Analysis/blob/main/Pics/Save%20Callback%20every%205%20epochs.png)

### Callback to Save Model's Weight Every 5 Epochs:
![5 epoch saving](https://github.com/tessiertodd/Neural_Network_Charity_Analysis/blob/main/Pics/Save%20Callback%20every%205%20epochs.png)


## Results - COMPILING, TRAINING AND EVALUATING THE MODEL - OPTIMIZATION (DELIVERABLE 3)
- Original Model had 2 hidden layers and 1 outer layer, but with optimization work I have added an additional hidden layer. Original Model had 80 neurons in first hidden layer and 30 neurons in second hidden layer... I increased them a bit when looking to increase model performance... it did not in any significant way.  The activation functions I used in the hidden layers were relu, and sigmoid on outer layer... chose those activation functions as they are the best given the type of data.
- I was not able to achieve the target model performance, despite making many changes - tried multiple changes on 3 different models results below.
- I removed columns, added a layer and even tried removing classification or application_type, both of which decreased the performance. Increasing the epochs did seem to improve the performance a little, though not enough to hit the 75% objective. I also increased the number of neurons and increased the number of layers.
- Even with all the changes that I tried, I was not able to get the model to achieve a 75% performance.

### Optimization 1
![Optimization 1](https://github.com/tessiertodd/Neural_Network_Charity_Analysis/blob/main/Pics/Model%20Performance%20Opt%201.png)

### Optimization 2
![Optimization 2](https://github.com/tessiertodd/Neural_Network_Charity_Analysis/blob/main/Pics/Model%20Performance%20Opt%202.png)

### Optimization 3
![Optimization 3](https://github.com/tessiertodd/Neural_Network_Charity_Analysis/blob/main/Pics/Model%20Performance%20Opt%203.png)


### Summary
Unfortunately we were not able to adjust model to reach 75% accuracy, but was very interesting to see how changing different things would adjust the outcome, even if just slightly.  When I excluded some variables from being features, I saw that accuracy dropped to between 65-70%, much less that the just over 72% we started with on first iteration of our model.

We could try to use a linear regression model or another machine learning model to see if we could improve the predictability... this may help given the type of data we are analyzing.
