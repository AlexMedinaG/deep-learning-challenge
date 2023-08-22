For this part of the assignment, you’ll write a report on the performance of the deep learning model you created for Alphabet Soup.

The report should contain the following:

Overview of the analysis: Explain the purpose of this analysis.

The purpose of this analysis was to make a machine learning model to predict successful financing of organizations, based on multiple features. 

Results: Using bulleted lists and images to support your answers, address the following questions:

Data Preprocessing

What variable(s) are the target(s) for your model?
-if the organization had a successful outcome or not. 

What variable(s) are the features for your model?
-a features list can be found on the Optimizatoin notebook, listed from highest relative importance to lowest (based on a Random Forest analysis). 
        ['APPLICATION_TYPE_Other', 'APPLICATION_TYPE_T10',
       'APPLICATION_TYPE_T19', 'APPLICATION_TYPE_T3', 'APPLICATION_TYPE_T4',
       'APPLICATION_TYPE_T5', 'APPLICATION_TYPE_T6', 'APPLICATION_TYPE_T7',
       'APPLICATION_TYPE_T8', 'AFFILIATION_CompanySponsored',
       'AFFILIATION_Independent', 'CLASSIFICATION_C1000',
       'CLASSIFICATION_C1200', 'CLASSIFICATION_C2000', 'CLASSIFICATION_C2100',
       'CLASSIFICATION_C3000', 'CLASSIFICATION_Other',
       'USE_CASE_CommunityServ', 'USE_CASE_Heathcare', 'USE_CASE_Preservation',
       'USE_CASE_ProductDev', 'ORGANIZATION_Association',
       'ORGANIZATION_Co-operative', 'ORGANIZATION_Corporation',
       'ORGANIZATION_Trust', 'INCOME_AMT_0', 'INCOME_AMT_1-9999',
       'INCOME_AMT_10000-24999', 'INCOME_AMT_100000-499999',
       'INCOME_AMT_10M-50M', 'INCOME_AMT_1M-5M', 'INCOME_AMT_25000-99999',
       'INCOME_AMT_50M+', 'INCOME_AMT_5M-10M', 'ASK_AMT_Binned_Very Low',
       'ASK_AMT_Binned_Low', 'ASK_AMT_Binned_Moderate', 'ASK_AMT_Binned_High',
       'ASK_AMT_Binned_Very High']

What variable(s) should be removed from the input data because they are neither targets nor features?
-These features did not provide any importance to the result.
['AFFILIATION_Family/Parent', 'AFFILIATION_National', 'SPECIAL_CONSIDERATIONS_N', 'SPECIAL_CONSIDERATIONS_Y', 'AFFILIATION_Regional']

Compiling, Training, and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why?
-used 39 neurons for the first layer, used 4 hidden layers with 100 neurons each and finally used 1 neuron (sigmoid) for bool output. 
 
Were you able to achieve the target model performance?
-no

What steps did you take in your attempts to increase model performance?
-tried to rank and remove features by their relative importance, made bins for ASK_AMT in order to take away the importance that was being given based on the values vs the other columns that had just ones and zeros, and finally tried different combinations of neurons and layers to try to get to the desired 75% accuracy. 


Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.
-I was not able to train the model to get to the desired accuracy, I would recommend trying additional models and comparing them to see if it can be improved. Also, a PCA analysis before the NN model could help reduce the number of features and possible reduce the complexity of the fine-tuning of the model. 