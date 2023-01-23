# Classificateurs

On veut automatiser la reconnaissance de motifs dans les données. On entraîne pour cela des modèles, qu'on désigne comme des *classificateurs*. Dans cette partie on s'intéressera aux différentes approches possibles pour créer et entraîner un classificateur, selon la nature de la tâche à réaliser. 
À noter que l'on modélise un objet comme un vecteur de $\mathbb{R}^n$, où $n$ est le nombre de caractéristiques utilisées pour décrire l'objet. Appellons $\vec{X}$ cet objet, on a ainsi: $\vec{X} \in \mathbb{R}^n$. 

## 1. Classificateurs paramétriques

Soit un jeu de données : $\left(\vec{X_i}, w_i\right)$ où $\vec{X_i}$ est le motif présent dans le jeu de données et, $w_i$ la classe. Cette dernière est donnée comme vérité terrain. Il est courant de diviser ce jeu de données en deux sous ensembles; 70% vont dans l'ensemble d'entraînement, et les 30% restants dans l'ensemble test.

***Note***: Une donnée ne peut pas se trouver dans les deux ensembles.

Pour trouver un classificateur permettant de déârtager ces données, on suppose que $\left(\vec{X_i}, w_i\right)$  sont modélisés par des distributions; $\vec{X}: P$ et $w:Q$. On décrit ainsi le jeu de données par : $\left(\vec{X_i}, w_i\right) \approx  <P, Q>$. Durant la phase d'entraînement on essaye de déterminer la distribution sous-jacente.

Parmi les classificateurs paramétrqiues nous nous pencherons ici sur :
- [Les classificateurs bayésiens](/lab/tree/bayesian_classifier.ipynb)
- [Les classificateurs bayésiens naïfs](/lab/tree/naive_bayes_classifier.ipynb)


## 2. Classificateurs non-paramétriques

Le problème avec les modèles paramétriques est qu'ils dépendent des assomptions faites sur la distribution sous-jacente des données. On tente ici une approche différente avec des modèles dits *non-paramétriques*. On cherche une *consistence universelle*. On ne fait ainsi aucune hypothèse sur la distribution $<P, Q>$, mais l'on échantillonne depuis la probabilité postérieure. Plusieurs classificateurs non-paramétriques seront étudiés ici :
- [Le "K-Nearest Neighbor"](/lab/tree/knn.ipynb)
- [Les arbres K-dimensionnels](/lab/tree/k-d_trees.ipynb)
- [Les arbres décisionnels](/lab/tree/decision_trees.ipynb)
- [Les classificateurs linéaires](/lab/tree/linear_classifiers.ipynb)

Finalement nous étuderions les [réseaux neuronaux](/lab/tree/NN.ipynb), et découvrirons les plus récents [réseaux neuronaux physiquement informés](/lab/tree/PINN.ipynb). Les *Notebooks* ici présents sont réalisés en utilisant mes supports de cours (Landoni) ainsi que les exemples de [Scikit-Learn](https://scikit-learn.org/stable/index.html). Pour davantage de détails sur les calculs, le livre [Pattern Classification by Richard O. Duda, David G. Stork, Peter E.Hart](https://www.amazon.it/Pattern-Classification-Richard-Duda/dp/0471056693) est parfois utilisé.
