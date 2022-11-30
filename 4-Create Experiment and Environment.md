# Create Experiment and Environment

---
 - ## **Import libraries :**
 
 ---

```
import azure.core
from azureml.core import Workspace,Environment,Experiment,ScriptRunConfig
from azureml.core.compute import AmlCompute, ComputeTarget
from azureml.core.compute_target import ComputeTargetException
 ```
 ---
 
 - **crtl+Entréé pour éxecuter la cellule :**

![a](https://user-images.githubusercontent.com/78825764/204784276-ea1f63a0-63c5-4372-aebd-2a492f1e5432.PNG)

---
- **Créer une variable ws qui renvoie à votre workspace :**

```
ws=Workspace.from_config()
```
![a](https://user-images.githubusercontent.com/78825764/204784924-f6dff83b-2d07-4f26-8f3b-44c2968ab544.PNG)
---

- ## **Créer une expérience :**

```
# Create Experiment
exp = Experiment(ws,'demo_expirement')
```
---
![image](https://user-images.githubusercontent.com/78825764/204786338-148b696c-ac8c-4302-9ccf-3ca178c878be.png)
---
- ## **Créer votre environement d'éxecution :**
---
- **Ajouter le script envfile.yml :**



**1.Cliquer sur Upload files**
  
![a](https://user-images.githubusercontent.com/78825764/204787891-b4d36bb3-2c77-40b3-ae8f-91186955a1e1.PNG)

  ---
   **2.Ajouter envfile.yml :**
 
![a](https://user-images.githubusercontent.com/78825764/204788746-22248046-b533-4ffc-974e-71ff27b3a102.PNG)
  
---
- **Ajouter cette cellule à votre notebook :**
```
# Create environment to execute your code
env = Environment.from_conda_specification(name="azure_ml",file_path="./envfile.yml")
```
---


![a](https://user-images.githubusercontent.com/78825764/204789691-9e311f4a-69be-4cf2-b5c5-a26a7774b515.PNG)


