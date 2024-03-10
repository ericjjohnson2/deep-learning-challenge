**1. Overview:** A nonprofit foundation seeks a model to evaluate applicant funding requests. This model uses a binary classifier to predict successful funding. Three models were made and this report is analyzing model number 3. 

**2. Results:** 
- **Data Preprocessing:**
    - **Target Variables of the Model:** The target variable is IS_SUCCESSFUL. This is how we'll test the model's predictive powers.  
    - **Feature Variables of the Model:** The feature variables are APPLICATION_TYPE, AFFILIATION	CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT. All of these variables seem to have an impact, even if small, on the model's performance.  
    - **Removed Variables:** The removed variables are EIN and NAME. These are unique categorical data that will not help the model make determinations.  
- **Compiling, Training, and Evaluating the Model:**
    - **Number of neurons, layers, and activation functions:** Model 3 contains three hidden layers, all using the tanh activation function. The first hidden layer has 8 neurons, the second has 4, and the final hidden layer has 2 neurons. 
    - **Model Performance Target:** Model 3 surpassed the target of 75% accuracy, acheiving about 79% accuracy.
    - **Enhancing the Model:** Model 3 improved on the first model which used both Relu and Sigmoid. In addition to the change in activation functions, I also experimented with dropping more columns, creating more bins, changing the number per bin, and changing the hidden layers and numbers of neurons. There are many combinations and further experimentation would likely yield a higher performing model. 

**3. Summary:** The overall results are 79% accuracte. It's a good start but more can be done. A different approach to creating the bins might yeild better results. 



![Model 3 Performance](img/model3.png)<br>
*Model 3 Performance*
