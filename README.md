# off-explore
Une exploration des données d'[Open Food Facts](https://fr.openfoodfacts.org/).

## Prérequis
Vous devez **télécharger les données d'Open Food Facts** exportées au format CSV <https://static.openfoodfacts.org/data/en.openfoodfacts.org.products.csv>.
Ce fichier pèse 4.3 Go, je vous invite donc à **lancer le téléchargement dès que possible**.

Pendant que les données sont téléchargées, vous devez vérifier que vous avez sur vos machines, ou installer le cas échéant :
* [git](https://git-scm.com/book/fr/v2/D%C3%A9marrage-rapide-Installation-de-Git) ;
* [miniconda](https://docs.conda.io/en/latest/miniconda.html) avec une version récente de **python 3** (3.8 et suivantes ; actuellement python 3.9) ou, éventuellement, [anaconda](https://www.anaconda.com/products/individual) avec une version récente de python 3 (idem) si vous l'avez déjà ;
* [JupyterLab](https://jupyter.org/install) ou jupyter notebook classique.


## Mise en place initiale

Nous allons travailler dans un environment virtuel conda qui contiendra python 3 et les bibliothèques nécessaires à la visualisation et à l'analyse des données: pandas, matplotlib, seaborn...

J'ai préparé un fichier `environment.yml` qui permet de créer un environnement nommé `off-explore` et d'installer les dépendances.

Dans le terminal (Linux, macOS), ou dans "Anaconda Prompt" (Windows), exécutez la commande:

```sh
conda env create -f environment.yml
```

## Session de travail

Pour travailler dans l'environnement, vous devez l'activer dans le terminal avant de lancer jupyter-lab :
```sh
conda activate off-explore
jupyter-lab
```

En fin de session, après avoir fermé jupyter-lab, vous pouvez désactiver l'environnement conda :
```sh
conda deactivate
```

## OpenFoodFacts
Dans cette série de notebooks, nous allons explorer les données contenues dans la base de données ouverte sur les produits alimentaires [Open Food Facts](https://fr.openfoodfacts.org/).
Nous allons notamment analyser le profil nutritionnel des produits alimentaires recensés.

Open Food Facts est une base de données ouverte sur les produits alimentaires.
Elle est produite et gérée comme un [bien commun numérique](https://fr.wikipedia.org/wiki/Biens_communs_num%C3%A9riques).
Tout le monde peut contribuer des données sur les produits alimentaires emballés : photos, ingrédients, valeurs nutritionnelles etc.
Cette base de données a permis la construction de nombreuses applications sur téléphone mobile, notamment d'applications de scan de produits pour aider les consommateurs pendant leurs achats.


## Notebooks


* [01 - Charger les données d'Open Food Facts](https://github.com/moreymat/off-explore/blob/master/notebooks/01%20-%20Charger%20les%20donn%C3%A9es%20d'OpenFoodFacts.ipynb)
* [02 - Filtrer les données d'Open Food Facts](https://github.com/moreymat/off-explore/blob/master/notebooks/02%20-%20Filtrer%20les%20donn%C3%A9es%20d'OpenFoodFacts.ipynb)
* [03 - Nettoyer les données d'Open Food Facts](https://github.com/moreymat/off-explore/blob/master/notebooks/03%20-%20Nettoyer%20les%20donn%C3%A9es%20d'OpenFoodFacts.ipynb)
* [04 - Explorer les données d'Open Food Facts](https://github.com/moreymat/off-explore/blob/master/notebooks/04%20-%20Explorer%20les%20donn%C3%A9es%20d'OpenFoodFacts.ipynb)
* [04b - Explorer les données d'Open Food Facts avec dirty-cat ](https://github.com/moreymat/off-explore/blob/master/notebooks/04b%20-%20Explorer%20les%20donn%C3%A9es%20d'Open%20Food%20Facts%20-%20dirty-cat.ipynb)
* [05 - Explorer les données d'Open Food Facts - t-SNE](https://github.com/moreymat/off-explore/blob/master/notebooks/05%20-%20Explorer%20les%20donn%C3%A9es%20d'OpenFoodFacts%20-%20t-SNE.ipynb)
