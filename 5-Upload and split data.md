# Upload and split data

- **Upload la data diabetes.csv :**
---
![a](https://user-images.githubusercontent.com/78825764/204796840-7acae84c-7c81-4687-a9d9-a53875a7bbb2.PNG)

---

- **Importer les bibliothèques qu'on va utilisé :**
```
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import classification_report,confusion_matrix,accuracy_score,auc
import pandas as pd
import joblib
import argparse
```


![a](https://user-images.githubusercontent.com/78825764/204805788-5ef309fd-d6dd-42cf-a8c5-f9c4104f05dc.PNG)
---
- **Read the data and print the columns :**

```
data=pd.read_csv("./diabetes.csv")
print(data.columns)
```
![a](https://user-images.githubusercontent.com/78825764/204807437-3d8a94c5-b3be-40f7-afc4-c10f09546fea.PNG)


