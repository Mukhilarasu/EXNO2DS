# EXNO2DS
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

dt = pd.read_csv("/content/titanic_dataset.csv")

dt
dt.info()
dt.shape
dt.head(4)
dt.tail(4)

dt.set_index("PassengerId", inplace=True)

dt.describe()
dt.nunique()

dt["Survived"].value_counts()

per = (dt["Survived"].value_counts() / dt.shape[0] * 100).round(2)
per

sns.countplot(data=dt, x="Survived")

dt

dt.Pclass.unique()

dt.rename(columns={"Sex": "Gender"}, inplace=True)
dt

sns.catplot(
    x="Gender",
    col="Survived",
    kind="count",
    data=dt,
    height=5,
    aspect=0.7
)

sns.scatterplot(x=dt["Age"], y=dt["Fare"])

sns.jointplot(x="Age", y="Fare", data=dt)

fig, ax1 = plt.subplots(figsize=(8, 5))
sns.boxplot(
    ax=ax1,
    x="Pclass",
    y="Age",
    hue="Gender",
    data=dt
)

sns.catplot(
    data=dt,
    col="Survived",
    x="Gender",
    hue="Pclass",
    kind="count"
)

corr = dt.corr()
sns.heatmap(corr, annot=True)

sns.pairplot(dt)

```

<img width="1806" height="424" alt="530334618-f5504073-9e25-410b-b7f3-47a97369d9be" src="https://github.com/user-attachments/assets/d0dcd53c-2c52-4189-b7ca-f0274925fdd1" />

<img width="1854" height="362" alt="530334650-506875e2-3a87-47dd-9aa2-ca91ebc93aee" src="https://github.com/user-attachments/assets/40d5dc61-36d3-49cc-8773-e312a31d5137" />


<img width="1798" height="548" alt="530334689-4fc8d02f-6c29-4a74-890e-3b7050017ab2" src="https://github.com/user-attachments/assets/a5d79076-e0c6-4d14-9c84-00de46154f48" />


<img width="1849" height="545" alt="530334718-96a77d9c-e14a-49da-8a30-79a4739a0243" src="https://github.com/user-attachments/assets/ac264560-1c8a-471d-b550-c76e0f7eb93a" />

<img width="1797" height="429" alt="530334754-cdaa48b4-d4a4-45c9-87df-382d6223e824" src="https://github.com/user-attachments/assets/db983f43-9e97-41e8-9a08-7fc7b57b4639" />


<img width="1795" height="388" alt="530334781-2708d8b2-6284-48a7-a492-2ed6c4eae62c" src="https://github.com/user-attachments/assets/b96e285f-7fe3-4473-b1d8-c73df7dea84e" />


<img width="1795" height="519" alt="530334808-99abc578-f9fd-4bef-9baa-c40f04d95881" src="https://github.com/user-attachments/assets/4d80ec70-dee5-4beb-be4e-086aa20e2742" />


<img width="1794" height="477" alt="530334846-6e950c7c-4550-45b0-abae-4febd0af99bb" src="https://github.com/user-attachments/assets/fb8c34f9-8eb8-48cd-a432-421162eeaedf" />


<img width="1786" height="421" alt="530334879-0875a44f-fb1f-486d-b6cd-30f124bc117b" src="https://github.com/user-attachments/assets/57f1acba-9b5b-4a31-ac2a-e2b07c678759" />


<img width="1804" height="573" alt="530334907-b5c340d2-ac17-4398-a5de-673f66c5f08c" src="https://github.com/user-attachments/assets/b319e8d0-32a0-4661-846e-6dc4aabd6bc0" />


<img width="1785" height="426" alt="530335006-32ba9faa-b79b-489b-9774-5facc620e2d8" src="https://github.com/user-attachments/assets/0825eb7f-812f-4478-9361-62ed35f002f8" />


<img width="1792" height="484" alt="530335087-3f40370c-78c8-4a8b-be09-ccc001e70f8d" src="https://github.com/user-attachments/assets/e4d46ec9-6597-40a5-96b0-cb61abdd7948" />




<img width="1811" height="509" alt="530335163-57fc427f-46f4-4515-a3d8-a93c5a1eff24" src="https://github.com/user-attachments/assets/a8a0f0de-2ac8-4c01-b75f-af30f835f779" />


<img width="1851" height="417" alt="530335200-7a9cd019-bce3-4c53-a8e5-3da73e184013" src="https://github.com/user-attachments/assets/2e68d03d-fc0a-4de1-80c4-3d9559a42b06" />



<img width="1834" height="412" alt="530335233-0fe47016-608e-439b-912e-1e98ac3bd748" src="https://github.com/user-attachments/assets/49a0df6c-8128-4762-998b-29066c946b8d" />

# RESULT
        <<INCLUDE YOUR RESULT HERE>>
