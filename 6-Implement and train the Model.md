# Implement and train the Model :

- **Train our data with RandomForestClassifier :**

```
from sklearn.ensemble import RandomForestClassifier
rf = RandomForestClassifier(n_estimators=100, random_state=0)
rf.fit(trainx, trainy)
print("Accuracy on training set: {:.3f}".format(rf.score(trainx, trainy)))
print("Accuracy on test set: {:.3f}".format(rf.score(testx, testy)))
```

![a](https://user-images.githubusercontent.com/78825764/204814268-40f06be2-b5dd-4ece-b7ba-0608c49f564a.PNG)

---

- **Define and Plot the Confusion Matrix :**

```
#Define conf_matrix
y_pred=rf.predict(testx)
classification_report(testy,y_pred)
conf_matrix =confusion_matrix(testy,y_pred)
# Print the confusion matrix using Matplotlib
import matplotlib.pyplot as plt
fig, ax = plt.subplots(figsize=(7.5, 7.5))
ax.matshow(conf_matrix, cmap=plt.cm.Blues, alpha=0.3)
for i in range(conf_matrix.shape[0]):
    for j in range(conf_matrix.shape[1]):
        ax.text(x=j, y=i,s=conf_matrix[i, j], va='center', ha='center', size='xx-large')
 
plt.xlabel('Predictions', fontsize=18)
plt.ylabel('Actuals', fontsize=18)
plt.title('Confusion Matrix', fontsize=18)
plt.show()
```
![a](https://user-images.githubusercontent.com/78825764/204816051-79c6d077-1a82-4b56-89ba-46b624e96b3f.PNG)

---

- **Print Accuracy of train and test set :**

```
acc=accuracy_score(testy,y_pred)
print("Accuracy",acc)
print(accuracy_score(testy,y_pred))
```

![a](https://user-images.githubusercontent.com/78825764/204816959-18d31579-2597-4a5b-955d-ef0f48863081.PNG)

- **Save the model :**

```
joblib.dump(rf, "./diabeticmodel.pkl")
```
![a](https://user-images.githubusercontent.com/78825764/204817726-711b195f-a028-4472-bbab-ae74e30e39fe.PNG)


