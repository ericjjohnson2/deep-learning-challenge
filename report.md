**1. Overview:** A nonprofit foundation seeks a model to evaluate applicant funding requests. This model uses a binary classifier to predict successful funding. Three models were made and this report is analyzing model number 4. 

**2. Results:** 
- **Data Preprocessing:**
    - **Target Variables of the Model:** The target variable is IS_SUCCESSFUL. This is how we'll test the model's predictive powers.  
    - **Feature Variables of the Model:** The feature variables are APPLICATION_TYPE, AFFILIATION	CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT. All of these variables seem to have an impact, even if small, on the model's performance.  
    - **Removed Variables:** The removed variables are EIN and NAME. These are unique categorical data that will not help the model make determinations.  
- **Compiling, Training, and Evaluating the Model:**
    - **Number of neurons, layers, and activation functions:** Model 4 contains three hidden layers, the first two using Relu and the last using Sigmoid activation functions. The first hidden layer has 4 neurons, the second has 3, and the final hidden layer has 2 neurons. 
    - **Model Performance Target:** Model 4 was closest to the target of 75% accuracy, acheiving about 73.12% accuracy.
    - **Enhancing the Model:** Model 4 uses both Relu and Sigmoid. It has about the same accuracy is Model 3 but with lower Loss. Model 4 improves upon Model 1 by using fewer neurons. In addition to the change in activation functions, I also experimented with dropping more columns, creating more bins, changing the number per bin, and changing the hidden layers and numbers of neurons. Model 5 explores using K-means clustering and PCA to reduce the fields but this did not yield better results. There are many combinations and further experimentation would likely yield a higher performing model. 
    - **Correction:** An error in the original code caused higher accuaracy results but this was due to including the customer names and IDs which should have no impact. Without these columns the model's accuracy is lower but training on those columns should not improve real world results on non-training data. 

**3. Summary:** The overall results are 73.11% accuracte, falling short of target. It's a good start but more can be done. A different approach to creating the bins might yeild better results. 



![Model 4 Performance: Loss: 0.5564002990722656, Accuracy: 0.731195330619812](img/model4.png)<br>
*Model 4 Performance*
