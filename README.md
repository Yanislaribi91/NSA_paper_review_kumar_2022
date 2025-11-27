# NSA_paper_review_kumar_2022

# Reproduction et exploration de l’article Kumar & Kumar (2022)

Ce dépôt contient le code que nous avons développé pour :

1. **reproduire partiellement les résultats de l’article de Kumar & Kumar (2022)**  
   (« An improved fuzzy clustering algorithm based on particle swarm optimization »),  

2. **expérimenter plus en profondeur certaines des techniques introduites dans l’article**,  
   notamment l’optimisation par essaim de particules (PSO) et le clustering flou (IFCM).

Trois notebooks composent ce repo, dont le contenu de chacun est détaillé ci-après :

---

## **1. `comparaison_algo_clustering_kumar_2022.ipynb`**

Ce notebook regroupe une **comparaison pratique entre plusieurs algorithmes de clustering** :

- PSOIFCM (implémentation basée sur l’article),
- FCM classique,
- K-means,
- d’autres méthodes de référence disponibles dans `scikit-learn`.

Objectifs du notebook :

- comparer les partitions obtenues sur différents jeux de données (réels et artificiels),
- analyser l’influence de la nouvelle distance $d_{\mathrm{new}}$,
- mesurer et visualiser des métriques comme l’accuracy, l’ICD (inter cluster distance) , ou la valeur de la fonction objectif à minimiser (OFV).


---

## **2. `PSOIFCM_reproduction_kumar_2022.ipynb`**

notebook dédié à 

- l’implémentation complète de l’algorithme **PSOIFCM**,  
  conformément aux équations et au pseudo-code de l’article (initialisation, PSO, IFCM) ;
- la **reproduction partielle des expériences** de Kumar & Kumar (2022) ;
- l’application de l’algorithme à plusieurs jeux de données (Iris, Wine, Two Moons, etc.) ;
- la génération de **visualisations** (ACP, affichage des clusters, trajectoires des centroïdes) ;
- l’analyse de la qualité du clustering via différentes métriques.


---

## **3. `Particle_swarm_optimization.ipynb`**

Ce notebook est consacré à une **étude du PSO lui-même**, indépendamment du clustering.

Il permet notamment :

- de **réimplémenter un PSO générique** capable de minimiser n’importe quelle fonction,
- de tester l’algorithme sur des **fonctions 2D visualisables** (Himmelblau, Rastrigin, etc.) ;
- de **visualiser dynamiquement** les particules : trajectoires, courbes de niveau ;
- d’étudier l’impact des hyperparamètres : inertie $\omega$, coefficients $c_1$, $c_2$, taille d’essaim, etc.




