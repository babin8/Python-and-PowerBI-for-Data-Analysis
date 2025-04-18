# Sales-Prediction-Model

This is my first official prompt engineering project. The goal is to create a prediction model that can project the daily sales for a convenience store.

The data used for this model are:
- Daily Sales data.
- Daily Sales data per department.
- Weather Data for the zip code associated with the store.

Tools used:
- Grok 3
- Jupyter Lab
- Python: pandas, numpy, scikitlearn


**Part 1: Data Initialization**

The conversation with Grok can be found at:
https://grok.com/share/c2hhcmQtMg%3D%3D_370fa49c-ea66-4605-8257-8cb0971cb44a

Data_initialization.ipynb

Step 1: Import the data, give info, describe the data, and give headers.

Step 2: Renaming the headers, deleting unwanted headers, adding more time identifiers, standardizing the data to list the values according to date including department-wise daily sales data.

Step 3: Data Cleaning; Formatting the data into standard formats, filling empty values, and encoding the non-numeric data

Step 4: Combining the data into a single large datafile.

Result: 141 Coulmns of identifiers with 1319 Rows of values.

**Part 1.5: Initial Data Analysis**

The conversation can be found at:
https://grok.com/chat/5a21fe89-0d63-48ff-9b93-3e3b81e9b309

Growth.ipynb

Step 1: Visualize the total sales and sales by department per day in the dataset range.

Step 2: Calculate Slope to visualize growth or reduction in sales for the metrics.

Step 3: Save the visualizations showing daily slope with slope into a new fodler named 'growth'

Result: The owners can get an initial idea about which deparments are performing well and which departments need to be pushed more.

**Part 2: Correlations**
