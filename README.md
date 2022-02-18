# CA03
Computer Assignment 3
This assignment deals with creating and testing DecisionTreeClassifiers

We begin by uploading data from this url "https://github.com/ArinB/MSBA-CA-Data/blob/main/CA03/census_data.csv?raw=true”
We then go on to examine and run some initial exploritory analysis using stacked bar charts

Next we go through a process of transforming our independent variable data using OneHotEncoder in order to get numerical representations of
the categorical data present in our census dataset.

We then initiate and fit our first DecisionTree using the training data provided and then visualize that tree using graphviz library.

Next we run initial performance summary scores for our model.

Then we manually alter the hyper parameters that go into the decisiontree initiation function. Here we have tested 4 different trees that use "entropy"
criteria and 4 different trees that use "gini" criteria

Next we create a function to automate the testing of these different hyperparameters in our Decision trees. This function takes in 4 different lists of
the different hyperparameters we want to change when evaluating the resulting trees. The hyperparameters along with their respective tree's performance 
statistics are recorded in a dataframe which is returned from the function. We can then save that dataframe as a CSV

Lastly we want to predict our dependent variable outcome (Less thank 50K income or Greater than 50K income) based on an information set for a new individual as described below:

• Hours Worked per Week = 48 
• Occupation Category = Mid - Low 
• Marriage Status & Relationships = High 
• Capital Gain = Yes 
• Race-Sex Group = Mid 
• Number of Years of Education = 12 
• Education Category = High 
• Work Class = Income 
• Age = 58

This categorical data is then saved in a dataframe and encoded using our OneHotEncoder from before. That encoded data is then ran through our Best performing DecisionTree. We make a judgement on that individual's income based on the resulting predicted probability. In this case we ultimately predicted that the individual's income is >50K.
