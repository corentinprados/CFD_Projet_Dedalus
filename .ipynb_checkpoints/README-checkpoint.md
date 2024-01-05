# Informations sur ce dépôt

- Ce projet a été réalisé dans le cadre du cours de M2 de Computational Fluid Dynamics à l'ENS de Lyon
- Il est décomposé en N Notebook résumé ci-dessous
- 
## Objectifs du projet
L'objectif de l'ensemble des Jupyter Notebooks de ce projet est de fournir une compréhension approfondie des bases algorithmiques sous-jacentes au projet Dedalus.

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

# 2.2. Méthode de recombinaison de Dirichlet 
1. Conditions de Dirichlet et de Neumann
2. Préconditionnement de Dirichlet
3. Retour sur l'exemple de la dérivée d'ordre un

> Remarques importantes :
> - Diagonalité de la matrice de changement de base
> - Expression des conditions aux limites
> - Matrice à bande

# 2.3 Systèmes d'équations au-delà du premier ordre
1. Introduction : changement de point de vue 
   a. Principe : d'une équation d'ordre $N$ à $N$ équations d'ordre un
   b. Exemple : l'équation de Poisson
   c. Généralisation à tout système 
2. Résolution des systèmes sous forme d'équations du premier ordre
   a. Principe de base : une méthode en six étapes
   b. Exemple : Retour sur l'équation de Poisson
   c. Généralisation : Application de la méthode bloc par bloc
3. Renversement de produit de Kronecker
   a. Définitions : Produit de Kronecker et matrices élementaires
   b. Rédaction alternative de la méthode bloc par bloc
   c. Application au résultat de l'équation de Poisson

   
### 1.4 Résumé de la partie