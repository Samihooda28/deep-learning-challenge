# deep-learning-challenge

Overview of the analysis:
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. We use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup by using Machine Learning and Neural Networks to create a Deep Learning algorithm.

Results
Data Preprocessing
Our target variable for this Deep Learning algorithm is called IS_SUCCESSFUL. This is a measure of whether the funding money was used successfully.

The input variables used are:

APPLICATION_TYPE: Alphabet Soup application type
AFFILIATION: Affiliated sector of industry
CLASSIFICATION: Government organization classification
USE_CASE: Use case for funding
ORGANIZATION: Organisation type
STATUS: Active status
INCOME_AMT: Income classification
SPECIAL_CONSIDERATIONS: Special considerations for application
Although the specific company applying will likely impact whether a grant is successful, we did not include NAME (Name of the company applying for the funding) as this would likely result in overfitting of the model and could leave Alphabet Soup open to accusations of bias. We also did not include EIN as its function is indexing.

overfitting

Compiling, Training, and Evaluating the Model
Initially, we used 2 hidden layers and an output layer, with 8 neurons each using a Rectified Linear Unit (ReLu) activation function. We chose this as a sort of standard setup, with ReLu being a very popular activation function, and not wanting to overload the model with nuance but still wanting some depth of field. We attempted optimization by trialing different activation functions, different numbers of neurons, and different numbers of layers, as well as reducing the input size. None of these methods were effective in raising the accuracy of the model to the target value of 75%.

activation_percentages model optimization

Summary
Overall, this attempt to create a Deep Learning model to predict whether a funding application would be successful did not succeed. This was likely due to the fact that this model was very difficult to optimize, likely due to the noisiness of the data. It is very difficult to identify outliers within this dataset, and the data does not lend itself to visualization to give any insight into how to structure the model. I would recommend looking for further input data and spending some time running various visualization and statistics for the dataset, to look for further insights on a good place to start the model. It could also be useful to split the data into smaller sets by Application Type or Classification and run models within those sets.

It could instead be beneficial to conduct supervised cluster analysis on the data using a simpler Machine Learning algorithm, such as a logistic regression, as the majority of this data is discrete, not continuous. This model would cluster the data into successful and not successful applications, and could predict which cluster any new application falls into.
