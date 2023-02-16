# Comment ajouter du contenu dans TLJH ?


## Evaluation des connaissances

Pour des petits groupes de formation (<20 personnes), un simple script bash ou Python peut suffire.

En général, j'utilise deux scripts différents : un pour envoyer les notebooks d'évaluation ainsiq que les jeux de données dans les espaces apprenant du Jupyter Hub et un pour récupérer l'évaluation.

En détail, voici ce que cela donne :

1 - J'importe dans l'espace formateur (admin) du Jupyter Hub les notebooks d'évaluation et les jeux de données

2 - Je lance le script suivant :

```python
def copy_file(students, file_name="Exercice.ipynb", remove=False):
    path = "/home"
    for name in students:
        src = os.path.join(path, f"jupyter-jupyadmin", file_name)
        dst = os.path.join(path, f"jupyter-{name}", f"Exercice_{name}.ipynb")
        if os.path.isfile(dst) is True:
            answer = input("Le fichier d'exercices existe déjà. Souhaitez-vous continuer ? (o/n)")
            if answer=="o":
                shutil.copyfile(src, dst)
                os.chmod(dst, 0o777)
                print(src, dst)
            else:
                print(f"Exercice_{name}.ipynb non modifié")
```

3 - Je vérifie que tout s'est correctement déroulé dans mon espace "apprenant" et que je peux accéder aux différents fichiers de l'évaluation

4 - Je récupère les notebooks en fin d'évaluation grâce au script suivant :

```python
def copy_file(students):
    path = "/home"
    for name in students:
        src = os.path.join(path, f"jupyter-{name}", f"Exercice_{name}.ipynb")
        dst = os.path.join(path, f"jupyter-jupyadmin/Results", f"Exercice_{name}.ipynb")
        shutil.copyfile(src, dst)
        print(src, dst)
    shutil.make_archive("results", 'zip', os.path.join(path, f"jupyter-jupyadmin", "Results"))
```

___

En plus de l'évaluation "manuelle" présentée précédemment, il existe différentes bibliothèques Python pour effectuer cette tâche. Voici une liste des bibliothèques existantes :

- Nbgrader 