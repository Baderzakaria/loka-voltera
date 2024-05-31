## Épidémiologie computationnelle : Simulation du modèle SIRD avec optimisation des paramètres

 Bonjour les data enthusiasts et les passionnés d'épidémiologie ! 

Ce projet vous invite à explorer la modélisation mathématique des épidémies   à l'aide du modèle SIRD (Susceptibles, Infectés, Rétablis, Décédés) et de la méthode d'Euler pour résoudre numériquement les équations différentielles associées.  

On se concentre ensuite sur l'ajustement des paramètres du modèle à des données empiriques  en utilisant une recherche par grille et en analysant l'impact des interventions sur la dynamique de l'épidémie .

### Fonctionnalités

* **Implémentation du modèle SIRD**  :
    * Définition des variables d'état (S, I, R, D) et des paramètres (β, γ, μ).
    * Discrétisation des équations différentielles SIRD par la méthode d'Euler.
    * Fonction `euler` pour simuler l'évolution de l'épidémie sur une période donnée. ⏳
* **Ajustement des paramètres du modèle** :
    * Lecture des données épidémiques à partir d'un fichier CSV. 
    * Définition d'une fonction de coût pour mesurer l'écart entre les données observées et les résultats du modèle SIRD. ⚖️
    * Utilisation de la recherche par grille pour trouver les valeurs optimales des paramètres β, γ et μ qui minimisent la fonction de coût. 
* **Analyse de scénarios de contrôle** :
    * Calcul du paramètre R0 (nombre de reproduction de base) à partir des paramètres β, γ et μ. 
    * Simulation de l'impact d'une intervention réduisant le taux de transmission (β) sur la dynamique de l'épidémie. 
    * Comparaison des scénarios avec et sans intervention à l'aide de graphiques. 

### Structure du code 

Le code est organisé en plusieurs fichiers Python :

* `modele_sird.py` : contient la définition du modèle SIRD et la fonction `euler` pour la simulation. ⚙️
* `ajustement_parametres.py` : implémente les fonctions de lecture des données, de calcul du coût et la recherche par grille. 
* `analyse_scenarios.py` : définit les fonctions de calcul de R0 et de comparaison des scénarios avec et sans intervention.  🆚
* `principal.py` : script principal qui orchestre l'exécution des modules précédents et génère des visualisations. 

### Instructions d'exécution 

1. **Cloner le dépôt** : utilisez `git clone` pour cloner ce dépôt localement.
2. **Installer les librairies requises** : exécutez `pip install numpy matplotlib pandas` dans votre terminal pour installer les librairies nécessaires.
3. **Exécuter le script principal** : lancez le script `principal.py` avec Python.

Le script générera des graphiques illustrant l'évolution de l'épidémie dans les scénarios avec et sans intervention. 

### Données 

Le jeu de données simulé des cas d'infection est fourni dans le fichier `sird_dataset.csv`.

### Conclusion 

Ce projet permet d'explorer la modélisation des épidémies et l'impact des interventions sur leur propagation. Les limitations des modèles simples comme le SIRD et l'importance de la prise en compte des incertitudes sur les paramètres sont à garder à l'esprit.  ⚠️

### Améliorations possibles 

* Intégration de modèles épidémiologiques plus complexes. 
* Prise en compte de l'hétérogénéité de la population et des structures des contacts. 
* Utilisation de méthodes d'optimisation plus sophistiquées pour l'ajustement des paramètres. 
* Analyse de sensibilité pour évaluer l'impact de l'incertitude sur les paramètres.  ⚖️

Ce projet constitue une base solide pour une exploration plus approfondie de la modélisation mathématique des épidémies. 
