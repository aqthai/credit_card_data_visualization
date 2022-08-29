# cc_capstone
Data engineering project that extracts data from a json api and files to visualize correlations.
![Dataflow](dataflow.PNG)
Loan application and credit card datasets undergo ETL using Python, MariaDB, Apache Spark, and Python Visualization libraries.
To run the virtual environment, open the terminal, go to this directory and activate the virtual environment with
`Scripts\activate`
Download dependencies with 
`pip install -r requirements.txt`
Run jupyter-lab with
`jupyter-lab`
When finished, close the virtual environment with
`deactivate` or `Scripts\deactivate`

This dataset has about a thousand randomly generated SSNs, so this rules out using a bar graph.  The lines representing each SSN were so small.  Instead, I've used scatter plots.  Hovering over a point will provide information.  Also, I made a barplot for each demographic upon application approval, because each had unique dependent variables.  If these had unanimous x-values, then a multi-bar plot would have been easy to make.  For example, options for dependents vary from 0, 1, 2, or 3+ in text format, but options for Married were Yes or No.  On the feature branch, I investigate the pd.get_dummies(<dataframe>) method for logistic regression and use plotly to show data when hovering the chart.  Another problem is that the dashboard does not show figures unless they are made with plotly.  I had trouble showing seaborn and matplotlib graphs.