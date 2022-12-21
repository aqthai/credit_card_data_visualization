# Credit Card Visualization
Here's how I would extract, transform, and load data from a json api and multiple files to visualize correlations.
![Dataflow](dataflow.PNG)
A thousand rows of loan application and credit card data were processed using Python, MariaDB, Apache Spark, and Python Visualization libraries.
To run the virtual environment, open the terminal, go to this directory and activate the virtual environment with
`Scripts\activate`
Download dependencies with 
`pip install -r requirements.txt`
Run jupyter-lab with
`jupyter-lab`
When finished, close the virtual environment with
`deactivate` or `Scripts\deactivate`

This dataset has about a thousand randomly generated SSNs, so I've used scatter plots to visualize spendings.  Hovering over a point will provide more information on each transaction.  To see how demographics correlate with credit card approval, a countplot was used for each demographic.  I used the pd.get_dummies(<dataframe>) method to change Yes and No values into 0 and 1's to try machine learning models and logistic regression worked best.  The dashboard was made with dashboard core components (dcc).  This does not show figures unless they are made with plotly, so seaborn and matplotlib graphs appear only on the index.ipynb file.
