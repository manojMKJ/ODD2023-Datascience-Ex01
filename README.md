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

# CODE:

# LOAN_DATA_CSV:
```
import pandas as pd
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
# DATA_SET.CSV:
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
## FOR LOAN_DATA:
# DATA:
```
import pandas as pd
df=pd.read_csv("/Loan_data.csv")
print(df)
df.head(10)
```
![DATA](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex01/assets/121418522/2a6c2342-4f9d-465a-b0c9-6b34d3c0036a)

# NON NULL BEFORE:
```
df.info
```
![info](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex01/assets/121418522/d2eb26c9-1a50-490e-b5eb-916682eccc34)

# MODE:
```
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()
```
![MODE](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex01/assets/121418522/ceb9d14e-ce00-47d6-b1dd-c175745c1dd5)

# MEAN:
```
df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()
```
![MEAN](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex01/assets/121418522/5e393bb6-7958-47b6-821d-4248b6c0393c)

# MEDIAN:
```
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()
```
![MEDIAN](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex01/assets/121418522/ea74ab58-1c5b-4021-9a6f-226c2a04b18b)

# NON NULL AFTER:

```
df.info()
```
![after](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex01/assets/121418522/b532b301-1fad-436c-bf15-3ee2535e4e90)

```
df.isnull().sum()
```
![sum](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex01/assets/121418522/3dd82ddd-f3b6-438c-af5c-b5faada58070)

## FOR DATA_SET:
# DATA:
```
import pandas as pd
df=pd.read_csv("/Data_set.csv")
print(df)
df.head(10)
```
![DATA1](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex01/assets/121418522/3a57bf29-ca7f-447e-84a6-8c4de79cc6c4)

# NON NULL BEFORE:
```
df.info()
```
![INFO1](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex01/assets/121418522/404c5862-d322-411f-a7e5-74006a11526a)

```
df.isnull()
```
![null](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex01/assets/121418522/8771c2a8-5e00-47ba-950f-5910087c86a6)

```
df.isnull().sum()
```
![sum1](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex01/assets/121418522/470baff8-b6e1-48ad-8d95-94cfd425851b)

# MODE:
```
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
```
![MODE1](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex01/assets/121418522/73f49e75-e6f9-4bff-80a1-b94529a931ee)

# MEAN:
```
df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
```
![MEAN1](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex01/assets/121418522/b62342d9-97fa-44f1-ac58-fe1396bfeb16)

# MEDIAN:
```
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()
```
![MEDIAN1](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex01/assets/121418522/e4fb6a1b-4ab6-4187-96b6-fd2659276687)

# NON NULL AFTER:
```
df.info()
```
![after info](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex01/assets/121418522/97d0c270-a76d-4c88-8eeb-84d45f40110c)

```
df.isnull()
```
![isnull](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex01/assets/121418522/cb5c56ff-529e-4d4d-8896-d48595d29636)

```
df.isnull().sum()
```
![null sum](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex01/assets/121418522/918a4cc2-154d-40ac-99f2-da647104206b)

# RESULT
Thus,the given data is read,cleansed and the cleaned data is saved into the file.
