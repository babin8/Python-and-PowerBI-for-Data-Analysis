# Sales-Prediction-Model

This is my first official prompt engineering project. The goal is to create a prediction model that can project the daily sales for a convenience store.

The data used for this model are:
    - Daily Sales data: containing the sales metrics to analyze their dependency with other factors.
    - Daily Sales data per department: containing sales and sales metrics per department to help predict sales data.
    - Weather Data for the zip code associated with the store.

Tools used:
          - Grok 3
          - Jupyter Lab
          - Python: pandas, numpy, scikitlearn


**Part 1: Data Initialization**

The conversation with Grok can be found at:
https://grok.com/share/c2hhcmQtMg%3D%3D_370fa49c-ea66-4605-8257-8cb0971cb44a

Data_initialization.ipynb

    Step 1: Importing the datafiles, give info, describe the data, and give headers.

    Step 2: Renaming the headers, deleting unwanted headers, adding more time identifiers,     standardizing the data to list the values according to date including department-wise daily sales data.

        Headers kept:
              - Time: Date, Day of the week, Day of the month, Month
              - Daily Sales: Total Sales, Average Sales, Total Items, Average Sales, Total Baskets
              - Department Sales: Same as daily sales for every department.
              - Weather Data: Minimum Temperature, Maximum Temperature, Average Temperature, Wether Conditions, Moonphase (To capture holidays), Sunset Time (To capture seasons)


    Step 3: Data Cleaning; Formatting the data into standard formats, filling empty values, and dummy-encoding the non-numeric data

    Step 4: Combining the data into a single large datafile.

Result: 1319 Rows x 141 Columns

  **Part 1.1: Initial Data Analysis**

  The conversation can be found at:
  https://grok.com/chat/5a21fe89-0d63-48ff-9b93-3e3b81e9b309

  Growth.ipynb

    Step 1: Visualize the total sales and sales by department per day in the dataset range.

    Step 2: Calculate Slope to visualize growth or reduction in sales for the metrics.

    Step 3: Save the visualizations showing daily sales with their slope into a new fodler named 'growth'

Result: Initial idea about the deparments that are performing well and the departments that need to be pushed.

**Part 2: Correlations**

Method used: Spearman's Correlation Coefficient

The conversation can be found at:
https://grok.com/chat/621124b3-d6e0-44b5-ad26-29d292106c18 

  **Part 2.1: Daily Sales**

  Correlations.ipynb

     Step 1: Calculate and visualize the correlations amongst the time identifiers, the weather identifiers, and then between daily sales metrics. Study the correlation matrix. Also add year as a time identifier.
  
     Step 2: Eliminate potential multicollinearity headers (headers with high correlation). Save the selected headers into a new file.

     Step 3: Create a basic linear regression model and a random forest regression model to predict the daily sales. Calculate the performance metrics and visualize the predicted sales vs actual sales.  

Result: 12 columns; 1 date, 9 features amd 2 prediction variables. Initial R2 scores close to zero.

**Part 3: Clustering**

Method used: K-means clustering, elbow method

The conversation can be found at:
https://grok.com/share/c2hhcmQtMg%3D%3D_0bbfaadb-cebe-475a-bb29-05366c548dff

    **Part 3.1: Daily Sales**

    Clustering.ipynb

      Step 1: Initial K-means clustering of the dataset.
        
      Step 2: Use Elbow method to calculate the optimal number of clusters and visualize the curve.

      Step 3: Create a new header to identify the cluster for each date.

      Step 4: Using the cluster as a feature with the existing feautes, predict the values for both the prediction variables using Linear Regression and Random Forest Regression. Calculate their prediction metrics.

Result: Linear Regression R2 score: 0.2377 and Random Forest R2 score: 0.3726 for predicting the total sales. Overall model improvement.
        
**Part 4: Normalization**

Method Used: Cyclical encoding, log(x+1) transformation, Robust encode, IQR to detect outliers.


