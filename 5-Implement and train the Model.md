# Implement and train the Model :


- **Ajouter le script train.py comme vous avez déja fais avec envfile.yml .**

---
![a](https://user-images.githubusercontent.com/78825764/204792103-557b0811-5fa2-4025-a2da-7218dd4d8787.PNG)
---

- **Upload la data diabetes.csv :**
---
![a](https://user-images.githubusercontent.com/78825764/204796840-7acae84c-7c81-4687-a9d9-a53875a7bbb2.PNG)
---
- **Exécuter le script train.py :**

```
config=ScriptRunConfig(source_directory="./",script="mytrain.py",compute_target='ComputeAML',environment=env)
execution=exp.submit(config)
execution.wait_for_completion(show_output=True)
```
---

![a](https://user-images.githubusercontent.com/78825764/204797417-8d2577cf-b126-476c-a001-85cc433c9377.PNG)

## **Visualiser l'expérience qu'on a crée :**

- **Cliquer sur Jobs > demo_expirement :**


![a](https://user-images.githubusercontent.com/78825764/204795989-097543fe-a083-4bab-92b3-2c7b8c7ccda0.PNG)
