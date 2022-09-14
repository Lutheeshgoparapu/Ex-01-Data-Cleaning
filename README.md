# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE
```
Program developed by: GOPARAPU LUTHEESH
Register number: 212221230029

import pandas as pd
import numpy as np
import seaborn as sns

df1 = pd.read_csv("Data_set.csv")
df1

df1.head()

df1.describe()

df1.info()

df1.tail()

df1.shape

df1.columns

df1.isnull().sum()

df1.duplicated()

#Using mode method to fill the data in columns as Object(String)
#mode()[0] - Takes the most reccuring value and fills the empty cells
df1['show_name'] = df1['show_name'].fillna(df1['show_name'].mode()[0])
df1['aired_on'] = df1['aired_on'].fillna(df1['aired_on'].mode()[0])
df1['original_network'] = df1['original_network'].fillna(df1['original_network'].mode()[0])

sns.boxplot(x="rating",data=df1)

#Using mean method to fill the data
df1['rating'] = df1['rating'].fillna(df1['rating'].mean())
df1['current_overall_rank'] = df1['current_overall_rank'].fillna(df1['current_overall_rank'].mean())
df1['watchers'] = df1['watchers'].fillna(df1['watchers'].mean())

#Checking the total no.of null values again
df1.isnull().sum()

#Checking info of the dataset to check all the columns have entries
df1.info()
```
# OUPUT:
![IMG-001](https://user-images.githubusercontent.com/94154531/190100942-9e98c34d-4be8-4013-bdde-271b315b8cda.png)
# HEAD:
[IMG-002](https://user-images.githubusercontent.com/94154531/190101103-c8431ada-0960-40e0-8b88-2086643d40f4.png)
# DESCRIBE:
![IMG-003](https://user-images.githubusercontent.com/94154531/190101358-eb624af4-9cb2-4963-8d8e-717bbfefe11b.png)
# INFO:
![IMG-004](https://user-images.githubusercontent.com/94154531/190101475-4ed1cbfa-4651-4b95-b693-edf75e32169a.png)
# TAIL:
![IMG-005](https://user-images.githubusercontent.com/94154531/190101926-f532cb1f-9bfb-473e-8cae-2280ceba05ff.png)
# SHAPE:
![IMG-006](https://user-images.githubusercontent.com/94154531/190101991-ff8fa468-2667-41e9-8192-3fac9479bcef.png)
# isnull().sum() - Pre Cleaning:
![IMG-007](https://user-images.githubusercontent.com/94154531/190102316-965c5cc0-6bfa-4a8a-afaa-8fea51f69861.png)
# DUPLICATES
![IMG-008](https://user-images.githubusercontent.com/94154531/190102376-e41b623b-9839-4093-b4e2-ee3b7bc43ad6.png)
# SNS PLOT - RATING:
![IMG-009](https://user-images.githubusercontent.com/94154531/190102560-a96ebb7e-8c00-4ad7-b033-14570dfb329c.png)
# isnull().sum() - Post Cleaning:
![IMG-10](https://user-images.githubusercontent.com/94154531/190102829-e46f213a-2ec3-4882-a395-e569c2ce1227.png)
# Info - Post Cleaning:
![IMG-11](https://user-images.githubusercontent.com/94154531/190102982-e29e1fca-34ea-44cf-b494-a1139ea8352c.png)
# RESULT:
The given data is read and data cleaning is performed and the cleaned data is saved to a file.
