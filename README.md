# Ex-08-Data-Visualization-

## AIM
To Perform Data Visualization on the given dataset and save the data to a file. 

# Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature generation and selection techniques to all the features of the data set
### STEP 4
Apply data visualization techniques to identify the patterns of the data.


# CODE
import pandas as pd

import seaborn as sns

df=pd.read_csv("/content/SuperStore (1).csv")

df.info()

df.isnull().sum()

import matplotlib.pyplot as plt

import numpy as np

sns.distplot(df['Sales'])

plt.axvline(x=np.mean(df['Sales']), c='red', ls='--', label='mean')

plt.axvline(x=np.percentile(df['Sales'],25),c='green', ls='--', label = '25th percentile:Q1')

plt.axvline(x=np.percentile(df['Sales'],75),c='orange', ls='--',label = '75th percentile:Q3' )

plt.legend()

sns.boxplot(x=df['Segment'], y=df['Sales'])

# OUPUT

![image](https://github.com/ATHDY005/Ex-08-Data-Visualization-/assets/84709944/0ff09632-7dbb-4680-a1e0-8281c3af2ff6)
![image](https://github.com/ATHDY005/Ex-08-Data-Visualization-/assets/84709944/2c3bb0c2-3606-4f3d-8c9c-d3b4ad1498c5)
![image](https://github.com/ATHDY005/Ex-08-Data-Visualization-/assets/84709944/7a110481-925a-4878-9682-314739acaff1)
![image](https://github.com/ATHDY005/Ex-08-Data-Visualization-/assets/84709944/75b669c7-cbf2-4933-8ab9-8c68c88ca8a8)
![image](https://github.com/ATHDY005/Ex-08-Data-Visualization-/assets/84709944/8245beef-1743-491d-b29d-f4af5ed420cf)

# RESULT

Hence Data Visualization on the given dataset is performed and the data was saved to a file successfully.
