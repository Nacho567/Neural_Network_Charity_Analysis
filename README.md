# Neural Network Charity Analysis

## **Overview**

In this analysis we tested data to create a neural network to see if applicants applying for Alphabet Soup funding will be successful. 

## **Results**

Data Preprocessing
- The target for this model was the 'IS_SUCCESSFUL' column, which helped train our model to see if a company used their funding successfully.
- The variables we used first for features are all of the columns pictured below, except: EIN, Name, and Is_successful.
- The EIN and Name variables were removed beacause it was decided that they provided no extra help to the learning model.

![application dataframe head]()

**Compiling, Training, and Evaluating the Model**
- The first model was given to us, and included: 44 input features, 80 neurons in the first layer, 30 neurons in the second layer, and 'relu' as the activation. Only two hidden layers were used.
- Target model performance was not met as the model could only achieve about 72%.
![First Model Accuracy]()

**Steps taken to try to improve the accuracy of the model:**
1. Everything was the same as the first run, but the first layer was changed to 60 neurons, the second was changed to 25 neurons, and the epochs were increased to 100. This resulted in practically the same accuracy of 72%.
2. An optimizer was then run to see what might create the best model on the current data. The best it returned was almost 73%.
3. After reassessing, the two columns that were originally dropped, EIN and Name, were kept. The Name column was looked at and all the single applications were put into one bin. The Application_Type and Class columns were binned as they were in the first model as well. This model was then run through an optimizer and the best it returned was 80%.
4. Using the optimization results found, a new model was initiated with: __input features, 73 neurons in the first layer, 49 neurons in the second layer, the epochs were increased to 200, and tanh as the activation. Again only two hidden layers were used. An accuracy of 78% was returned, improving on the original model by 6%.

Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.
