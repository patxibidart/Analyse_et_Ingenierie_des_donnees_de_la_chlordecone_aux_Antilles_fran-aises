# Analyse et Ingénierie des données de la chlordécone aux Antilles françaises

La chlordécone est un pesticide organochloré utilisé aux Antilles françaises jusqu’au début des années 1990. Sa persistance dans les sols, les eaux et les chaînes alimentaires en fait aujourd’hui un enjeu sanitaire, environnemental et socio-économique majeur.

Ce dépôt regroupe les travaux de recherche, d'analyse et de visualisation des données concernant l'impact environnemental et sanitaire de la chlordécone aux Antilles françaises (Martinique et Guadeloupe).

L'objectif de ce projet est de traiter les données brutes, de les nettoyer, et d'en extraire des analyses statistiques et spatiales afin de mieux comprendre la répartition et les conséquences de cette pollution.

## 📊 Consulter le rapport interactif

L'ensemble des analyses (Jupyter Notebooks) est compilé et accessible sous forme de site web interactif et professionnel.

👉 **[Voir le site des analyses](https://patxibidart.github.io/Analyse_et_Ingenierie_des_donnees_de_la_chlordecone_aux_Antilles_fran-aises/)** *(Note: vérifiez que ce lien correspond bien à votre URL finale)*

---

## 📂 Structure du projet

- `data/` : Contient les jeux de données bruts et nettoyés utilisés pour l'analyse.
- `fig/` : Contient les figures, graphiques et cartes générés par le code.
- `site_notebook/` : **Dossier principal du site web**. Il contient les notebooks finaux et les fichiers de configuration de Jupyter Book.
- `.github/workflows/` : Contient l'automate de déploiement (`deploy.yml`) qui met à jour le site à chaque modification.

---

## 🛠️ Consignes de maintenance du site (À lire avant toute modification)

Le site web est généré automatiquement grâce à **Jupyter Book** et **GitHub Actions**. Pour garantir que le site se mette à jour correctement sans erreur "404" ou "Build failed", veuillez respecter scrupuleusement les règles suivantes :

### 1. Ajout ou modification d'un Notebook
- Tous les notebooks destinés à apparaître sur le site **doivent** être placés dans le dossier `site_notebook/`.
- Si vous modifiez un notebook existant, il vous suffit de faire un `git push` (ou d'importer le fichier modifié sur GitHub). Le site se mettra à jour tout seul en 2 à 3 minutes.

### 2. Règles de nommage (Très important)
- Les noms de vos fichiers `.ipynb` ne doivent contenir **aucun espace** et **aucun accent**. 
- Utilisez des tirets du bas (`_`). *Exemple : `01_chargement_donnees.ipynb`*.

### 3. Mise à jour du menu (`_toc.yml`)
Si vous ajoutez un **nouveau** notebook ou si vous en renommez un, le site plantera si vous ne mettez pas à jour le fichier `_toc.yml` (situé dans `site_notebook/`).
- Ouvrez `_toc.yml`.
- Ajoutez ou modifiez le nom du fichier **sans l'extension .ipynb**.
  ```yaml
  format: jb-book
  root: index  # (ou intro, selon votre configuration de page d'accueil)
  chapters:
    - file: 01_chargement_decouverte
    - file: 02_nettoyage_cleaning
    # Ajoutez le nouveau fichier ici :
    - file: 07_nouvelle_analyse
