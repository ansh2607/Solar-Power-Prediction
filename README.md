# Solar-Power-Prediction
Solar energy plays an increasingly important part of the country’s growth and sustainability. The project will perform data mining and knowledge discovery of power quality events associated with the solar grids and estimate the solar PV output loss (in kWh)

### Cleaning of data
The data cleaning and transformation tasks were systematically performed through the Python programming language. The tasks were decomposed and grouped into logical modules through custom-built functions in Python.
The critical alarms data cleaning tasks involve the following:
• Input: Critical Alarm Dataset files in Excel (XLSX) format.
• Output(s): processed alarm Dataset.csv, pivoted alarm Dataset.csv
– Merging all the files containing yearly data into one dataframe
– Categorized the grid and non-grid events in a seperate column
– Determined the period in which the event took place
– Calculated the hours for which the event was active
– Pivoted the event data on the basis of the details of the event to get the Grid Duration Hours, Maintenance Duration hours and the hours for which DelREMO was not communicating, as seperate columns
– Finally, saved the datasets as CSV files
The weather data cleaning tasks involve the following:
• Input: Weather Dataset in CSV format. • Output(s): weather data.csv
– Dropping the unnecessary columns
The plant output data cleaning tasks involve the following:
• Input: Plant Output Dataset files in Excel (XLSX) format. • Output(s): Combined Solar Dataset.csv
– Transforming the plant output data sets from Excel (XLSX) format to CSV
(commaseparated value) data sets respectively

### Final Dataset
• Input(s): Plant Output Data, Critical Alarm Data and Weather Dataset in CSV format.
• Output(s): final dataset.csv
– Merging all the input files to form a final dataset containing all the necessary
columns and excluding all erroneus data.
The data contains (7) independent variables and (1) dependent variable which are used for the analysis and model selection as follows,
– Total Yield [kWh] - Output generated from the plant (Dependent Column)
– GridDurationHours - represents the number of hours the grid events took place
– MaintDurationHours - represents the number of hours the Maintenance events took place
– DelREMO - represents the number of hours for which DelREMO site stopped communicating
– Temp - Temperature on a particular day
– Prcp - represents the amount of precipitation recorded per day
– Cloud Cover - represents the coverage of the clouds per day
– Conditions - Categorical variable captures the weather conditions, whether the weather was clear, rainy or partially cloudy
