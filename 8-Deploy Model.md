## Deploy the Model :
---

- ## **Register the model in your workspace :**

```
# Register the model in workspace
from azureml.core import Model
model = Model.register(ws,model_path="./diabeticmodel.pkl",model_name="first_ml_model")
model = Model(ws,"first_ml_model")
```

![a](https://user-images.githubusercontent.com/78825764/204823374-ef7d13ad-89f6-4e0c-a468-7d9ba42ac30f.PNG)

---

- ## **Create a new envirement for deployement:**

```
from azureml.core.model import InferenceConfig
from azureml.core.environment import CondaDependencies
myenv=Environment(name="demo-env")
conda_packages = ['numpy']
pip_packages = ['azureml-sdk','azureml-defaults','scikit-learn']
mycondaenv = CondaDependencies.create(conda_packages=conda_packages, pip_packages=pip_packages, python_version='3.6.2')
myenv.python.conda_dependencies=mycondaenv
myenv.register(workspace=ws)
```

![a](https://user-images.githubusercontent.com/78825764/204824574-7d7749bf-63c6-4089-9310-6321d2cc8947.PNG)

---
- ## **Add score.py script**

![a](https://user-images.githubusercontent.com/78825764/204825774-1ddd6777-8223-4035-a7f2-b37a74294600.PNG)

---

- ## **Add InferrenceConfig method with our new environment and score.py entry script:**

```
inference_config = InferenceConfig(environment=myenv,source_directory='.',entry_script='score.py')
```


![a](https://user-images.githubusercontent.com/78825764/204826075-9a84dda1-588a-40bf-8c78-e271d80a2994.PNG)
---
- ## **Add deploy Configuration :**

```
from azureml.core.webservice import AciWebservice
aciconfig = AciWebservice.deploy_configuration(cpu_cores=1,memory_gb=1)
```
![a](https://user-images.githubusercontent.com/78825764/204826470-153980ce-f94a-42e3-8e8e-1adc9122c83a.PNG)

---
- ## **Deploy the model:**


```
# Deploying the model
service = Model.deploy(ws,"endpointsmodel", #This is endpoint name
                           models=[model],
                           inference_config=inference_config,
                           deployment_config=aciconfig,
                           #deployment_target=predenv,
                           overwrite=True)
service.wait_for_deployment(show_output=True)
url = service.scoring_uri
print(url)
```







