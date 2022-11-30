# Implement and train the Model :



- **Ajouter le script train.py comme vous avez déja fais avec envfile.yml .**

---
![a](https://user-images.githubusercontent.com/78825764/204792103-557b0811-5fa2-4025-a2da-7218dd4d8787.PNG)
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
---
- **Vous pouvez s'assurer que le status est Completed

![a](https://user-images.githubusercontent.com/78825764/204798340-6eadce19-1381-408b-a300-caf7a8ace81c.PNG)
---

- **