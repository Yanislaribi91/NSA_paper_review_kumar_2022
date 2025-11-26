# NSA_paper_review_kumar_2022

# Reproduction et exploration de l’article Kumar & Kumar (2022)

Ce dépôt contient le code que nous avons développé pour :

1. **reproduire partiellement les résultats de l’article de Kumar & Kumar (2022)**  
   (« An improved fuzzy clustering algorithm based on particle swarm optimization »),  

2. **expérimenter plus en profondeur certaines des techniques introduites dans l’article**,  
   notamment l’optimisation par essaim de particules (PSO) et le clustering flou (IFCM).

Trois notebooks composent ce repo, dont le contenu de chacun est détaillé ci-après :

---

## **1. `comparaison_algo_clustering_kumar2022.ipynb`**

Ce notebook regroupe une **comparaison pratique entre plusieurs algorithmes de clustering** :

- PSOIFCM (implémentation basée sur l’article),
- FCM classique,
- K-means,
- d’autres méthodes de référence disponibles dans `scikit-learn`.

Objectifs du notebook :

- comparer les partitions obtenues sur différents jeux de données (réels et artificiels),
- analyser l’influence de la distance modifiée $d_{\mathrm{new}}$,
- mesurer et visualiser des métriques comme l’accuracy, l’ICD, ou la fonction objectif OFV.

Ce notebook sert de **module de validation expérimentale** pour situer PSOIFCM par rapport à des méthodes standard.

---

## **2. `PSOIFCM_reproduction_kumar_2022.ipynb`**

Il s’agit du **notebook principal**, dédié à :

- l’implémentation complète de l’algorithme **PSOIFCM**,  
  conformément aux équations et au pseudo-code de l’article (initialisation, PSO, IFCM) ;
- la **reproduction partielle des expériences** de Kumar & Kumar (2022) ;
- l’application de l’algorithme à plusieurs jeux de données (Iris, Wine, Two Moons, etc.) ;
- la génération de **visualisations** (ACP, affichage des clusters, trajectoires des centroïdes) ;
- l’analyse de la qualité du clustering via différentes métriques.

Ce notebook constitue le **cœur de notre reproduction**, avec un code documenté et commenté.

---

## **3. `Particle_swarm_optimization.ipynb`**

Ce notebook est consacré à une **étude approfondie du PSO lui-même**, indépendamment du clustering.

Il permet notamment :

- de **réimplémenter un PSO générique** capable de minimiser n’importe quelle fonction,
- de tester l’algorithme sur des **fonctions 2D visualisables** (Himmelblau, Rastrigin, etc.) ;
- de **visualiser dynamiquement** les particules : trajectoires, convergence, courbes de niveau ;
- d’étudier l’impact des hyperparamètres : inertie $\omega$, coefficients $c_1$/$c_2$, taille d’essaim, etc.

Ce notebook nous a servi à mieux comprendre les **mécanismes internes de PSO** et à justifier certains choix dans l’algorithme PSOIFCM.

---

## **Contenu complémentaire**

Le dépôt inclut également :

- des fonctions utilitaires pour le calcul de la distance $d_{\mathrm{new}}$ et des critères IFCM,
- des routines de visualisation (ACP, scatter plots, animations PSO),
- divers tests sur des jeux de données réels et simulés,
- des commentaires détaillés concernant les équations tirées du papier.

---

## **Objectif pédagogique**

Au-delà de la reproduction de l’article, ce projet nous a permis de :

- approfondir PSO et le clustering flou,
- analyser rigoureusement les choix méthodologiques de l’article,
- développer une implémentation complète, modulaire et commentée,
- expérimenter de manière contrôlée sur différents jeux de données.

---

N’hésitez pas à consulter les notebooks dans l’ordre indiqué pour suivre le déroulement logique de notre étude.

