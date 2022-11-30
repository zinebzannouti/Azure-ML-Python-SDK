# Implement and train the Model :


- **Ajouter le script train.py comme vous avez déja fais avec envfile.yml .**

---
![a](https://user-images.githubusercontent.com/78825764/204792103-557b0811-5fa2-4025-a2da-7218dd4d8787.PNG)

- **Exécuter le script train.py :**

```
config=ScriptRunConfig(source_directory="./",script="mytrain.py",compute_target='ComputeAML',environment=env)
execution=exp.submit(config)
execution.wait_for_completion(show_output=True)
```
