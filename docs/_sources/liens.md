# Pour aller plus loin avec TLJH

## 📓 Documentation officielle TLJH

La **documentation officielle TLJH** est **assez complète**. Elle présente beaucoup d'informations que je n'ai pas présentées comme par exemple les **différents types d'authentifications**, l'installation sur d'**autres fournisseurs de cloud** qu'Azure ou même sur votre propre serveur...

Lien : https://tljh.jupyter.org/en/latest/

## 📚 Documentation officielle Jupyter Hub

Si vous avez besoin de déployer un Jupyter Hub pour **beaucoup d'utilisateurs (> 100)**, il est préférable de déployer le JupyterHub avec **Kubernetes** avec la documentation **Zero to JupyterHub (ZTJH)**.

Lien : https://z2jh.jupyter.org/en/stable/

## ➕ Modules complémentaires de TLJH

### Nbgitpuller

Si vous utilisez un **dépôt Git** pour gérer le **contenu de vos formations**, la **bibliothèque nbgitpuller** vous permet de **récupérer le contenu** de votre dépôt Git à l'**ouverture des espaces** des apprenants ou des formateurs dans le JupyterHub.

Lien : https://hub.jupyter.org/nbgitpuller/

### Nbgrader

Cette **bibliothèque complémentaire** de TLJH permet de mettre en place une **évaluation automatique** des notebooks d'examens ou de tests. Elle n'est **pas très simple** à mettre en place en l'état actuel et n'est donc **pas très pertinente** pour des formations en **petits groupes** (<20 personnes).

Lien : https://nbgrader.readthedocs.io/en/stable/

## 🪐 Exemples de cas d'usages des JupyterHubs

### Université de Berkeley (Californie)

L'université de **Berkeley** a mis en place des formations à la **data science** pour les étudiants de **tous les domaines** grâce à un JupyterHub (ZTJH avec Kubernetes).

Lien : http://www.data8.org/

### Université de Lyon

Le **département de mécanique** de l'**université de Lyon** a mis en place un **JupyterHub** pour des TP. La bibliothèque [Nbgrader](https://nbgrader.readthedocs.io/en/stable/) a aussi été utilisée pour effectuer des **évaluations**.

Lien : https://perso.univ-lyon1.fr/marc.buffat/COURS/BOOK_VALIDATION_HTML/intro.html

### Université Paris-Saclay

Différents départements de l'**université Paris-Saclay** utilisent des **JupyterHubs** pour leurs enseignements scientifiques.

Lien : https://jupyterhub.ijclab.in2p3.fr/

