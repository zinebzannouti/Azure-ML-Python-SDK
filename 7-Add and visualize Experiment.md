## **Créer une expérience avec le script mytrain_log.py :**
---
- **Ajouter le script mytrain_log.py**

![a](https://user-images.githubusercontent.com/78825764/204818997-0bf304c7-13c7-478b-9c14-5e2a86f729ca.PNG)
---
- **Exécuter le script avec l'expérience exp et l'environnement env qu'on a déjà créer:**

```
config=ScriptRunConfig(source_directory="./",script="mytrain_log.py",compute_target='ComputeAML',environment=env,
                            arguments=['--min_samples_leaf',5,
                                       '--min_samples_split',7])
execution=exp.submit(config)
```

![a](https://user-images.githubusercontent.com/78825764/204819766-55ca7aa8-9c82-4686-bfda-cfdd0edf5660.PNG)
---
## **Visualiser votre demo_expirement**
- **Cliquer sur Jobs > demo_expirement :**


![a](https://user-images.githubusercontent.com/78825764/204795989-097543fe-a083-4bab-92b3-2c7b8c7ccda0.PNG)
---
- **Vous pouvez s'assurer que le status du job est Completed**

![a](https://user-images.githubusercontent.com/78825764/204820689-ed31f595-7063-4ee6-b4e7-4a0a6f50cb55.PNG)

---

- **Cliquer sur le nom de job créer**

![a](https://user-images.githubusercontent.com/78825764/204821000-e70586be-968e-48b3-a889-7063515f58b5.PNG)


- **Vous pouvez voir toutes les informations sur le modèle : Metrics , Outputs+logs...**
