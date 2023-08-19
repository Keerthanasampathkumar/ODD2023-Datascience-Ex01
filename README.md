# Ex-01_DS_Data_Cleansing


## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

# CODE
LOAN_DATA_CSV
```import pandas as pd
df=pd.read_csv("/Loan_data.csv")
print(df)
df.head(10)
df.info()
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()

df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()

df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()

df.info()
df.isnull().sum()
```

DATA_SET.CSV
```
import pandas as pd
df=pd.read_csv("/Data_set.csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()

df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()

df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()

df.info()
df.isnull()
df.isnull().sum()
```

# OUTPUT
FOR LOAN_DATA:
```
import pandas as pd
df=pd.read_csv("/Loan_data.csv")
print(df)
df.head(10)
```

![image](https://github.com/Keerthanasampathkumar/ODD2023-Datascience-Ex01/assets/119477890/5beba759-64ab-4dae-9f56-f2c652effae8)

NON NULL BEFORE
```
df.info
```
![image](https://github.com/Keerthanasampathkumar/ODD2023-Datascience-Ex01/assets/119477890/ddd129d1-64f0-43df-9909-9261ae057ccd)

MODE
```
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()
```
![image](https://github.com/Keerthanasampathkumar/ODD2023-Datascience-Ex01/assets/119477890/cf59458b-b912-4f99-af53-9f73cf9b89f7)

MEAN
```
df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()
```

![image](https://github.com/Keerthanasampathkumar/ODD2023-Datascience-Ex01/assets/119477890/a07c9f97-0d11-40c1-8fa8-04f0ea61a96f)

MEDIAN
```
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()
```
![image](https://github.com/Keerthanasampathkumar/ODD2023-Datascience-Ex01/assets/119477890/b7e85da6-8d84-4113-8195-3f8479de4a09)

NON NULL AFTER
```
df.info()
```
![image](https://github.com/Keerthanasampathkumar/ODD2023-Datascience-Ex01/assets/119477890/4ca7de59-09dc-44c8-9c33-f9f378daee2d)

```
df.isnull()
```
![image](https://github.com/Keerthanasampathkumar/ODD2023-Datascience-Ex01/assets/119477890/d01afd2a-2368-40df-aef7-1c66c4443f87)

```
df.isnull().sum()
```
![image](https://github.com/Keerthanasampathkumar/ODD2023-Datascience-Ex01/assets/119477890/5e448f6b-d94c-4670-a8bf-186155958851)

MODE
```
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
```
![image](https://github.com/Keerthanasampathkumar/ODD2023-Datascience-Ex01/assets/119477890/6b0d6b85-2994-4e05-bb35-6dfea0411390)
MEAN
```
df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
```
![image](https://github.com/Keerthanasampathkumar/ODD2023-Datascience-Ex01/assets/119477890/752263f7-7679-4504-a60a-b4e5d59a49e5)
MEDIAN
```
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()
```
![image](https://github.com/Keerthanasampathkumar/ODD2023-Datascience-Ex01/assets/119477890/300ef0ca-1412-4807-82ae-8c55dd3e5125)

NON NULL AFTER
```
df.info()
```
![image](https://github.com/Keerthanasampathkumar/ODD2023-Datascience-Ex01/assets/119477890/21753c4a-de37-490f-8c42-1f7bae4f57f3)

```
df.isnull()
```
![image](https://github.com/Keerthanasampathkumar/ODD2023-Datascience-Ex01/assets/119477890/40d74b64-1a0b-4c10-9ed3-ce156011aaa0)

```
df.isnull().sum()
```
![image](https://github.com/Keerthanasampathkumar/ODD2023-Datascience-Ex01/assets/119477890/89f9f4d3-df2d-43bc-8486-82cc8f7dcf5d)

## RESULT
Thus,the given data is read,cleansed and the cleaned data is saved into the file.
