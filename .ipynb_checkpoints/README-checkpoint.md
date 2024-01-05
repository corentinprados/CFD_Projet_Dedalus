# Informations sur ce dépôt

- Ce projet a été réalisé dans le cadre du cours de M2 de Computational Fluid Dynamics à l'ENS de Lyon
- Il est centré autour du framework Dedalus.
- Il est décomposé en N Notebook résumé ci-dessous dans la tables des matières 
  
# Motivations

J'ai découvert personnellement ce framework lors d'un stage de M1 à l'ENS de Lyon, encadré par Louis-Alexandre Couston. Ce stage portait sur l'influence de la forme de l'interface eau-glace sur les propriétés d'un écoulement de Poiseuille. Vous pouvez consulter le rapport de ce stage à ce lien : [Rapport de stage](https://louiscouston.github.io/files/M1SDM_STAGE_Prados_Corentin.pdf).

Pour simuler cet écoulement, j'ai utilisé Dedalus, un outil remarquablement user-friendly qui permet, en peu de temps grâce aux exemples fournis sur le site, de réaliser des simulations d'écoulements en mécanique des fluides. Comme de nombreux utilisateurs de ce framework, je n'ai pas immédiatement cherché à comprendre son fonctionnement interne.

L'objectif principal de ce projet est d'acquérir une compréhension approfondie des bases numériques sous-jacentes à Dedalus, en mettant particulièrement l'accent sur une méthode spécifique appelée la méthode tau. Ce projet vise à m'aider à comprendre le fonctionnement de Dedalus, mais il est également ouvert à toute personne souhaitant découvrir ou approfondir ses connaissances sur le sujet. Je suis naturellement ouvert à toute critique constructive et à tout complément qui serait accueilli avec enthousiasme.

# Références 

Ce projet s'appuie principalement sur le papier suivant :

> K J Burns, G M Vasil, J S Oishi, D Lecoanet, B P Brown, "Dedalus: A Flexible Framework for Numerical Simulations with Spectral Methods," Physical Review Research, vol. 2, no. 2, Apr. 2020.

Ainsi que sur le site et la documentation associée au projet Dedalus :
- Index du site : [https://dedalus-project.org/index.html](https://dedalus-project.org/index.html)
- Documentation : [https://dedalus-project.readthedocs.io/en/latest/index.html](https://dedalus-project.readthedocs.io/en/latest/index.html)

Les documents complémentaires utilisés seront cités lors de leur utilisation.

# Construction du projet 

Les auteurs du projet Dedalus ont opté pour des explications concises, ce qui, de mon point de vue, peut rendre la lecture du papier difficile sans une connaissance préalable du sujet.

Les Jupyter Notebooks rédigés ont donc pour objectif de détailler et d'expliquer chaque point du papier, dans le but de créer une explication pédagogique des choix de la méthode numérique utilisée par les auteurs. Chaque principe sera illustré d'exemples.

Ce travail a été réalisé de manière individuelle, il est donc probablement incomplet et peut contenir des erreurs (y compris dans la compréhension des notions). Les notebooks ont été construits selon le cheminement intellectuel que j'ai suivi pour comprendre les prémices de la méthode tau. La construction des notebooks est progressive, ajoutant peu à peu chaque notion utile pour finalement arriver à la méthode globale utilisée.

Le papier étant riche en informations, ce projet se limite à la partie "SPARSE SPECTRAL METHODS". La partie "Fundamentals of spectral methods" est traité dans le notebook "1_Fondamentaux_sur_les_méthodes_spectrales" et celle nommée "A general sparse tau method" dans le notebook "2_Methode_tau_generale_avec_matrices_creuses".

**À terminer**



# Tables des matières 

## 0. Introduction
- Les différentes méthodes numériques
- Pourquoi le projet Dedalus ?

## 1. Fondamentaux sur les méthodes spectrales

### 1.1. Méthode spectrale classique
1. Principe : décomposition et projection du problème dans une base
2. Exemple de la base de Fourrier : référence pour les problèmes périodiques
3. Exemples des Polynômes de Chebyshev : premier aperçu de la famille

> Remarques importantes :
> - Représentation spectrale numérique des fonctions
> - Calcul de produit matriciel
> - Notion de matrice dense et de matrice creuse/sparse

### 1.2. Méthode de Galerkin
1. Principe : décomposition la base d'essaie et projection dans la base de test
2. Exemples des polynômes de Chebyshev : référence pour les problèmes non périodiques

> Remarque importantes :
> - Choix de la base d'essaie et la base de test
> - Diagonalité d'un matrice diagoanle décalée 

### 1.3. Prise en compte des conditions aux bords
1. La méthode de "collocation" : approximation aux points spécifiques du domaine
2. Méthode "tau" : résolution exacte par ajout de termes

### 1.4 Résumé de la partie



## 2. Méthode tau générale avec matrices creuses

### 2.1. Principe numérique de la méthode tau
1. Ajout du terme tau et application de la méthode de Galerkin
2. Choix du polynôme associé
3. Écriture condensée du problème
4. Application à un exemple simple : dérivée d'ordre un

> Remarques importantes :
> - LHS, simplicité de la méthode tau en pratique
> - RHS, attention au terme ajouté
> - Permutation des lignes dans la représentation matricielle

### 2.2. Méthode de recombinaison de Dirichlet 
1. Conditions de Dirichlet et de Neumann
2. Préconditionnement de Dirichlet
3. Retour sur l'exemple de la dérivée d'ordre un

> Remarques importantes :
> - Diagonalité de la matrice de changement de base
> - Expression des conditions aux limites
> - Matrice à bande

### 2.3 Systèmes d'équations au-delà du premier ordre
1. Introduction : changement de point de vue

   a. Principe : d'une équation d'ordre $N$ à $N$ équations d'ordre un
   
   b. Exemple : l'équation de Poisson
   
   c. Généralisation à tout système
   
3. Résolution des systèmes sous forme d'équations du premier ordre
   
   a. Principe de base : une méthode en six étapes
   
   b. Exemple : Retour sur l'équation de Poisson
   
   c. Généralisation : Application de la méthode bloc par bloc
   
5. Renversement de produit de Kronecker
   
   a. Définitions : Produit de Kronecker et matrices élementaires
   
   b. Rédaction alternative de la méthode bloc par bloc
   
   c. Application au résultat de l'équation de Poisson

   
### 1.4 Résumé de la partie
