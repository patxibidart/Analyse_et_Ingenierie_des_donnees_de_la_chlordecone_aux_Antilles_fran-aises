# Analyse et Ingénierie des données de la chlordécone aux Antilles

Ce projet propose une suite d'analyses statistiques et spatiales sur la pollution à la chlordécone. Pour faciliter la lecture des résultats sans installer d'environnement Python complexe, un **visualiseur de notebooks interactif** est inclus.

## 🚀 Comment utiliser le site de récapitulation ?

Le site fonctionne comme un lecteur de fichiers local. Aucune donnée n'est envoyée sur internet.

1.  Ouvrez le dossier `site_notebook/`.
2.  Lancez le fichier **`index.html`** dans votre navigateur (Chrome, Firefox ou Safari).
3.  **Déposez vos fichiers :** * Sélectionnez vos 6 notebooks (`.ipynb`) dans votre explorateur de fichiers.
    * Faites-les glisser (Drag & Drop) directement sur la zone pointillée du site.
4.  **Naviguez :** Des onglets apparaîtront en haut pour passer d'une étape de l'analyse à l'autre de manière fluide.

---

## 🎨 Consignes de Style et Présentation

L'interface a été conçue pour être **sobre, naturelle et professionnelle**, en accord avec une démarche scientifique :

- **Couleurs :** Fond clair (`#F4F6F8`), textes sombres et accents bleu-gris pour ne pas fatiguer l'œil.
- **Graphiques :** Le site respecte le rendu de vos bibliothèques (Matplotlib, Seaborn, Plotly). Pour une harmonie parfaite, veillez à utiliser des thèmes `whitegrid` ou `minimal` dans vos notebooks.
- **Typographie :** Utilisation de polices système sans empattement (Sans-serif) pour une clarté maximale des données chiffrées.

---

## 🛠️ Maintenance et Mise à jour du site

Si vous souhaitez modifier l'apparence du site (`index.html`), respectez les consignes suivantes pour ne pas casser l'outil de lecture :

### 1. Structure du Code
- **Ne pas toucher au JavaScript** à la fin du fichier : il contient la logique "magique" qui transforme le format JSON des notebooks en HTML lisible.
- **Modification du CSS :** Vous pouvez ajuster les couleurs dans la section `:root` du CSS au début du fichier pour les accorder précisément à vos graphiques.

### 2. Export des Notebooks
- Pour que le site lise correctement vos fichiers, assurez-vous d'enregistrer vos notebooks (`Ctrl+S`) après avoir **exécuté toutes les cellules**. Le site affiche les résultats qui sont *déjà* stockés dans le fichier.
- **Poids des fichiers :** Évitez les graphiques 3D trop lourds ou les cartes comportant des millions de points, ce qui pourrait ralentir la navigation dans le navigateur.

### 3. Noms des onglets
Le visualiseur utilise le nom de vos fichiers pour créer les onglets. 
- **Conseil :** Nommez vos fichiers de façon claire (ex: `01_Analyse_Sols.ipynb`) pour que la navigation soit intuitive.
