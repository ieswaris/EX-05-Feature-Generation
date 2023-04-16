# EX-05-Feature-Generation

# AIM

To read the given data and perform Feature Generation process and save the data to a file.

# Explanation

Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.

# ALGORITHM

# STEP 1

Read the given Data

# STEP 2

Clean the Data Set using Data Cleaning Process

# STEP 3

Apply Feature Generation techniques to all the feature of the data set

# STEP 4

Save the data to the file

# CODE
```
data.csv
import pandas as pd   
import seaborn as sbn 
df=pd.read_csv("/content/data.csv") 
df.info() 
df.isnull().sum()
from sklearn.preprocessing import LabelEncoder 
le = LabelEncoder() 
df['Ord_2'] = le.fit_transform(df['Ord_2']) 
sbn.set(style ="darkgrid") 
sbn.countplot(df['Ord_2'])
from sklearn.preprocessing import OneHotEncoder 
enc = OneHotEncoder() 
enc = enc.fit_transform(df[['City']]).toarray() 
encoded_colm = pd.DataFrame(enc) 
df = pd.concat([df, encoded_colm], axis=1) 
df = df.drop(['City'], axis=1) 
df.head(10) 
df = pd.get_dummies(df, prefix=['Ord_2'], columns=['Ord_2']) 
df.head(10) 
df = pd.get_dummies(df, prefix=['Ord_1'], columns=['Ord_1']) 
df.head(10)
```

# encoding.csv
```
import pandas as pd 
import seaborn as sbn 
data=pd.read_csv("/content/Encoding Data.csv") 
data.info() 
data.isnull().sum() from sklearn.preprocessing import LabelEncoder 
le = LabelEncoder() data['ord_2'] = le.fit_transform(data['ord_2']) 
sbn.set(style ="darkgrid") 
sbn.countplot(data['ord_2']) from sklearn.preprocessing import OneHotEncoder 
en = OneHotEncoder() 
en = en.fit_transform(data[['nom_0']]).toarray() 
encoded_colm = pd.DataFrame(en) 
data= pd.concat([data, encoded_colm], axis=1) 
data= data.drop(['nom_0'], axis=1) 
data.head(10) 
data = pd.get_dummies(df, prefix=['bin_2'], columns=['bin_2']) 
data.head(10)
```

# titanic.csv
```
import pandas as pd 
import seaborn as sbn 
dt=pd.read_csv("/content/titanic_dataset.csv") 
dt.info() 
dt.isnull().sum() 
dt['Age']=dt['Age'] . fillna(dt ['Age'].mean()) 
dt ['Cabin']=dt['Cabin']. fillna(dt['Cabin']. mode() [0]) 
dt ['Embarked']=dt['Embarked'] . fillna(df ['Embarked'].mode( )[0]) 
dt.isnull().sum( ) from sklearn.preprocessing import LabelEncoder 
lc = LabelEncoder() 
df['Sex'] = lc.fit_transform(df['Sex']) 
sbn.set(style ="darkgrid") 
sbn.countplot(df['Sex']) from sklearn.preprocessing import OneHotEncoder 
enc= OneHotEncoder() 
enc= enc.fit_transform(dt[['Name']]).toarray() 
encoded_colm = pd.DataFrame(enc) 
dt= pd.concat([dt, encoded_colm], axis=1) 
dt= dt.drop(['Name'], axis=1) 
dt.head(10) 
dt = pd.get_dummies(dt, prefix=['Ticket'] ,columns=['Ticket']) 
df.head(10) 
dt = pd.get_dummies(dt, prefix=['Embarked'] ,columns=['Embarked']) 
df.head(10)
```

# OUPUT

# Data.csv

![image](https://user-images.githubusercontent.com/127847210/232328702-5886933a-5c10-47e2-b7e3-18171e743296.png)

![image](https://user-images.githubusercontent.com/127847210/232328746-02560c94-4be3-443d-b813-a427ed384ed1.png)

![image](https://user-images.githubusercontent.com/127847210/232328761-82e98532-121b-46bd-b266-134073b85be6.png)

![image](https://user-images.githubusercontent.com/127847210/232328775-7326483b-7550-4fb1-8902-51f4fc38e08a.png)

![image](https://user-images.githubusercontent.com/127847210/232328820-19834a7a-e1c7-406c-ae58-dceea04de9cd.png)

# Encoding.csv

![image](https://user-images.githubusercontent.com/127847210/232328895-1da84619-6d18-4048-b402-5eac60391eb4.png)

![image](https://user-images.githubusercontent.com/127847210/232328904-4e98af54-ea56-44f1-a5ec-29d9de2d82bb.png)

![image](https://user-images.githubusercontent.com/127847210/232328918-95b2a696-70cb-471a-b921-a34b0548db8f.png)

![image](https://user-images.githubusercontent.com/127847210/232328951-42bcd0f5-80ad-4d8e-86c5-18b4750a4929.png)

# Titanic.csv

![image](https://user-images.githubusercontent.com/127847210/232328965-a76c02af-a11d-4b3f-af09-23595a292122.png)

![image](https://user-images.githubusercontent.com/127847210/232328988-c3340d91-8064-43cc-b067-333d82c27ea3.png)

![image](https://user-images.githubusercontent.com/127847210/232329000-387ce431-40db-4eee-8cae-c314562bd889.png)

![image](https://user-images.githubusercontent.com/127847210/232329052-773575ea-e513-4e37-9fdc-5c8b558c094c.png)

![image](https://user-images.githubusercontent.com/127847210/232329070-48bdddc5-25eb-44fc-be98-c20bc1fa0db8.png)

![image](https://user-images.githubusercontent.com/127847210/232329077-0dfdab1a-3e24-43e5-b6b8-1707581d75e6.png)

# RESULT:

Thus the program for Feature Generation is executed successfully.

